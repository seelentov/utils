compile-files:
	@find -name "*.cpp" -not -name "main.cpp" -print0 | xargs -0 g++ -c >/dev/null 2>&1 || true 
	
compile-main:
	@g++ main.cpp *.o -o main >/dev/null 2>&1 || g++ main.cpp -o main

compile:
	@make compile-files
	@make compile-main

clear:
	@rm -rf *.o && rm main

execute:
	@./main

execute-print:
	@make execute > result.txt

compile-execule:
	@make compile
	@make execute
	@make clear

run:
	@make compile-execule | grep -v "make\[.*\]:.*"
