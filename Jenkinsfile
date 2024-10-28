pipeline {
    agent any
    
    environment {
        SNOWFLAKE_USER = credentials('WALE2688')
        SNOWFLAKE_PASSWORD = credentials('Derindura2577@')
        SNOWFLAKE_ACCOUNT = 'wxemsbb-fb26581'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/your-repo-path.git'
            }
        }

        stage('Deploy to Snowflake') {
            steps {
                script {
                    sh """
                    snowsql -a $SNOWFLAKE_ACCOUNT -u $SNOWFLAKE_USER -p $SNOWFLAKE_PASSWORD                     -d your_database -s your_schema -f sql/tables/create_customers_table.sql
                    
                    snowsql -a $SNOWFLAKE_ACCOUNT -u $SNOWFLAKE_USER -p $SNOWFLAKE_PASSWORD                     -d your_database -s your_schema -f sql/inserts/insert_single_record.sql
                    
                    snowsql -a $SNOWFLAKE_ACCOUNT -u $SNOWFLAKE_USER -p $SNOWFLAKE_PASSWORD                     -d your_database -s your_schema -f sql/inserts/insert_multiple_records.sql
                    """
                }
            }
        }
    }
}
