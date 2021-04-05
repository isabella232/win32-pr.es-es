---
title: Cómo crear un control de edición de una sola línea
description: En este tema se muestra cómo crear un cuadro de diálogo que contiene un control de edición de una sola línea.
ms.assetid: 742DF606-9998-46D0-8D0A-F79508AAFFC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5d39a4c9fbc806de6ca151606e770eb0cea9b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078615"
---
# <a name="how-to-create-a-single-line-edit-control"></a><span data-ttu-id="2614c-103">Cómo crear un control de edición de una sola línea</span><span class="sxs-lookup"><span data-stu-id="2614c-103">How to Create a Single Line Edit Control</span></span>

<span data-ttu-id="2614c-104">En este tema se muestra cómo crear un cuadro de diálogo que contiene un control de edición de una sola línea.</span><span class="sxs-lookup"><span data-stu-id="2614c-104">This topic demonstrates how to create a dialog box that contains a single-line edit control.</span></span>

<span data-ttu-id="2614c-105">El control de edición de una sola línea tiene el estilo de [**\_ contraseña es**](edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2614c-105">The single-line edit control has the [**ES\_PASSWORD**](edit-control-styles.md) style.</span></span> <span data-ttu-id="2614c-106">De forma predeterminada, los controles de edición con este estilo muestran un asterisco para cada carácter que escribe el usuario.</span><span class="sxs-lookup"><span data-stu-id="2614c-106">By default, edit controls with this style display an asterisk for each character that is typed by the user.</span></span> <span data-ttu-id="2614c-107">Sin embargo, en este ejemplo se usa el mensaje [**em \_ SETPASSWORDCHAR**](em-setpasswordchar.md) para cambiar el carácter predeterminado de un asterisco a un signo más (+).</span><span class="sxs-lookup"><span data-stu-id="2614c-107">This example, however, uses the [**EM\_SETPASSWORDCHAR**](em-setpasswordchar.md) message to change the default character from an asterisk to a plus sign (+).</span></span> <span data-ttu-id="2614c-108">En la captura de pantalla siguiente se muestra el cuadro de diálogo después de que el usuario haya escrito una contraseña.</span><span class="sxs-lookup"><span data-stu-id="2614c-108">The following screen shot shows the dialog box after the user has entered a password.</span></span>

![captura de pantalla de un cuadro de diálogo que contiene un control de edición para escribir una contraseña](images/passworddlg.png)

> [!Note]  
> <span data-ttu-id="2614c-110">Comctl32.dll versión 6 no es redistribuible.</span><span class="sxs-lookup"><span data-stu-id="2614c-110">Comctl32.dll version 6 is not redistributable.</span></span> <span data-ttu-id="2614c-111">Para usar Comctl32.dll versión 6, especifíquelo en un manifiesto.</span><span class="sxs-lookup"><span data-stu-id="2614c-111">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="2614c-112">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2614c-112">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="2614c-113">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="2614c-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2614c-114">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="2614c-114">Technologies</span></span>

-   [<span data-ttu-id="2614c-115">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="2614c-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2614c-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2614c-116">Prerequisites</span></span>

-   <span data-ttu-id="2614c-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="2614c-117">C/C++</span></span>
-   <span data-ttu-id="2614c-118">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="2614c-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2614c-119">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="2614c-119">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a><span data-ttu-id="2614c-120">Paso 1: crear una instancia del cuadro de diálogo contraseña.</span><span class="sxs-lookup"><span data-stu-id="2614c-120">Step 1: Create an instance of the password dialog box.</span></span>

<span data-ttu-id="2614c-121">En el siguiente ejemplo de código de C++ se usa la función DialogBox para crear un cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="2614c-121">The following C++ code example uses the DialogBox function to create a modal dialog box.</span></span> <span data-ttu-id="2614c-122">La plantilla de cuadro de diálogo de **IDD \_ contraseña** se pasa como parámetro.</span><span class="sxs-lookup"><span data-stu-id="2614c-122">The dialog box template **IDD\_PASSWORD** is passed as a parameter.</span></span> <span data-ttu-id="2614c-123">Define, entre otras cosas, los estilos de ventana, los botones y las dimensiones del cuadro de diálogo contraseña.</span><span class="sxs-lookup"><span data-stu-id="2614c-123">It defines, among other things, the window styles, buttons, and dimensions of the password dialog box.</span></span>


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a><span data-ttu-id="2614c-124">Paso 2: inicializar el cuadro de diálogo y procesar los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2614c-124">Step 2: Initialize the dialog box and process user input.</span></span>

<span data-ttu-id="2614c-125">El procedimiento de ventana del siguiente ejemplo inicializa el cuadro de diálogo contraseña y procesa los mensajes de notificación y los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2614c-125">The window procedure in the following example initializes the password dialog box and processes notification messages and user input.</span></span>

<span data-ttu-id="2614c-126">Durante la inicialización, el procedimiento de ventana cambia el carácter de contraseña predeterminado a un **+** signo y establece el método predeterminado para **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="2614c-126">During initialization, the window procedure changes the default password character to a **+** sign and sets the default pushbutton to **Cancel**.</span></span>

<span data-ttu-id="2614c-127">Durante el procesamiento de los datos proporcionados por el usuario, el procedimiento de ventana cambia el botón de opción predeterminado de **Cancelar** a **correcto** en cuanto el usuario escribe texto en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="2614c-127">During user input processing, the window procedure changes the default push button from **CANCEL** to **OK** as soon as the user enters text in the edit control.</span></span> <span data-ttu-id="2614c-128">Si el usuario presiona el botón **Aceptar** , el procedimiento de ventana utiliza los mensajes [**em \_ LINELENGTH**](em-linelength.md) y [**em \_ GETLINE**](em-getline.md) para recuperar el texto.</span><span class="sxs-lookup"><span data-stu-id="2614c-128">If the user presses the **OK** button, the window procedure uses the [**EM\_LINELENGTH**](em-linelength.md) and [**EM\_GETLINE**](em-getline.md) messages to retrieve the text.</span></span>



```C++
INT_PTR CALLBACK PasswordProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    TCHAR lpszPassword[16]; 
    WORD cchPassword; 

    switch (message) 
    { 
        case WM_INITDIALOG: 
            // Set password character to a plus sign (+) 
            SendDlgItemMessage(hDlg, 
                               IDE_PASSWORDEDIT, 
                               EM_SETPASSWORDCHAR, 
                               (WPARAM) '+', 
                               (LPARAM) 0); 

            // Set the default push button to "Cancel." 
            SendMessage(hDlg, 
                        DM_SETDEFID, 
                        (WPARAM) IDCANCEL, 
                        (LPARAM) 0); 

            return TRUE; 

        case WM_COMMAND: 
            // Set the default push button to "OK" when the user enters text. 
            if(HIWORD (wParam) == EN_CHANGE && 
                                LOWORD(wParam) == IDE_PASSWORDEDIT) 
            {
                SendMessage(hDlg, 
                            DM_SETDEFID, 
                            (WPARAM) IDOK, 
                            (LPARAM) 0); 
            }
            switch(wParam) 
            { 
                case IDOK: 
                    // Get number of characters. 
                    cchPassword = (WORD) SendDlgItemMessage(hDlg, 
                                                            IDE_PASSWORDEDIT, 
                                                            EM_LINELENGTH, 
                                                            (WPARAM) 0, 
                                                            (LPARAM) 0); 
                    if (cchPassword >= 16) 
                    { 
                        MessageBox(hDlg, 
                                   L"Too many characters.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 
                    else if (cchPassword == 0) 
                    { 
                        MessageBox(hDlg, 
                                   L"No characters entered.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 

                    // Put the number of characters into first word of buffer. 
                    *((LPWORD)lpszPassword) = cchPassword; 

                    // Get the characters. 
                    SendDlgItemMessage(hDlg, 
                                       IDE_PASSWORDEDIT, 
                                       EM_GETLINE, 
                                       (WPARAM) 0,       // line 0 
                                       (LPARAM) lpszPassword); 

                    // Null-terminate the string. 
                    lpszPassword[cchPassword] = 0; 

                    MessageBox(hDlg, 
                               lpszPassword, 
                               L"Did it work?", 
                               MB_OK); 

                    // Call a local password-parsing function. 
                    ParsePassword(lpszPassword); 

                    EndDialog(hDlg, TRUE); 
                    return TRUE; 

                case IDCANCEL: 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
            } 
            return 0; 
    } 
    return FALSE; 
    
    UNREFERENCED_PARAMETER(lParam); 
}
```



## <a name="related-topics"></a><span data-ttu-id="2614c-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2614c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2614c-130">Acerca de los controles de edición</span><span class="sxs-lookup"><span data-stu-id="2614c-130">About Edit Controls</span></span>](about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="2614c-131">Editar referencia de control</span><span class="sxs-lookup"><span data-stu-id="2614c-131">Edit Control Reference</span></span>](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="2614c-132">Usar controles de edición</span><span class="sxs-lookup"><span data-stu-id="2614c-132">Using Edit Controls</span></span>](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[<span data-ttu-id="2614c-133">Control de edición</span><span class="sxs-lookup"><span data-stu-id="2614c-133">Edit Control</span></span>](edit-controls.md)
</dt> </dl>

 

 