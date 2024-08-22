**Project Description:**
The Makersharks Search API is a Node.js-based RESTful API designed to help users search for manufacturers on the Makersharks platform based on specific criteria such as location, nature of business, and manufacturing process. This proof of concept (POC) allows buyers to find manufacturers that meet their customized requirements, facilitating the connection between buyers and suppliers. 
The API supports filtering by various parameters and includes pagination to handle large result sets efficiently. It’s built with scalability in mind, ensuring that as the database of suppliers grows, users can still quickly and easily find the manufacturers they need.

**Setup Instructions:**
git clone https://github.com/swetamaurya/makersharks-search-api.git
cd makersharks-search-api
npm install
nodemon 

**API Documentation:**
**Describe the endpoint:**
This endpoint allows users to query the Makersharks database for manufacturers that meet specific criteria, such as their location, nature of business, and the manufacturing processes they offer.

**Method:**
POST

**Request Body Parameters:**
location (string, required): The city or location where the manufacturer is based.
nature_of_business (string, required): The scale of the business. Possible values include:
small_scale
medium_scale
large_scale
manufacturing_process (string, required): The type of manufacturing process the supplier is capable of. Possible values include:
moulding
3d_printing
casting
coating
limit (integer, optional): The maximum number of results to return per page. Defaults to a specified value if not provided.
page (integer, optional): The page number to retrieve, useful for pagination. Defaults to the first page if not provided.

**Response:**
A JSON array of objects, each representing a manufacturer that matches the query criteria. Each object contains the following fields:
supplier_id (string): The unique identifier for the supplier.
company_name (string): The name of the supplier's company.
website (string): The URL of the supplier's website.
location (string): The city where the supplier is located.
nature_of_business (string): The scale of the supplier's business.
manufacturing_processes (array of strings): The manufacturing processes that the supplier is capable of.
