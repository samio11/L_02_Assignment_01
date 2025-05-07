## Question-01:- What are some differences between interfaces and types in TypeScript?

# Ans:-

1. Interface can be extend by (extends) keyword, for types it can be extended by (&) keyword

interface IPerson {
name: string;
age: number;
}
interface IPersonAddRole extends IPerson {
role: "Admin" | "User";
}

type TPerson = {
name: string;
age: number;
};
type TPersonAddRole = TPerson & { role: "Admin" | "User" };

2. Interface Preferred for defining object shapes, Types More flexible for complex type combinations

## Question-02:- What is the use of the keyof keyword in TypeScript? Provide an example.

# Ans:-

When we need to get only the key of types/interface we use it, for dynamically getting all keys value in Optional way

type TVehicles = {
car: string;
bike: string;
boat: string;
};

//We want type like this "car" | "bike" | "boat"

type TOwnVehicles = keyof TVehicles;
