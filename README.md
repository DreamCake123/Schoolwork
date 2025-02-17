*Authored by Cake*
Jakarta EE boilerplate made to hosted by Glassfish, for module ITP4511

# How to Run the Jakarta Application with GlassFish

1. **Download and Install GlassFish:**

2. **Build the Application:**
   - Navigate to the project directory:
     ```
     sh
     cd my-jakarta-app
     ```
   - Build the project using Maven:
     ```
     sh
     mvn clean package
     ```

3. **Start the GlassFish server and deploy the App to GlassFish:**
   - Start the GlassFish server:
     ```
     sh
     glassfish4/bin/asadmin start-domain
     ```
   - Deploy the application:
     ```
     sh
     glassfish4/bin/asadmin deploy ./target/my-jakarta-app-1.0-SNAPSHOT.war
     ```

4. **Access the Application:**
   - Open a web browser and navigate to:
     ```
     http://localhost:8080/my-jakarta-app-1.0-SNAPSHOT/myServlet
     ```
   - When hosted from Codespace: 
     ```
     http://container-url-here.github.dev:8080/my-jakarta-app-1.0-SNAPSHOT/myServlet
     ```
  
5. **Stop the GlassFish Server:**
   - To stop the server, run:
     ```
     sh
     glassfish4/bin/asadmin stop-domain
     ```

# Note

Installed is Glassfish 6 and Jakarta EE 9. 
This project is made specifically with these, 
other versions are not tested and may not work.