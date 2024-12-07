+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 6e12510bc1ec409e8e25aada24cd1e94 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: Caccam, Jesus Allyson O.   | DATE PERFORMED:        | /50      |
|                                  | October 10, 2024       |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | October 10, 2024       |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Setting Up Webserver

# Requirement: 

-   A virtual machine running Linux and Windows OS

    Task Instructions:

1.  Install IIS by adding it as a role, select necessary features,
    include monitoring tools

    ![](vertopal_6e12510bc1ec409e8e25aada24cd1e94/media/image2.png){width="6.753314741907261in"
    height="4.739133858267716in"}

2.  Create a website by opening IIS Manager

    -   Right-click on the server's name and select Internet Information
        Services Manager.

    -   Right-click on Sites and select Add Website.

    -   Enter a name, description, physical path (where your website
        files will reside), IP address, port, and host name.

        ![](vertopal_6e12510bc1ec409e8e25aada24cd1e94/media/image3.png){width="6.24045384951881in"
        height="6.011255468066492in"}

3.  Configure the Website:

    -   Right-click on your website and select Edit.

    -   Set the Default Document to the name of your main HTML file
        \>default.html

    -   Configure other settings as needed (e.g., SSL certificates,
        authentication)

4.  Create a Web Page:

    -   Create an HTML file in the physical path you specified.

        ![](vertopal_6e12510bc1ec409e8e25aada24cd1e94/media/image4.png){width="3.652083333333333in"
        height="1.52377624671916in"}

    -   Save it as default.html or your preferred name.

        ![](vertopal_6e12510bc1ec409e8e25aada24cd1e94/media/image5.png){width="6.250872703412074in"
        height="1.2085017497812773in"}

5.  Test the Web Server:

    -   Open a web browser and enter the URL of your website (e.g.,
        http://localhost).

    -   You should see your web page displayed.

![](vertopal_6e12510bc1ec409e8e25aada24cd1e94/media/image6.png){width="3.0525142169728783in"
height="2.3961712598425198in"}![](vertopal_6e12510bc1ec409e8e25aada24cd1e94/media/image7.png){width="3.9484667541557306in"
height="2.5107666229221346in"}

Grading Rubric

  ------------------------------------------------------------------------------
  **Criteria**      **Points**   **Description**
  ----------------- ------------ -----------------------------------------------
  Web Server        15           Correctly installs IIS or another web server on
  Installation                   the virtual machine.

  Website           15           Successfully configures the website with the
  Configuration                  correct physical path, IP address, port, and
                                 default document.

  Successful Access 15           Successfully accesses the web page from the
                                 client computer using the correct URL.

  Troubleshooting   15           Demonstrates ability to troubleshoot common
                                 issues, such as network connectivity problems
                                 or configuration errors.

  Documentation     10           Provides clear and concise documentation of the
                                 installation, configuration, and testing
                                 process.

  Total             /70          
  ------------------------------------------------------------------------------
