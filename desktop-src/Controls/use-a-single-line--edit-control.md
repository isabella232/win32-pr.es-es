---
title: Cómo crear un control de edición de una sola línea
description: En este tema se muestra cómo crear un cuadro de diálogo que contiene un control de edición de una sola línea.
ms.assetid: 742DF606-9998-46D0-8D0A-F79508AAFFC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 597c3e611f53af56a42f837c4d85a43f97ff846e371314b130d72c568aaf860e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829125"
---
# <a name="how-to-create-a-single-line-edit-control"></a>Cómo crear un control de edición de una sola línea

En este tema se muestra cómo crear un cuadro de diálogo que contiene un control de edición de una sola línea.

El control de edición de una sola línea tiene el [**estilo ES \_ PASSWORD.**](edit-control-styles.md) De forma predeterminada, los controles de edición con este estilo muestran un asterisco para cada carácter que escribe el usuario. Sin embargo, en este ejemplo se usa el [**mensaje EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md) para cambiar el carácter predeterminado de un asterisco a un signo más (+). La siguiente captura de pantalla muestra el cuadro de diálogo después de que el usuario haya escrito una contraseña.

![captura de pantalla de un cuadro de diálogo que contiene un control de edición para escribir una contraseña](images/passworddlg.png)

> [!Note]  
> Comctl32.dll versión 6 no es redistribuible. Para usar Comctl32.dll versión 6, es especificarlo en un manifiesto. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a>Paso 1: Crear una instancia del cuadro de diálogo de contraseña.

En el siguiente ejemplo de código de C++ se usa la función DialogBox para crear un cuadro de diálogo modal. La plantilla de cuadro de **diálogo IDD \_ PASSWORD** se pasa como parámetro. Define, entre otras cosas, los estilos de ventana, los botones y las dimensiones del cuadro de diálogo de contraseña.


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a>Paso 2: Inicializar el cuadro de diálogo y procesar la entrada del usuario.

El procedimiento de ventana del ejemplo siguiente inicializa el cuadro de diálogo de contraseña y procesa los mensajes de notificación y la entrada del usuario.

Durante la inicialización, el procedimiento de ventana cambia el carácter de contraseña predeterminado a un signo y **+** establece el botón de inserción predeterminado en **Cancelar**.

Durante el procesamiento de entradas de usuario, el procedimiento de ventana cambia el botón de inserción predeterminado de **CANCEL** a **OK** en cuanto el usuario escribe texto en el control de edición. Si el usuario presiona el botón **Aceptar,** el procedimiento de ventana usa los mensajes [**EM \_ LINELENGTH**](em-linelength.md) y [**EM \_ GETLINE**](em-getline.md) para recuperar el texto.



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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de editar controles](about-edit-controls.md)
</dt> <dt>

[Editar referencia de control](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Usar controles de edición](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Editar control](edit-controls.md)
</dt> </dl>

 

 