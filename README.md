# NileFin Mission A: Repair the Model

**Team A:** Nankya Zaharah, Mbabazi Angel, Nambooze Hellen Noeline

## Mission description

NileFin stores its customer records as plain Python lists, such as `["C101", "Amina", "Kampala"]`. The meaning of each value depends only on its position. NileFin also has transactions, support records, duplicates and missing values, and management is asking about prediction, so the customer data is going to grow.

Our mission is to **repair the customer model**: pick a data representation that makes NileFin's everyday operations easy and safe, and back that choice with runnable evidence.

The operations the model has to support are:

1. Find a customer by ID
2. Find customers by city
3. Add a new customer

### What the mission asks for

- Compare possible representations (list, dictionary, dataclass)
- Implement two of them (we chose a **list** and a **dataclass**)
- Show where the list works well and where it causes mistakes
- Recommend one representation and defend the choice
- Provide runnable proof, the trade-off, and one unresolved question

## Our answer

| | |
|---|---|
| **Chosen representation** | Dataclass (`Customer` with `customer_id`, `name`, `city`) |
| **Why** | Named fields make the data easier to read and maintain. A list silently accepted `["Amina", "C105", "Kampala"]` with the ID and name swapped. |
| **Runnable proof** | The "Runnable proof" section of the notebook finds a customer by ID, filters by city and adds a customer, all using the dataclass. |
| **Trade-off** | A dataclass needs more setup than a list. A list is fine for a small, throwaway script. |
| **Assumption** | Customer data will grow, and customer IDs are unique. |
| **Unresolved question** | How should NileFin handle duplicate or missing customer information? Must IDs be unique, can names repeat, and must every customer have a city? |

## Open the notebook

Open [NileFin_Mission_A_Repair_the_Model.ipynb](NileFin_Mission_A_Repair_the_Model.ipynb) in VS Code with the Jupyter extension, or use JupyterLab. Run the cells from top to bottom.

## Requirements

- Python 3
- Jupyter Notebook support

The notebook uses only Python's built-in data structures and does not require external datasets or third-party Python packages.
