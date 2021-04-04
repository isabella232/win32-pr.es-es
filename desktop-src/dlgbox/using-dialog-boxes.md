---
title: Usar cuadros de diálogo
description: Los cuadros de diálogo se usan para mostrar información y solicitar la intervención del usuario.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Interfaz de usuario de Windows, ventanas
- Interfaz de usuario de Windows, cuadros de diálogo
- ventanas, cuadros de diálogo
- cuadros de diálogo, acerca de
- cuadros de diálogo, Mostrar
- cuadros de diálogo modales
- cuadros de diálogo no modales
- cuadros de diálogo, modales
- cuadros de diálogo, no modales
- cuadros de diálogo, inicializar
- plantillas de cuadro de diálogo
- cuadros de diálogo, plantillas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21da47d7d59f4cadc21314566bce41a9ef3456a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078181"
---
# <a name="using-dialog-boxes"></a><span data-ttu-id="c7b42-115">Usar cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="c7b42-115">Using Dialog Boxes</span></span>

<span data-ttu-id="c7b42-116">Los cuadros de diálogo se usan para mostrar información y solicitar la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="c7b42-116">You use dialog boxes to display information and prompt for input from the user.</span></span> <span data-ttu-id="c7b42-117">La aplicación carga e inicializa el cuadro de diálogo, procesa los datos proporcionados por el usuario y destruye el cuadro de diálogo cuando el usuario finaliza la tarea.</span><span class="sxs-lookup"><span data-stu-id="c7b42-117">Your application loads and initializes the dialog box, processes user input, and destroys the dialog box when the user finishes the task.</span></span> <span data-ttu-id="c7b42-118">El proceso de control de cuadros de diálogo varía en función de si el cuadro de diálogo es modal o no modal.</span><span class="sxs-lookup"><span data-stu-id="c7b42-118">The process for handling dialog boxes varies, depending on whether the dialog box is modal or modeless.</span></span> <span data-ttu-id="c7b42-119">Un cuadro de diálogo modal requiere que el usuario cierre el cuadro de diálogo antes de activar otra ventana en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c7b42-119">A modal dialog box requires the user to close the dialog box before activating another window in the application.</span></span> <span data-ttu-id="c7b42-120">Sin embargo, el usuario puede activar Windows en aplicaciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="c7b42-120">However, the user can activate windows in different applications.</span></span> <span data-ttu-id="c7b42-121">Un cuadro de diálogo no modal no requiere una respuesta inmediata del usuario.</span><span class="sxs-lookup"><span data-stu-id="c7b42-121">A modeless dialog box does not require an immediate response from the user.</span></span> <span data-ttu-id="c7b42-122">Es similar a una ventana principal que contiene controles.</span><span class="sxs-lookup"><span data-stu-id="c7b42-122">It is similar to a main window containing controls.</span></span>

<span data-ttu-id="c7b42-123">En las secciones siguientes se explica cómo usar ambos tipos de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-123">The following sections discuss how to use both types of dialog boxes.</span></span>

-   [<span data-ttu-id="c7b42-124">Mostrar un cuadro de mensaje</span><span class="sxs-lookup"><span data-stu-id="c7b42-124">Displaying a Message Box</span></span>](#displaying-a-message-box)
-   [<span data-ttu-id="c7b42-125">Crear un cuadro de diálogo modal</span><span class="sxs-lookup"><span data-stu-id="c7b42-125">Creating a Modal Dialog Box</span></span>](#creating-a-modal-dialog-box)
-   [<span data-ttu-id="c7b42-126">Crear un cuadro de diálogo no modal</span><span class="sxs-lookup"><span data-stu-id="c7b42-126">Creating a Modeless Dialog Box</span></span>](#creating-a-modeless-dialog-box)
-   [<span data-ttu-id="c7b42-127">Inicializar un cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="c7b42-127">Initializing a Dialog Box</span></span>](#initializing-a-dialog-box)
-   [<span data-ttu-id="c7b42-128">Crear una plantilla en memoria</span><span class="sxs-lookup"><span data-stu-id="c7b42-128">Creating a Template in Memory</span></span>](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a><span data-ttu-id="c7b42-129">Mostrar un cuadro de mensaje</span><span class="sxs-lookup"><span data-stu-id="c7b42-129">Displaying a Message Box</span></span>

<span data-ttu-id="c7b42-130">La forma más sencilla de cuadro de diálogo modal es el cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c7b42-130">The simplest form of modal dialog box is the message box.</span></span> <span data-ttu-id="c7b42-131">La mayoría de las aplicaciones usan cuadros de mensaje para advertir al usuario de los errores y para solicitar instrucciones sobre cómo continuar después de que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="c7b42-131">Most applications use message boxes to warn the user of errors and to prompt for directions on how to proceed after an error has occurred.</span></span> <span data-ttu-id="c7b42-132">Cree un cuadro de mensaje mediante la función [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) o [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) , especificando el mensaje y el número y tipo de botones que se van a mostrar.</span><span class="sxs-lookup"><span data-stu-id="c7b42-132">You create a message box by using the [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) or [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) function, specifying the message and the number and type of buttons to display.</span></span> <span data-ttu-id="c7b42-133">El sistema crea un cuadro de diálogo modal, que proporciona su propio procedimiento y plantilla de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-133">The system creates a modal dialog box, providing its own dialog box template and procedure.</span></span> <span data-ttu-id="c7b42-134">Una vez que el usuario cierra el cuadro de mensaje, **MessageBox** o **MessageBoxEx** devuelve un valor que identifica el botón elegido por el usuario para cerrar el cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c7b42-134">After the user closes the message box, **MessageBox** or **MessageBoxEx** returns a value identifying the button chosen by the user to close the message box.</span></span>

<span data-ttu-id="c7b42-135">En el ejemplo siguiente, la aplicación muestra un cuadro de mensaje que solicita al usuario una acción una vez que se ha producido una condición de error.</span><span class="sxs-lookup"><span data-stu-id="c7b42-135">In the following example, the application displays a message box that prompts the user for an action after an error condition has occurred.</span></span> <span data-ttu-id="c7b42-136">En el cuadro de mensaje se muestra el mensaje que describe la condición de error y cómo resolverlo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-136">The message box displays the message that describes the error condition and how to resolve it.</span></span> <span data-ttu-id="c7b42-137">El estilo **MB \_ síno** dirige [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) para proporcionar dos botones con los que el usuario puede elegir cómo proceder:</span><span class="sxs-lookup"><span data-stu-id="c7b42-137">The **MB\_YESNO** style directs [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) to provide two buttons with which the user can choose how to proceed:</span></span>


```
int DisplayConfirmSaveAsMessageBox()
{
    int msgboxID = MessageBox(
        NULL,
        L"temp.txt already exists.\nDo you want to replace it?",
        L"Confirm Save As",
        MB_ICONEXCLAMATION | MB_YESNO
    );

    if (msgboxID == IDYES)
    {
        // TODO: add code
    }

    return msgboxID;    
}
```



<span data-ttu-id="c7b42-138">En la imagen siguiente se muestra el resultado del ejemplo de código anterior:</span><span class="sxs-lookup"><span data-stu-id="c7b42-138">The following image shows the output from the preceding code example:</span></span>

![cuadro de mensaje](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a><span data-ttu-id="c7b42-140">Crear un cuadro de diálogo modal</span><span class="sxs-lookup"><span data-stu-id="c7b42-140">Creating a Modal Dialog Box</span></span>

<span data-ttu-id="c7b42-141">Puede crear un cuadro de diálogo modal mediante la función [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) .</span><span class="sxs-lookup"><span data-stu-id="c7b42-141">You create a modal dialog box by using the [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) function.</span></span> <span data-ttu-id="c7b42-142">Debe especificar el identificador o el nombre de un recurso de plantilla de cuadro de diálogo y un puntero al procedimiento de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-142">You must specify the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="c7b42-143">La función **DialogBox** carga la plantilla, muestra el cuadro de diálogo y procesa todos los datos proporcionados por el usuario hasta que el usuario cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-143">The **DialogBox** function loads the template, displays the dialog box, and processes all user input until the user closes the dialog box.</span></span>

<span data-ttu-id="c7b42-144">En el ejemplo siguiente, la aplicación muestra un cuadro de diálogo modal cuando el usuario hace clic en **Eliminar elemento** en un menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c7b42-144">In the following example, the application displays a modal dialog box when the user clicks **Delete Item** from an application menu.</span></span> <span data-ttu-id="c7b42-145">El cuadro de diálogo contiene un control de edición (en el que el usuario escribe el nombre de un elemento) y los botones **Aceptar** y **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="c7b42-145">The dialog box contains an edit control (in which the user enters the name of an item) and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="c7b42-146">Los identificadores de control de estos controles son ID. \_ ITEMNAME, IDOK y IDCANCEL, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c7b42-146">The control identifiers for these controls are ID\_ITEMNAME, IDOK, and IDCANCEL, respectively.</span></span>

<span data-ttu-id="c7b42-147">La primera parte del ejemplo consta de las instrucciones que crean el cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="c7b42-147">The first part of the example consists of the statements that create the modal dialog box.</span></span> <span data-ttu-id="c7b42-148">Estas instrucciones, en el procedimiento de ventana de la ventana principal de la aplicación, crean el cuadro de diálogo cuando el sistema recibe un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) con el \_ identificador de menú DELETEITEM de IDM.</span><span class="sxs-lookup"><span data-stu-id="c7b42-148">These statements, in the window procedure for the application's main window, create the dialog box when the system receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_DELETEITEM menu identifier.</span></span> <span data-ttu-id="c7b42-149">La segunda parte del ejemplo es el procedimiento de cuadro de diálogo, que recupera el contenido del control de edición y cierra el cuadro de diálogo tras recibir un mensaje de **\_ comando de WM** .</span><span class="sxs-lookup"><span data-stu-id="c7b42-149">The second part of the example is the dialog box procedure, which retrieves the contents of the edit control and closes the dialog box upon receiving a **WM\_COMMAND** message.</span></span>

<span data-ttu-id="c7b42-150">Las instrucciones siguientes crean el cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="c7b42-150">The following statements create the modal dialog box.</span></span> <span data-ttu-id="c7b42-151">La plantilla de cuadro de diálogo es un recurso del archivo ejecutable de la aplicación y tiene el identificador de recursos DLG \_ DELETEITEM.</span><span class="sxs-lookup"><span data-stu-id="c7b42-151">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_DELETEITEM.</span></span>


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_DELETEITEM: 
            if (DialogBox(hinst, 
                          MAKEINTRESOURCE(DLG_DELETEITEM), 
                          hwnd, 
                          (DLGPROC)DeleteItemProc)==IDOK) 
            {
                // Complete the command; szItemName contains the 
                // name of the item to delete. 
            }

            else 
            {
                // Cancel the command. 
            } 
            break; 
    } 
    return 0L; 
```



<span data-ttu-id="c7b42-152">En este ejemplo, la aplicación especifica su ventana principal como ventana propietaria para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-152">In this example, the application specifies its main window as the owner window for the dialog box.</span></span> <span data-ttu-id="c7b42-153">Cuando el sistema muestra inicialmente el cuadro de diálogo, su posición es relativa a la esquina superior izquierda del área de cliente de la ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="c7b42-153">When the system initially displays the dialog box, its position is relative to the upper left corner of the owner window's client area.</span></span> <span data-ttu-id="c7b42-154">La aplicación utiliza el valor devuelto de [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) para determinar si se debe continuar con la operación o cancelarla.</span><span class="sxs-lookup"><span data-stu-id="c7b42-154">The application uses the return value from [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) to determine whether to proceed with the operation or cancel it.</span></span> <span data-ttu-id="c7b42-155">Las instrucciones siguientes definen el procedimiento de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-155">The following statements define the dialog box procedure.</span></span>


```
char szItemName[80]; // receives name of item to delete. 
 
BOOL CALLBACK DeleteItemProc(HWND hwndDlg, 
                             UINT message, 
                             WPARAM wParam, 
                             LPARAM lParam) 
{ 
    switch (message) 
    { 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    if (!GetDlgItemText(hwndDlg, ID_ITEMNAME, szItemName, 80)) 
                         *szItemName=0; 
 
                    // Fall through. 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, wParam); 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



<span data-ttu-id="c7b42-156">En este ejemplo, el procedimiento usa [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) para recuperar el texto actual del control de edición identificado por el identificador \_ ITEMNAME.</span><span class="sxs-lookup"><span data-stu-id="c7b42-156">In this example, the procedure uses [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) to retrieve the current text from the edit control identified by ID\_ITEMNAME.</span></span> <span data-ttu-id="c7b42-157">A continuación, el procedimiento llama a la función [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) para establecer el valor devuelto del cuadro de diálogo en IDOK o IDCANCEL, dependiendo del mensaje recibido, y para comenzar el proceso de cerrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-157">The procedure then calls the [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) function to set the dialog box's return value to either IDOK or IDCANCEL, depending on the message received, and to begin the process of closing the dialog box.</span></span> <span data-ttu-id="c7b42-158">Los identificadores IDOK y IDCANCEL se corresponden con los botones **Aceptar** y **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="c7b42-158">The IDOK and IDCANCEL identifiers correspond to the **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="c7b42-159">Una vez que el procedimiento llama a **EndDialog**, el sistema envía mensajes adicionales al procedimiento para destruir el cuadro de diálogo y devuelve el valor devuelto del cuadro de diálogo a la función que creó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-159">After the procedure calls **EndDialog**, the system sends additional messages to the procedure to destroy the dialog box and returns the dialog box's return value back to the function that created the dialog box.</span></span>

## <a name="creating-a-modeless-dialog-box"></a><span data-ttu-id="c7b42-160">Crear un cuadro de diálogo no modal</span><span class="sxs-lookup"><span data-stu-id="c7b42-160">Creating a Modeless Dialog Box</span></span>

<span data-ttu-id="c7b42-161">Puede crear un cuadro de diálogo no modal mediante la función [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) , especificando el identificador o el nombre de un recurso de plantilla de cuadro de diálogo y un puntero al procedimiento del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-161">You create a modeless dialog box by using the [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) function, specifying the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="c7b42-162">**CreateDialog** carga la plantilla, crea el cuadro de diálogo y, opcionalmente, la muestra.</span><span class="sxs-lookup"><span data-stu-id="c7b42-162">**CreateDialog** loads the template, creates the dialog box, and optionally displays it.</span></span> <span data-ttu-id="c7b42-163">La aplicación es responsable de recuperar y enviar mensajes de entrada del usuario al procedimiento del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-163">Your application is responsible for retrieving and dispatching user input messages to the dialog box procedure.</span></span>

<span data-ttu-id="c7b42-164">En el ejemplo siguiente, la aplicación muestra un cuadro de diálogo no modal (si aún no se muestra) cuando el usuario hace clic en **ir a** desde un menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c7b42-164">In the following example, the application displays a modeless dialog box — if it is not already displayed — when the user clicks **Go To** from an application menu.</span></span> <span data-ttu-id="c7b42-165">El cuadro de diálogo contiene un control de edición, una casilla y botones **Aceptar** y **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="c7b42-165">The dialog box contains an edit control, a check box, and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="c7b42-166">La plantilla de cuadro de diálogo es un recurso del archivo ejecutable de la aplicación y tiene el identificador de recurso DLG \_ goto.</span><span class="sxs-lookup"><span data-stu-id="c7b42-166">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_GOTO.</span></span> <span data-ttu-id="c7b42-167">El usuario escribe un número de línea en el control de edición y activa la casilla para especificar que el número de línea es relativo a la línea actual.</span><span class="sxs-lookup"><span data-stu-id="c7b42-167">The user enters a line number in the edit control and checks the check box to specify that the line number is relative to the current line.</span></span> <span data-ttu-id="c7b42-168">Los identificadores de control son \_ línea ID, ID \_ ABSREL, IDOK y IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="c7b42-168">The control identifiers are ID\_LINE, ID\_ABSREL, IDOK, and IDCANCEL.</span></span>

<span data-ttu-id="c7b42-169">Las instrucciones de la primera parte del ejemplo crean el cuadro de diálogo no modal.</span><span class="sxs-lookup"><span data-stu-id="c7b42-169">The statements in the first part of the example create the modeless dialog box.</span></span> <span data-ttu-id="c7b42-170">Estas instrucciones, en el procedimiento de ventana de la ventana principal de la aplicación, crean el cuadro de diálogo cuando el procedimiento de ventana recibe un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) que tiene el \_ identificador de menú ir Goto, pero solo si la variable global no contiene ya un identificador válido.</span><span class="sxs-lookup"><span data-stu-id="c7b42-170">These statements, in the window procedure for the application's main window, create the dialog box when the window procedure receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_GOTO menu identifier, but only if the global variable does not already contain a valid handle.</span></span> <span data-ttu-id="c7b42-171">La segunda parte del ejemplo es el bucle de mensajes principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c7b42-171">The second part of the example is the application's main message loop.</span></span> <span data-ttu-id="c7b42-172">El bucle incluye la función [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) para asegurarse de que el usuario puede usar la interfaz de teclado de cuadro de diálogo de este cuadro de diálogo no modal.</span><span class="sxs-lookup"><span data-stu-id="c7b42-172">The loop includes the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function to ensure that the user can use the dialog box keyboard interface in this modeless dialog box.</span></span> <span data-ttu-id="c7b42-173">La tercera parte del ejemplo es el procedimiento de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-173">The third part of the example is the dialog box procedure.</span></span> <span data-ttu-id="c7b42-174">El procedimiento recupera el contenido del control de edición y la casilla de verificación cuando el usuario hace clic en el botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="c7b42-174">The procedure retrieves the contents of the edit control and check box when the user clicks the **OK** button.</span></span> <span data-ttu-id="c7b42-175">El procedimiento destruye el cuadro de diálogo cuando el usuario hace clic en el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="c7b42-175">The procedure destroys the dialog box when the user clicks the **Cancel** button.</span></span>


```
HWND hwndGoto = NULL;  // Window handle of dialog box 
                
...

case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_GOTO: 
            if (!IsWindow(hwndGoto)) 
            { 
                hwndGoto = CreateDialog(hinst, 
                                        MAKEINTRESOURCE(DLG_GOTO), 
                                        hwnd, 
                                        (DLGPROC)GoToProc); 
                ShowWindow(hwndGoto, SW_SHOW); 
            } 
            break; 
    } 
    return 0L; 
```



<span data-ttu-id="c7b42-176">En las instrucciones anteriores, se llama a [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) solo si no `hwndGoto` contiene un identificador de ventana válido.</span><span class="sxs-lookup"><span data-stu-id="c7b42-176">In the preceding statements, [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) is called only if `hwndGoto` does not contain a valid window handle.</span></span> <span data-ttu-id="c7b42-177">Esto garantiza que la aplicación no muestre dos cuadros de diálogo al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-177">This ensures that the application does not display two dialog boxes at the same time.</span></span> <span data-ttu-id="c7b42-178">Para admitir este método de comprobación, el procedimiento de cuadro de diálogo debe establecer en **null** cuando destruya el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-178">To support this method of checking, the dialog procedure must set to **NULL** when it destroys the dialog box.</span></span>

<span data-ttu-id="c7b42-179">El bucle de mensajes de una aplicación consta de las siguientes instrucciones.</span><span class="sxs-lookup"><span data-stu-id="c7b42-179">The message loop for an application consists of the following statements.</span></span>


```
BOOL bRet;

while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0) 
{ 
    if (bRet == -1)
    {
        // Handle the error and possibly exit
    }
    else if (!IsWindow(hwndGoto) || !IsDialogMessage(hwndGoto, &msg)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
} 
```



<span data-ttu-id="c7b42-180">El bucle comprueba la validez del identificador de ventana para el cuadro de diálogo y solo llama a la función [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) si el identificador es válido.</span><span class="sxs-lookup"><span data-stu-id="c7b42-180">The loop checks the validity of the window handle to the dialog box and only calls the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function if the handle is valid.</span></span> <span data-ttu-id="c7b42-181">**IsDialogMessage** solo procesa el mensaje si pertenece al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-181">**IsDialogMessage** only processes the message if it belongs to the dialog box.</span></span> <span data-ttu-id="c7b42-182">De lo contrario, devuelve **false** y el bucle envía el mensaje a la ventana correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c7b42-182">Otherwise, it returns **FALSE** and the loop dispatches the message to the appropriate window.</span></span>

<span data-ttu-id="c7b42-183">Las instrucciones siguientes definen el procedimiento de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-183">The following statements define the dialog box procedure.</span></span>


```
int iLine;             // Receives line number.
BOOL fRelative;        // Receives check box status. 
 
BOOL CALLBACK GoToProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    BOOL fError; 
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
            CheckDlgButton(hwndDlg, ID_ABSREL, fRelative); 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    fRelative = IsDlgButtonChecked(hwndDlg, ID_ABSREL); 
                    iLine = GetDlgItemInt(hwndDlg, ID_LINE, &fError, fRelative); 
                    if (fError) 
                    { 
                        MessageBox(hwndDlg, SZINVALIDNUMBER, SZGOTOERR, MB_OK); 
                        SendDlgItemMessage(hwndDlg, ID_LINE, EM_SETSEL, 0, -1L); 
                    } 
                    else 

                    // Notify the owner window to carry out the task. 
 
                    return TRUE; 
 
                case IDCANCEL: 
                    DestroyWindow(hwndDlg); 
                    hwndGoto = NULL; 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



<span data-ttu-id="c7b42-184">En las instrucciones anteriores, el procedimiento procesa los mensajes de [**\_ comandos**](/windows/desktop/menurc/wm-command) de [**WM \_ INITDIALOG**](wm-initdialog.md) y WM.</span><span class="sxs-lookup"><span data-stu-id="c7b42-184">In the preceding statements, the procedure processes the [**WM\_INITDIALOG**](wm-initdialog.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="c7b42-185">Durante el procesamiento de **\_ INITDIALOG de WM** , el procedimiento inicializa la casilla pasando el valor actual de la variable global a [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx).</span><span class="sxs-lookup"><span data-stu-id="c7b42-185">During **WM\_INITDIALOG** processing, the procedure initializes the check box by passing the current value of the global variable to [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx).</span></span> <span data-ttu-id="c7b42-186">Después, el procedimiento devuelve **true** para indicar al sistema que establezca el foco de entrada predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c7b42-186">The procedure then returns **TRUE** to direct the system to set the default input focus.</span></span>

<span data-ttu-id="c7b42-187">Durante el procesamiento de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) , el procedimiento cierra el cuadro de diálogo solo si el usuario hace clic en el botón **Cancelar** , es decir, el botón que tiene el identificador IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="c7b42-187">During [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) processing, the procedure closes the dialog box only if the user clicks the **Cancel** button — that is, the button having the IDCANCEL identifier.</span></span> <span data-ttu-id="c7b42-188">El procedimiento debe llamar a [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para cerrar un cuadro de diálogo no modal.</span><span class="sxs-lookup"><span data-stu-id="c7b42-188">The procedure must call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) to close a modeless dialog box.</span></span> <span data-ttu-id="c7b42-189">Observe que en el procedimiento también se establece la variable en **null** para asegurarse de que otras instrucciones que dependen de esta variable funcionan correctamente.</span><span class="sxs-lookup"><span data-stu-id="c7b42-189">Notice that the procedure also sets the variable to **NULL** to ensure that other statements that depend on this variable operate correctly.</span></span>

<span data-ttu-id="c7b42-190">Si el usuario hace clic en el botón **Aceptar** , el procedimiento recupera el estado actual de la casilla y lo asigna a la variable **fRelative** .</span><span class="sxs-lookup"><span data-stu-id="c7b42-190">If the user clicks the **OK** button, the procedure retrieves the current state of the check box and assigns it to the **fRelative** variable.</span></span> <span data-ttu-id="c7b42-191">A continuación, usa la variable para recuperar el número de línea del control de edición.</span><span class="sxs-lookup"><span data-stu-id="c7b42-191">It then uses the variable to retrieve the line number from the edit control.</span></span> <span data-ttu-id="c7b42-192">[**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) traduce el texto del control de edición en un entero.</span><span class="sxs-lookup"><span data-stu-id="c7b42-192">[**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) translates the text in the edit control into an integer.</span></span> <span data-ttu-id="c7b42-193">El valor de **fRelative** determina si la función interpreta el número como un valor con o sin signo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-193">The value of **fRelative** determines whether the function interprets the number as a signed or unsigned value.</span></span> <span data-ttu-id="c7b42-194">Si el texto del control de edición no es un número válido, **GetDlgItemInt** establece el valor de la variable **fError** en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="c7b42-194">If the edit control text is not a valid number, **GetDlgItemInt** sets the value of the **fError** variable to nonzero.</span></span> <span data-ttu-id="c7b42-195">El procedimiento comprueba este valor para determinar si se va a mostrar un mensaje de error o si se lleva a cabo la tarea.</span><span class="sxs-lookup"><span data-stu-id="c7b42-195">The procedure checks this value to determine whether to display an error message or carry out the task.</span></span> <span data-ttu-id="c7b42-196">En caso de error, el procedimiento del cuadro de diálogo envía un mensaje al control de edición y lo dirige a seleccionar el texto del control para que el usuario pueda reemplazarlo fácilmente.</span><span class="sxs-lookup"><span data-stu-id="c7b42-196">In the event of an error, the dialog box procedure sends a message to the edit control, directing it to select the text in the control so that the user can easily replace it.</span></span> <span data-ttu-id="c7b42-197">Si **GetDlgItemInt** no devuelve un error, el procedimiento puede llevar a cabo la propia tarea solicitada o enviar un mensaje a la ventana propietaria y dirigirla para llevar a cabo la operación.</span><span class="sxs-lookup"><span data-stu-id="c7b42-197">If **GetDlgItemInt** does not return an error, the procedure can either carry out the requested task itself or send a message to the owner window, directing it to carry out the operation.</span></span>

## <a name="initializing-a-dialog-box"></a><span data-ttu-id="c7b42-198">Inicializar un cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="c7b42-198">Initializing a Dialog Box</span></span>

<span data-ttu-id="c7b42-199">Inicializa el cuadro de diálogo y su contenido mientras procesa el mensaje de [**\_ INITDIALOG de WM**](wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="c7b42-199">You initialize the dialog box and its contents while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="c7b42-200">La tarea más común consiste en inicializar los controles para reflejar la configuración actual del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-200">The most common task is to initialize the controls to reflect the current dialog box settings.</span></span> <span data-ttu-id="c7b42-201">Otra tarea habitual es centrar un cuadro de diálogo en la pantalla o en su ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="c7b42-201">Another common task is to center a dialog box on the screen or within its owner window.</span></span> <span data-ttu-id="c7b42-202">Una tarea útil para algunos cuadros de diálogo es establecer el foco de entrada en un control especificado, en lugar de aceptar el foco de entrada predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c7b42-202">A useful task for some dialog boxes is to set the input focus to a specified control rather than accept the default input focus.</span></span>

<span data-ttu-id="c7b42-203">En el ejemplo siguiente, el procedimiento del cuadro de diálogo centra el cuadro de diálogo y establece el foco de entrada al procesar el mensaje de [**\_ INITDIALOG de WM**](wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="c7b42-203">In the following example, the dialog box procedure centers the dialog box and sets the input focus while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="c7b42-204">Para centrar el cuadro de diálogo, el procedimiento recupera los rectángulos de ventana para el cuadro de diálogo y la ventana propietaria y calcula una nueva posición para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-204">To center the dialog box, the procedure retrieves the window rectangles for the dialog box and the owner window and calculates a new position for the dialog box.</span></span> <span data-ttu-id="c7b42-205">Para establecer el foco de entrada, el procedimiento comprueba el parámetro *wParam* para determinar el identificador del foco de entrada predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c7b42-205">To set the input focus, the procedure checks the *wParam* parameter to determine the identifier of the default input focus.</span></span>


```
HWND hwndOwner; 
RECT rc, rcDlg, rcOwner; 

....
 
case WM_INITDIALOG: 

    // Get the owner window and dialog box rectangles. 

    if ((hwndOwner = GetParent(hwndDlg)) == NULL) 
    {
        hwndOwner = GetDesktopWindow(); 
    }

    GetWindowRect(hwndOwner, &rcOwner); 
    GetWindowRect(hwndDlg, &rcDlg); 
    CopyRect(&rc, &rcOwner); 

    // Offset the owner and dialog box rectangles so that right and bottom 
    // values represent the width and height, and then offset the owner again 
    // to discard space taken up by the dialog box. 

    OffsetRect(&rcDlg, -rcDlg.left, -rcDlg.top); 
    OffsetRect(&rc, -rc.left, -rc.top); 
    OffsetRect(&rc, -rcDlg.right, -rcDlg.bottom); 

    // The new position is the sum of half the remaining space and the owner's 
    // original position. 

    SetWindowPos(hwndDlg, 
                 HWND_TOP, 
                 rcOwner.left + (rc.right / 2), 
                 rcOwner.top + (rc.bottom / 2), 
                 0, 0,          // Ignores size arguments. 
                 SWP_NOSIZE); 

    if (GetDlgCtrlID((HWND) wParam) != ID_ITEMNAME) 
    { 
        SetFocus(GetDlgItem(hwndDlg, ID_ITEMNAME)); 
        return FALSE; 
    } 
    return TRUE; 
```



<span data-ttu-id="c7b42-206">En las instrucciones anteriores, el procedimiento usa la función [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) para recuperar el identificador de la ventana propietaria de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7b42-206">In the preceding statements, the procedure uses the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function to retrieve the owner window handle to a dialog box.</span></span> <span data-ttu-id="c7b42-207">La función devuelve el identificador de la ventana propietaria a los cuadros de diálogo y el identificador de la ventana primaria a las ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="c7b42-207">The function returns the owner window handle to dialog boxes, and the parent window handle to child windows.</span></span> <span data-ttu-id="c7b42-208">Dado que una aplicación puede crear un cuadro de diálogo que no tiene ningún propietario, el procedimiento comprueba el identificador devuelto y usa la función [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) para recuperar el identificador de la ventana del escritorio, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="c7b42-208">Because an application can create a dialog box that has no owner, the procedure checks the returned handle and uses the [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) function to retrieve the desktop window handle, if necessary.</span></span> <span data-ttu-id="c7b42-209">Después de calcular la nueva posición, el procedimiento usa la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para mover el cuadro de diálogo, especificando el \_ valor superior de HWND para asegurarse de que el cuadro de diálogo permanece en la parte superior de la ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="c7b42-209">After calculating the new position, the procedure uses the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to move the dialog box, specifying the HWND\_TOP value to ensure that the dialog box remains on top of the owner window.</span></span>

<span data-ttu-id="c7b42-210">Antes de establecer el foco de entrada, el procedimiento comprueba el identificador del control del foco de entrada predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c7b42-210">Before setting the input focus, the procedure checks the control identifier of the default input focus.</span></span> <span data-ttu-id="c7b42-211">El sistema pasa el identificador de ventana del foco de entrada predeterminado en el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="c7b42-211">The system passes the window handle of the default input focus in the *wParam* parameter.</span></span> <span data-ttu-id="c7b42-212">La función [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) devuelve el identificador del control identificado por el identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="c7b42-212">The [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) function returns the identifier for the control identified by the window handle.</span></span> <span data-ttu-id="c7b42-213">Si el identificador no coincide con el identificador correcto, el procedimiento utiliza la función [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) para establecer el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="c7b42-213">If the identifier does not match the correct identifier, the procedure uses the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function to set the input focus.</span></span> <span data-ttu-id="c7b42-214">La función [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) es necesaria para recuperar el identificador de ventana del control deseado.</span><span class="sxs-lookup"><span data-stu-id="c7b42-214">The [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) function is required to retrieve the window handle of the desired control.</span></span>

## <a name="creating-a-template-in-memory"></a><span data-ttu-id="c7b42-215">Crear una plantilla en memoria</span><span class="sxs-lookup"><span data-stu-id="c7b42-215">Creating a Template in Memory</span></span>

<span data-ttu-id="c7b42-216">A veces, las aplicaciones adaptan o modifican el contenido de los cuadros de diálogo en función del estado actual de los datos que se están procesando.</span><span class="sxs-lookup"><span data-stu-id="c7b42-216">Applications sometimes adapt or modify the content of dialog boxes depending on the current state of the data being processed.</span></span> <span data-ttu-id="c7b42-217">En tales casos, no es práctico proporcionar todas las plantillas de cuadro de diálogo posibles como recursos en el archivo ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c7b42-217">In such cases, it is not practical to provide all possible dialog box templates as resources in the application's executable file.</span></span> <span data-ttu-id="c7b42-218">Pero la creación de plantillas en memoria ofrece a la aplicación más flexibilidad para adaptarse a cualquier circunstancia.</span><span class="sxs-lookup"><span data-stu-id="c7b42-218">But creating templates in memory gives the application more flexibility to adapt to any circumstances.</span></span>

<span data-ttu-id="c7b42-219">En el ejemplo siguiente, la aplicación crea una plantilla en memoria para un cuadro de diálogo modal que contiene un mensaje y botones **Aceptar** y **ayuda** .</span><span class="sxs-lookup"><span data-stu-id="c7b42-219">In the following example, the application creates a template in memory for a modal dialog box that contains a message and **OK** and **Help** buttons.</span></span>

<span data-ttu-id="c7b42-220">En una plantilla de cuadro de diálogo, todas las cadenas de caracteres, como el cuadro de diálogo y los títulos de los botones, deben ser cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7b42-220">In a dialog template, all character strings, such as the dialog box and button titles, must be Unicode strings.</span></span> <span data-ttu-id="c7b42-221">En este ejemplo se usa la función [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) para generar estas cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7b42-221">This example uses the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings.</span></span>

<span data-ttu-id="c7b42-222">Las estructuras [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) de una plantilla de cuadro de diálogo se deben alinear en los límites **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c7b42-222">The [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures in a dialog template must be aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="c7b42-223">Para alinear estas estructuras, en este ejemplo se usa una rutina auxiliar que toma un puntero de entrada y devuelve el puntero más cercano que está alineado en un límite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c7b42-223">To align these structures, this example uses a helper routine that takes an input pointer and returns the closest pointer that is aligned on a **DWORD** boundary.</span></span>


```
#define ID_HELP   150
#define ID_TEXT   200

LPWORD lpwAlign(LPWORD lpIn)
{
    ULONG ul;

    ul = (ULONG)lpIn;
    ul ++;
    ul >>=1;
    ul <<=1;
    return (LPWORD)ul;
}

LRESULT DisplayMyMessage(HINSTANCE hinst, HWND hwndOwner, LPSTR lpszMessage)
{
    HGLOBAL hgbl;
    LPDLGTEMPLATE lpdt;
    LPDLGITEMTEMPLATE lpdit;
    LPWORD lpw;
    LPWSTR lpwsz;
    LRESULT ret;
    int nchar;

    hgbl = GlobalAlloc(GMEM_ZEROINIT, 1024);
    if (!hgbl)
        return -1;
 
    lpdt = (LPDLGTEMPLATE)GlobalLock(hgbl);
 
    // Define a dialog box.
 
    lpdt->style = WS_POPUP | WS_BORDER | WS_SYSMENU | DS_MODALFRAME | WS_CAPTION;
    lpdt->cdit = 3;         // Number of controls
    lpdt->x  = 10;  lpdt->y  = 10;
    lpdt->cx = 100; lpdt->cy = 100;

    lpw = (LPWORD)(lpdt + 1);
    *lpw++ = 0;             // No menu
    *lpw++ = 0;             // Predefined dialog box class (by default)

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "My Dialog", -1, lpwsz, 50);
    lpw += nchar;

    //-----------------------
    // Define an OK button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 70;
    lpdit->cx = 80; lpdit->cy = 20;
    lpdit->id = IDOK;       // OK button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_DEFPUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "OK", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a Help button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 55; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_HELP;    // Help button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_PUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class atom

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "Help", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a static text control.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_TEXT;    // Text identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | SS_LEFT;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0082;        // Static class

    for (lpwsz = (LPWSTR)lpw; *lpwsz++ = (WCHAR)*lpszMessage++;);
    lpw = (LPWORD)lpwsz;
    *lpw++ = 0;             // No creation data

    GlobalUnlock(hgbl); 
    ret = DialogBoxIndirect(hinst, 
                           (LPDLGTEMPLATE)hgbl, 
                           hwndOwner, 
                           (DLGPROC)DialogProc); 
    GlobalFree(hgbl); 
    return ret; 
}
```



 

 