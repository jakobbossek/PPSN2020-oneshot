# File format of evaluations.csv
===

* Column seperator is a single whitespace
* First row contains columns names

# Note
===

ALL *.diff values are absolute values (not squared)

# Column names
===

* repl:               Replication of experiment
* time.running:       Running time in seconds
* algorithm:          Constant value EVALUATOR; not relevant
* design:             Absolute path to design in file system
* fid:                BBOB function identifier
* iid:                BBOB instance identifier
* learner:            Learning method / surrogate model
* destype:            Type of design, e.g., UNIFORM or LHS
* n.points:           Number of points
* dimension:          Dimension of underlying problem
* performance.test:   MSE (mean squared error) on test data
* performance.train:  MSE on training data
* min.y.diff:         Minimal squared distance between model and true function on test data
* opt.diff:           Difference between known global optimum of true function and result of hillclimbing from the best point in the test data
* opt.diff2:          Difference between true function value at "optimal" parameter value determined by hillclimber (see opt.diff) and the corresponding value of the surrogate
* des.diff:           Difference of best point from "test data" to global opt
* des.diff2:          ... and the difference to the corresponding fitness value at its location
* des.diff3:
* y.opt:              Known value f(x*) of global optimum of the function.
* yhat.opt:           fhat(x*)
* y.best.design:      f(x**) where x** is the the design point with minimal fhat(x**) value
* yhat.best.design:   fhat(x**)
* y.best.bfgs:        f(z) where z is the final point of BFGS started from x**
* yhat.best.bfgs:     fhat(z)
* discrepancy:        Discrepancy value of design (NA value if not available due to high computational costs)
* best.in.design.val: min_i f(x_i) (best design point - classical one shot setting)
* opt.diff4:          min_i f(x_i) - f(x*)
* opt.diff4.decision: Euclidean distance of argmin_i f(x_i) and x* (Euclidean distance makes more sense in decision space)
