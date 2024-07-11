# json_parser
JSON解析器，使用C++实现
# 使用方式
    int main() {
        std::ifstream fin("json.txt");
        std::stringstream ss; ss << fin.rdbuf();
        std::string s{ ss.str() };
        auto x = parser(s).value();
        std::cout << x << "\n";
        std::cout << x["123"] << std::endl;
    }
