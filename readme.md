## Assignment Task

# 1. Register User
This API allows users to register for a loan by providing basic personal information. Upon registration, it triggers an asynchronous Celery task to calculate the user's credit score. The credit score is determined based on a provided CSV file containing transactions for multiple users.

# 2. Apply Loan
This API is designed to handle loan applications against a user's credit card. It initiates the loan process if the application meets certain criteria and generates a repayment schedule with monthly EMIs. Additionally, the API calculates the monthly EMI, daily interest, and minimum due. Detailed calculations

# 3. Make Payment
This API facilitates users in repaying their EMIs. It ensures that users at least pay the Minimum Due amount of the EMI and adjusts any overpayments or underpayments in subsequent EMIs, ensuring the complete loan amount is paid off before the due date.

# 4. Get Statement
 API which would only print all the transactions done and also all the future EMIs.


# 5. Billing Process
A Cron job implemented with celery would do the billing of the users whose billing date is the current date. It would also create a table of Billing details and due payments.



## Set Up Process
   # Clone the Repository
   # Create a Virtual environment
   # Enter the directory
      cd credit_card_service
   # Start the Server
      python manage.py runserver
   # Start Celery Worker
       python -m celery -A credit_card_service worker -l info
   # Start Celery Beat
      python -m celery -A credit_card_service beat -l info

   # Project Access
      http://localhost:8000/


  ##  Screenshots

      ![Screenshot (789)](https://github.com/Yashg5311/CreditService/assets/91370994/3c6fc134-1326-4777-84d7-b6bc936b7616)
![Screenshot (790)](https://github.com/Yashg5311/CreditService/assets/91370994/4da33329-2997-4756-89b8-f40e7e60a645)
![Screenshot (791)](https://github.com/Yashg5311/CreditService/assets/91370994/5929a319-43eb-4a87-b450-179ae5803893)

![Screenshot (792)](https://github.com/Yashg5311/CreditService/assets/91370994/8bc97119-f229-49cd-a7a2-fab8cf5e59d3)
