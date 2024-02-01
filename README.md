#include <iostream>

class Transport {
public:
    Transport() {
        std::cout << "Transport constructor\n";
    }

    virtual ~Transport() {
        std::cout << "Transport destructor\n";
    }

    virtual void print() const {
        std::cout << "Transport\n";
    }
};

class Car : public Transport {
public:
    Car() {
        std::cout << "Car constructor\n";
    }

    ~Car() override {
        std::cout << "Car destructor\n";
    }

    void print() const override {
        std::cout << "Car\n";
    }
};

class Truck : public Transport {
public:
    Truck() {
        std::cout << "Truck constructor\n";
    }

    ~Truck() override {
        std::cout << "Truck destructor\n";
    }

    void print() const override {
        std::cout << "Truck\n";
    }
};

class Steamship : public Transport {
public:
    Steamship() {
        std::cout << "Steamship constructor\n";
    }

    ~Steamship() override {
        std::cout << "Steamship destructor\n";
    }

    void print() const override {
        std::cout << "Steamship\n";
    }
};

class Airplane : public Transport {
public:
    Airplane() {
        std::cout << "Airplane constructor\n";
    }

    ~Airplane() override {
        std::cout << "Airplane destructor\n";
    }

    void print() const override {
        std::cout << "Airplane\n";
    }
};

int main() {
    Transport transport;
    Car car;
    Truck truck;
    Steamship steamship;
    Airplane airplane;

    std::cout << "\nTesting polymorphism:\n";
    Transport* polymorphicArray[] = {&car, &truck, &steamship, &airplane};
    for (const auto& vehicle : polymorphicArray) {
        vehicle->print();
    }

    return 0;
}
