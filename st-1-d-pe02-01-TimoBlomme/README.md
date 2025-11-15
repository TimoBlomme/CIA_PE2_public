# Coin Chop

> "Split bills with friends"

This example application serves as a basis for a deeper understanding in the Continuous Integration cycle and Unit Testing methodology.

The architectural model consists of three main layers, bound to three projects;


- ### Howest.Prog.CoinChop.**Core**

    Contains Domain objects and logic. It has no dependencies on any other frameworks or infrastructure. Uses interfaces to communicate with the other layers.

- ### Howest.Prog.CoinChop.**Infrastructure**

    Implements specific interfaces which map to the Core layer. Uses Entity Framework for persistence and SmtpClient for mailing.

    This project depends on the Core project.

- ### Howest.Prog.CoinChop.**Web**

    Interfaces with the user by using the Model-View-Controller pattern in ASP.NET Core. The Controllers call the application logic in the Core layer and present the results to the user.

    This project depends on the Core and Infrastructure projects to tie all dependencies together using Inversion of Control.


For more information, please consult the `/docs` folder.