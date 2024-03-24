#include <iostream>
#include <fstream>
#include <vector>
#include <string>

int main() {
    std::ifstream input_file("river.txt");
    std::ofstream output_file("text.txt");

    if (!input_file.is_open()) {
        std::cerr << "Error 404\n";
        return 1;
    }

    if (!output_file.is_open()) {
        std::cerr << "Error 404\n";
        return 1;
    }

    std::vector<std::string> coordinates_x;
    std::vector<std::string> coordinates_y;

    std::string line;
    while (std::getline(input_file, line)) {
        size_t space_pos = line.find(' ');
        if (space_pos != std::string::npos) {
            coordinates_x.push_back(line.substr(0, space_pos));
            coordinates_y.push_back(line.substr(space_pos + 1));
        }
        else {
            coordinates_x.push_back(line);
        }
    }

    for (const auto& x : coordinates_x) {
        output_file << x << " ";
    }
    output_file << "\n";
    for (const auto& y : coordinates_y) {
        output_file << y << " ";
    }

    input_file.close();
    output_file.close();

    return 0;
}
