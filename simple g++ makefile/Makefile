compile-files:
	@find -name "*.cpp" -not -name "main.cpp" -print0 | xargs -0 g++ -c
	
compile-main:
	@g++ main.cpp *.o -o main

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
