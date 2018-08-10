# Hands-on Blockchain with Hyperledger

<a href="https://www.packtpub.com/big-data-and-business-intelligence/hands-blockchain-hyperledger?utm_source=github&utm_medium=repository&utm_campaign=9781788994521"><img src="https://d255esdrn735hr.cloudfront.net/sites/default/files/imagecache/ppv4_main_book_cover/B10152_Newcover.png" alt="Hands-on Blockchain with Hyperledger" height="256px" align="right"></a>

This is the code repository for [Hands-on Blockchain with Hyperledger](https://www.packtpub.com/big-data-and-business-intelligence/hands-blockchain-hyperledger?utm_source=github&utm_medium=repository&utm_campaign=9781788994521), published by Packt.


## What is this book about?
Blockchain and Hyperledger technologiesare hot topics today. Hyperledger Fabric and Hyperledger Composer are open source projects that help organizations create private, permissioned blockchain networks. These find application in finance, banking, supply chain, and IoT among several other sectors. This book will be an easy reference to explore and build blockchain networks using Hyperledger technologies.

This book covers the following exciting features: 
* Discover why blockchain is a game changer in the technology landscape
* Set up blockchain networks using basic Hyperledger Fabric deployment
* Understand the considerations for creating decentralized applications
* Learn to integrate business networks with existing systems
* Write Smart Contracts quickly with Hyperledger Composer

If you feel this book is for you, get your [copy](https://www.amazon.com/dp/1788994523) today!

<a href="https://www.packtpub.com/?utm_source=github&utm_medium=banner&utm_campaign=GitHubBanner"><img src="https://raw.githubusercontent.com/PacktPublishing/GitHub/master/GitHub.png" 
alt="https://www.packtpub.com/" border="5" /></a>


## Instructions and Navigations
All of the code is organized into folders.

The code will look like the following:

func checkInit(t *testing.T, stub *shim.MockStub, args [][]byte) {
 res := stub.MockInit("1", args)
 if res.Status != shim.OK {
 fmt.Println("Init failed", string(res.Message))
 t.FailNow()
 }
}

**Following is what you need for this book:**
The book benefits business leaders as it provides a comprehensive view on blockchain business models, governance structure, and business design considerations of blockchain solutions. Technology leaders stand to gain a lot from the detailed discussion around the technology landscape, technology design, and architecture considerations in the book. With model-driven application development, this guide will speed up understanding and concept development for blockchain application developers. The simple and well organized content will put novices at ease with blockchain concepts and constructs.

With the following software and hardware list you can run all code files present in the book (Chapter 1-12).

### Software and Hardware List

| Chapter  | Software required                   | OS required                        |
| -------- | ------------------------------------| -----------------------------------|
| 1        | git                    | Windows, Mac OS X, and Linux (Any) |
| 2        | gpg          | Windows, Mac OS X, and Linux (Any) |
| 3        | travis-ci            | Windows, Mac OS X, and Linux (Any) |
| 4        | Hyperledger Fabric & Composer           | Windows, Mac OS X, and Linux (Any) |




### Related products <Paste books from the Other books you may enjoy section>
* Building Blockchain Projects [[Packt]](https://www.packtpub.com/big-data-and-business-intelligence/building-blockchain-projects?utm_source=github&utm_medium=repository&utm_campaign=9781787122147) [[Amazon]](https://www.amazon.com/dp/178712214X)

* Mastering Blockchain - Second Edition [[Packt]](https://www.packtpub.com/big-data-and-business-intelligence/mastering-blockchain-second-edition?utm_source=github&utm_medium=repository&utm_campaign=9781788839044) [[Amazon]](https://www.amazon.com/dp/1788839048)

## Get to Know the Authors
**Nitin Gaur**

Nitin Gaur, as the director of IBM's Blockchain Labs, is responsible for instituting a body of knowledge and organizational understanding around blockchain technology and industry-specific applications. Tenacious and customer focused, he is known for his ability to analyze opportunities and create technologies that align with operational needs, catapult profitability, and dramatically improve customer experience. He is also an IBM Distinguished Engineer. 

**Luc Desrosiers**

Luc Desrosiers is an IBM-certified IT architect with 20+ years of experience. Throughout his career, he has taken on different roles: developer, consultant, and pre-sales architect. He recently moved from Canada to the UK to work in a great lab: IBM Hursley. This is where he had the opportunity to join the IBM Blockchain team. He is now working with clients across multiple industries to help them explore how blockchain technologies can enable transformative uses and solutions.


**Venkatraman Ramakrishnar**

Venkatraman Ramakrishna is an IBM researcher with 10 years of experience. Following a BTech from IIT Kharagpur and PhD from UCLA, he worked in the Bing infrastructure team in Microsoft, building reliable application deployment software. At IBM Research, he worked in mobile computing and security before joining the Blockchain team. He has developed applications for trade and regulation, and is now working on improving the performance and privacy-preserving characteristics of the Hyperledger platform.


**Petr Novotny**

Petr Novotny is a research scientist at IBM Research, with 15+ years of experience in engineering and research of software systems. He received an MSc from University College London and PhD from Imperial College London, where he was also a post-doctoral research associate. He was a visiting scientist at the U.S. Army Research Lab. At IBM, he works on innovations of blockchain technologies and leads the development of blockchain solutions and analytical tools.


**Dr. Salman A. Baset**

Dr. Salman A. Baset is the CTO of security in IBM Blockchain Solutions. He oversees the security and compliance of blockchain solutions being built by IBM in collaboration with partners such as Walmart and Maersk, and interfaces with clients on blockchain solutions and their security. He drives the implementation of the General Data Protection Regulation for blockchain-based solutions. He has also built the identity management system, used by Fortune 500 companies involved in global trade digitization, and IBM Food Trust blockchain solutions.


**Anthony O'Dowd**

Anthony O'Dowd works in IBM's Blockchain team. He is based in Europe as part of a worldwide team that helps users build solutions that benefit from blockchain tech. Anthony has a background in middle and back office systems, and has led the development of key IBM middleware in enterprise messaging and integration. He likes to work in different industries to understand how they can exploit middleware to build more efficient, integrated business systems.


### Suggestions and Feedback
[Click here](https://docs.google.com/forms/d/e/1FAIpQLSdy7dATC6QmEL81FIUuymZ0Wy9vH1jHkvpY57OiMeKGqib_Ow/viewform) if you have any feedback or suggestions.
 

# Trade Application
This is a use case on trade finance and logistics, designed to demonstrate the capabilities of Hyperledger (mainly Fabric) blockchain tools.

# Use Case Scenario Overview
The trade scenario consists of 6 participants:
- *Exporter*: An entity that is selling goods
- *Importer*: An entity that is buying goods from an exporter in exchange for money
- *Importer's Bank*: Maintains a bank account for an importer, and issues a Letter of Credit on its behalf
- *Exporter's Bank*: Maintains a bank account for an exporter, and handles L/Cs and payments on its behalf
- *Carrier*: Entity that ships goods from exporter's to importer's location.
- *Regulatory Auhority*: Public or governmental body that approves the export of goods, and audits the process

The flow diagam below illustrates the steps from a trade agreement to the final payment settlement.
(For more details, see the [full description](docs/Use-Case-Description.docx).

![alt text](docs/Flow-Diagram.png)

# Application folder structure
```
./
├── chaincode
├── middleware
└── application
└── composer
└── network
└── docs
└── README.md
```
The [chaincode](chaincode) folder contains the source code for all versions of the chaincode.

The [middleware](middleware) folder contains wrapper functions that use the Fabric SDK library to implement channel and chaincode operations.

The [application](application) folder contains code to start a web server and offer a REST API for users to register, login,
set up the channel and application, and run trade operations.

The [network](network) folder contains configurations and code to launch a single-machine Docker network setup corresponding to a minimal
version of the trade application scenario.

The [docs](docs) folder contains more documentation on the use case.

# Testing and Running the Application
To test and run the complete application, you will need to perform the following steps in sequence:
- **Test the chaincode (smart contract)**: Navigate to the [chaincode](chaincode) folder for instructions.
- **Launch a trade network**: Navigate to the [network](network) folder for instructions.
- **Prepare the middleware**: Navigate to the [middleware](middleware) folder for instructions.
- **Start and exercise the application server**: Navigate to the [application](application) folder for instructions.

# Augmenting the Application
Two kinds of augmentation are currently supported:
## Add a New Organization and Peers
- See instructions in [network](network) to create configuration files for the new organization and peers.
- See instructions in [middleware](middleware) to update the running application to incorporate the new organization and peers.
  * Alternatively, see instructions in [application](application) to upgrade chaincode through the application server.
## Upgrade Chaincode
- (*Note*: the upgrade version of the chaincode in this repository assumes that the new organization has already been added above.
  * To test chaincode upgrade without new organizations, modify and test the upgrade version of the chaincode suitably.)
- See instructions in [chaincode](chaincode) to validate the upgrade version, or apply custom modifications followed by unit testing.
- See instructions in [middleware](middleware) to upgrade chaincode in a running trade application.
  * Alternatively, see instructions in [application](application) to upgrade chaincode through the application server.
  
  
  
  ## Errata
  
 In the diagram on page 74 (PDF)/98 (Book) (in Chapter 3), the directionality of arrows marked 1 and 2 should be reversed:
 ![alt text](https://github.com/PacktPublishing/Handson-Blockchain-Development-with-Hyperledger/blob/master/B10152_03_1.png?raw=true)
