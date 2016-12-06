# PairwiseComparisons library

### The repository contains:
* R file - responsible for computes
* .jar library
* Java source code of the library
* Example project in Java, which shows the use of the library

### In order to use PairwiseComparisons library in own project need to:
1. Install R package (http://cran.us.r-project.org/)
2. Download pairwiseComparisons.R file.t
3. Add PairwiseComparisons.jar to project build path.
4. Import class _main.out.pl.edu.agh.talaga.PairwiseComparisons_.
5. Create new object PairwiseComparisons. You can give the path to pairwiseComparisons.R file as parameter in constructor or place it in the main project folder.
6. Call methods.

### Additional information to help you use the library:
1. Library can work in continous mode (one permanent connection) or disposable mode (one connection for every function call).
Contionus mode works faster with greater number of function calls, but you be should close connection when it will no longer be used.

2. Default constructor switch continous mode. In order to change mode, you should call constructor with parameter false: ``new PairwiseComparisons(false)``.

3. Function ``seetKeepOpenConnection(boolean)`` is also used for determining the mode library. It can be called many times during the runtime.

4. Functions _open_ and _close_ allow open/close connection manually.