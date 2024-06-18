import string
import random
import sys
import argparse

vowels = "aoeuiy"


def check_positive(value):
    ivalue = int(value)
    if ivalue <= 0:
        raise argparse.ArgumentTypeError("%s needs to be positive" % value)
    return ivalue


def m():
    yield 'z' + vowels[random.randint(0, len(vowels) - 1)] + string.ascii_lowercase[
        random.randint(0, len(string.ascii_lowercase) - 1)
    ]


def main():
    # Create an argument parser
    parser = argparse.ArgumentParser(description='Generate random strings.')

    # Add an argument
    parser.add_argument("num", help="display random strings", type=check_positive)

    # Parse the arguments
    args = parser.parse_args()

    for x in range(args.num):
        for value in m():
            print(value, end="\t")


if __name__ == "__main__":
    main()
