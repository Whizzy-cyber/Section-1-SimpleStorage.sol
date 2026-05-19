# Section-1-SimpleStorage.sol

// SPDX-License-Identifier: MIT    Test me on function
pragma solidity ^0.8.19;
// contract SimpleStorage{
 // Basic Storage values 
//     bool hasFavoriteNumber = true;
//     uint256 favoriteNumber = 88;
//     string favoriteNumberInText = "eighty-eight";
//     int256 favoriteInt = -88;
//     address myAddress = 0xAB1b7206aa6840C795aB7A6AE8b15417B7E63A8D;
//     bytes32 favoriteBytes32 = "cat";
// }

// contract VisibiltyExample {
//     uint256 internal number = 10;
// // 1. View function accessible only inside this contract
// function privateViewFunction()
// private view returns(uint256){
//     return number;
// }
// // 2. Pure function not accessible internally
// function externalPureFunction(uint256 a, uint256 b) 
// external pure returns(uint256){
//     return a + b;
// }
// // 3. View function accessible in children contracts
// function internalViewFunction()
// internal view returns(uint256){
//     return number;
// function publicViewFunction()
// public view returns(uint256){
//     return number;
//}}
// }

// Test me on Arrays & Structs
// contract ListofAnimals {
// //Dynamic array to store animals
// string[] public animals = ["Dog", "Cat", "Lion"];

// // function to add more animals
// function addAnimal(string memory _animal) public {
//     animals.push(_animal); 
// } 

// // function to view all animals
// function getAnimals() public view returns(string[] memory){
//     return animals;
// }
// }

// Test me on Array & Structs
// contract ListofFruits {
// // Dynamic array to store fruits
// string[] public fruits = ["Banana", "Apple", "Pineapple"];

// // function to add more fruits
// function addFruit(string memory _fruit) public {
//     fruits.push(_fruit);
// }

// // function to view all fruits
// function getFruits() public view returns(string[] memory){
//     return fruits;
// }
// }

// Test me on calldata, memory, storage
// contract DataLocations {
//     // Step 1: Create State Variable(Storage variable): stored permanently on-chain
//     string public name;
//     // Step 2: create function using calldata: read-only temporary data
//     function setName(string calldata _name) external {

//         // Step 3: Use memory: temporary writable code
//         string memory temporaryName = _name;
        
//         // Step 4: Update storage varible: Blockchain state updates
//         name = temporaryName;
//     }
// }

// Test me on Mappings
contract AddressToBalance{
    // variables needed: uint & address
    // Mapping
    mapping(address => uint256) public addressToBalance;

    // Function to store balance 
    function store(uint256 _balance) public {

        // msg.sender = address calling the function here the wallet address currently calling the function. For example if you call store(500), the address gets linked to 500
        addressToBalance[msg.sender] = _balance; // here it stores the balance for the address calling the function
    }

    // Funtion to retrive balance
    function retrive(address _user) public view returns(uint256){
        return 
        addressToBalance[_user];
    }
}
 
