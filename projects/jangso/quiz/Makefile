CFLAGS = -Wall -fpic -coverage -lm

testme: testme.c
	gcc -o testme.exe -g testme.c  $(CFLAGS)

runtests: testme
	touch unittestresult.out
	./testme.exe &> unittestresult.out

coverage:
	gcov testme.c &> coverage.out
	cat coverage.out

clean:
	rm -rf *.o *.exe *.gcov *.gcda *.gcno *.so *.out *.dSYM
