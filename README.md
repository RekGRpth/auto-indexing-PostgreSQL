# Auto-Indexing in PostgreSQL

> This (toy)-project uses various strategies to automatically maintain indices by dynamically adapting the database workload in PostgreSQL.

You may want to check out the [report.pdf](/docs/report.pdf) file for more details. It was made as the final project for CS 387 - **Database and Information Systems Lab** course in Autumn 2018 at Indian Institute of Technology (IIT) Bombay, India.

## Getting Started

Follow the instructions below to get our project running on your local machine.

1. Get the source code for PostgreSQL and clone this repository.
2. Replace `postgres.c` at (`/src/backend/tcop/`) and `execMain.c` at (`/src/backend/executor/`) in PostgreSQL source and install it.
3. Now, run the `main.py` file and start using your database.

### Prerequisites

- psycopg2 - Install psycopg2 from PyPI using the command `pip3 install psycopg2`.

- HypoPG  - Follow the instructions at [GitHub](https://github.com/HypoPG/hypopg) to install.
- libpg_query - Follow the instructions at [GitHub](https://github.com/lfittl/libpg_query) to install.

## Built With

* PostgreSQL
* Python3 - All the strategies we deployed are coded as a Python3 script ([main.py](src/main.py)) as well as the tests.
* [psycopg2](http://initd.org/psycopg/) - The PostgreSQL adaptor we use to interact with PostgreSQL database in Python code.
* HypoPG extension for PostgreSQL - For more efficient decisions about auto-indexing.
* libpg_query - To fingerprint the queries creating same hashes for queries with similar internal PostgreSQL parse tree

## Authors

* **Vamsi Krishna Reddy Satti** - [vamsi3](https://github.com/vamsi3)
* Vighnesh Reddy Konda - [scopegeneral](https://github.com/scopegeneral)
* Niranjan Vaddi
* Sai Praneeth Reddy Sunkesula - [praneeth11009](https://github.com/praneeth11009)

## Acknowledgements

- [**Julien Rouhaud**](https://github.com/rjuju) for the **HypoPG** extension.
- [**Lukas Fittl**](https://github.com/lfittl) for the **libpg_query** code.
- [**Prof. S. Sudarshan**](https://www.cse.iitb.ac.in/~sudarsha/) for his important guidance and ideas throughout our work on this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

### Caution!

This is a toy project and is not complete. It was just done to learn about internals of PostgreSQL and databases in general along with various indexing strategies. So, feel free to utilise this work further at your own risk.