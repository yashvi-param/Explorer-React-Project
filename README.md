explorer-studentdata-react.netlify.app/

Features

Add new products

Update existing products

Redux Toolkit state management

Auto-fill form when editing a product

Controlled form inputs

Single form for Add / Update

Clean and reusable logic

| Field    | Description            |
| -------- | ---------------------- |
| Name     | Product name           |
| Price    | Product price          |
| Category | Product category       |
| Quantity | Product stock quantity |

🛠️ Technologies Used

React

Redux Toolkit

React Redux Hooks (useDispatch, useSelector)

JavaScript (ES6+)


📦 Redux Structure
Redux Slice Location
src/futures/Products/productSlice.js

Actions Used
Action	      Description
addProduct	  Adds a new product
updateProduct  	Updates an existing product
setUpdateState	  Sets or clears update mode

🧠 Component Logic Overview
Local State
const [product, setProduct] = useState({
    name: "",
    price: "",
    category: "",
    qty: 10,
});


Manages form inputs

Resets after submit


Add Product Flow

User fills the form

Clicks Submit

addProduct action is dispatched

Product is stored in Redux

Alert confirms addition

Update Product Flow

User selects a product to edit

updateState is set in Redux

useEffect populates the form

User edits details

Clicks Update

updateProduct action is dispatched

Update state is cleared


🔄 useEffect for Edit Mode
useEffect(() => {
    if (updateState) {
        setProduct(updateState.product);
    }
}, [updateState]);


Automatically fills form when updating a product

📄 Component Usage
import InputForm from "./components/InputForm";

function App() {
    return (
        <div>
            <InputForm />
        </div>
    );
}

export default App;
🎯 Button Behavior

| Mode   | Button Text |
| ------ | ----------- |
| Add    | Submit      |
| Update | Update      |



📌 Folder Structure Example
src/
 ├── components/
 │    └── InputForm.jsx
 ├── futures/
 │    └── Products/
 │         └── productSlice.js
 ├── store.js
 └── App.js

 ✅ Future Enhancements

Form validation

Toast notifications instead of alerts

Persist data with localStorage or API
ling (Bootstrap / Tailwind)

Search and filter products

📜 License

This project is open-source and intended for learning and practice purposes.


UI sty<img width="1651" height="816" alt="Screenshot 2025-12-29 202341" src="https://github.com/user-attachments/assets/50280d5d-a4f7-4b20-87bf-ccdf422c0576" />

