#include <iostream>
#include <map>
#include <string>

int main() {
    std::map<std::string, std::string> bookMap;
    bookMap["9780132350884"] = "The C++ Programming Language";
    bookMap["9780321563842"] = "Effective C++";
    bookMap["9780201633610"] = "Design Patterns";
    std::string inputISBN;
    std::cout << "Enter the ISBN: ";
    std::cin >> inputISBN;
    auto bookIterator = bookMap.find(inputISBN);
    if (bookIterator != bookMap.end()) {
        std::cout << "Book Title: " << bookIterator->second << std::endl;
    } else {
        std::cout << "Book not available in the library." << std::endl;
    }

    return 0;
}
