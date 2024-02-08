# TEAM_iCuHack
We participated in AWS iQuHACK 2024 In-Person Challenge.
This is our repo and we have short slides about our noise aware compilation of
AWS Braket circuits.
[Link to our slides](https://docs.google.com/presentation/d/1j7Nu_adU32vfPOUmudidZ-MPrti-X4SPa5-mQk71t44/edit?usp=sharing)

![Technical Diagram iQuHack drawio](https://github.com/codejoey/2024_AWS_iQuHack/assets/31334632/4452ea6d-5b33-484e-b341-b3d5316d3b97)
Quiet Quacks is a noise aware compiler for quantum circuits. Built for AWS Braket and quantum computing interfacing. It consists of three components: qubit fidelity optimisation, ZX calculus circuit redesign, and a noise testing suite.
My contribution was the noise testing suite, slides, logo, design diagram, and engaging stakeholders for refinement.

## Instructions: Trying out our compiler
**First,** fork the repo and open it in your terminal.

**Second,** activate your virtual enviornment to run poetry.
```
source .venv/bin/activate
```

**Third,** install `poetry` to install our package (our compiler) and its dependencies.
```
poetry install
```

**Finally,** using the following line of code you can test our compiler!
```
# Compile the demo circuit with our compiler
python compiler.py demo1.py candidate_pair.json

# Execute the compiled file with python
python demo1_compiled.py
```

Of course, you can run `demo1.py` directly with pyton (withour our compiler) to run the code
directly on an AWS Braket backend.
```
python demo1.py
```

In general,
```
python compiler.py <circuit>.py <optional candidate pair>.json

python <circuit>_compiled.py
```

If you'd like to print out the intermediate representations, you will have to edit the compiler.py file to print things like the CircuitDSL representation, ZX Caculus, or the generated circuit QASM.

Enjoy!
