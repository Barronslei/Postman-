# Postman&Docker Compose files for the full Protocol stack

from flask import Flask 

app=Flask(__name__)

#初始化路由

@app.route('/chain', methods=['GET'])
def full_chain():
    return 'we will get new chain'

@app.route('/transactions/new', methods=['POST'])
def new_transaction():
    return "We'll add a new transaction"
 
#初始化运行入口

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)
