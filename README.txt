Session 1 :

During this session, the main objective is to create the home page of a pizza store application. This app will have various features such as enabling customers to order pizzas, customize them according to their preferences, and keep track of the delivery status.

The current implementation of the home page component is a simple one, consisting of a single component that displays basic information. The next step is to add a list of available pizza specials. To do this, a @code block with a list field is included in the Index.razor page. Additionally, an HttpClient is injected into the Index component using the @inject directive to retrieve the list of pizza specials.

After retrieving the list of pizza specials, a markup is added to the Index component to display the pizza specials list. To define the layout of the pizza store app, the MainLayout component is defined in Shared/MainLayout.razor, which inherits from LayoutComponentBase. Furthermore, the MainLayout component is updated to define a top bar that includes a branding logo and a navigation link for the home page.

![](RackMultipart20230331-1-1zh05n_html_6ba65317ebf977da.png)

Session 2 :

In this session, the primary focus is on adding new functionality to the pizza ordering feature that enables users to customize their pizza orders. To achieve this, we start by adding an event handler that listens for clicks on pizza specials and displays a pizza customization dialog. Additionally, we add some extra fields to the @code block to keep track of the pizza being customized and whether the customization dialog is visible.

Next, we create a new component called ConfigurePizzaDialog.razor that enables users to specify the size and toppings of their pizza. We include a slider in the dialog to allow users to adjust the pizza size, and use data binding to update the pizza size stored in the configuringPizza object whenever the slider is moved.

To complete the customization process, we add buttons to the dialog that allow users to either cancel or add the pizza to their order. The cancel button enables users to exit the dialog and return to the main page without adding the pizza to their order. On the other hand, the add button adds the pizza to their order, and returns the user to the main page.

Finally, we update the Pages/Index.razor file to display the ConfigurePizzaDialog whenever a pizza special is selected. When a user clicks on a pizza special, the ConfigurePizzaDialog is shown, enabling the user to customize their pizza. We also implement functionality to close the dialog when the user clicks the cancel button, enabling them to return to the main page without adding the pizza to their order.

Session 3 and 4 :

For session 3, we had to work on updating orders. That is why we created an Orders component to manage orders and orders status. The page "My Orders" displays the recap of all the client's orders. We also added a button to track the order.

In session 4, we solved a problem. To do that, we used the AppState pattern which can outlive components and hold on to state even with changing UI. The AppState pattern solves state management issues in Blazor by storing shared state in a separate AppState instead of individual components. Components call AppState methods to update the state, and EventCallback handles notifying relevant components of the changes. This prevents loss of state when users move between pages.

Session 5:

In the session 5 we created a checkout page to a pizza ordering app in Blazor. We had to create a new page component for the checkout, to capture the delivery address with a reusable AddressEditor component, and to add server-side and client-side validation to check entered address' validity before an order can be submitted.

Session 6:

We added a register/login page.

Session 7:

We integrated a real-time map to the pizza delivery order status page, allowing users to track their pizza delivery. To display the map with specific markers, we utilized the Map component, which generates a div with a unique ID and invokes the deliveryMap.showOrUpdate function.

Additionally, we implemented a confirmation prompt to ensure that users genuinely want to remove a pizza from their order whenever they click on the Remove button. To achieve this, we included a RemovePizza function that calls the Confirm method to prompt users before deleting a pizza from their order.

Session 8:

We made components more reusable.

Session 9:

We incorporated Progressive Web App (PWA) functionalities to a Blazor web application. These functionalities comprise installing the application into the OS taskbar or home screen, allowing the app to function offline, and receiving push notifications. To make these features possible, we needed to implement a service worker, which is a small file that includes event handlers that the browser can trigger outside of the application's context.