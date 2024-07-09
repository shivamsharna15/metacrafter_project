# metacrafter_project

create-a-token-metacrafter
This project is a Solidity assessment for Metacrafter, where you will create a token contract with specific requirements.

Requirements

Public Variables Token Name Token Abbreviation Total Supply
Mapping Variable address => uint mapping to store the balances
Mint Function Takes two parameters: address and value Increases the Total Supply by the value Increases the balance of the address by the value
Burn Function Takes two parameters: address and value it is used to decrease the supply Decreases the Total Supply by the value Decreases the balance of the address by the value Has a conditional to ensure the balance of the address is greater than or equal to the value
Running the Program To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website.

**Executing program**
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:
contract MyToken {
    // public variables
    string public tokenName;
    string public tokenAbb;
    uint public allSupply;

    // mapping variable
    mapping(address => uint) public balances;

    // constructor
    constructor() {
        tokenName = "ElonMusk";
        tokenAbb = "EMK";
        allSupply = 50000;
    }

    // mint function
    function mint(address _address, uint _value) public {
        allSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        require(balances[_address] >= _value, "Insufficient balance");
        allSupply -= _value;
        balances[_address] -= _value;
    }
}

We goto "DEPLOY & RUN TRANSACTIONS" and click on Deploy . Then click on "Deployed/Unpinned Contracts". Then we can copy Account id and we do further use of mint and burn function . We can also do check our "Tokenname, Token Abb, allSupply " values there.
