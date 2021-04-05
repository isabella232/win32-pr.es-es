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
# <a name="how-to-create-a-single-line-edit-control"></a>Cómo crear un control de edición de una sola línea

En este tema se muestra cómo crear un cuadro de diálogo que contiene un control de edición de una sola línea.

El control de edición de una sola línea tiene el estilo de [**\_ contraseña es**](edit-control-styles.md) . De forma predeterminada, los controles de edición con este estilo muestran un asterisco para cada carácter que escribe el usuario. Sin embargo, en este ejemplo se usa el mensaje [**em \_ SETPASSWORDCHAR**](em-setpasswordchar.md) para cambiar el carácter predeterminado de un asterisco a un signo más (+). En la captura de pantalla siguiente se muestra el cuadro de diálogo después de que el usuario haya escrito una contraseña.

![captura de pantalla de un cuadro de diálogo que contiene un control de edición para escribir una contraseña](images/passworddlg.png)

> [!Note]  
> Comctl32.dll versión 6 no es redistribuible. Para usar Comctl32.dll versión 6, especifíquelo en un manifiesto. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a>Paso 1: crear una instancia del cuadro de diálogo contraseña.

En el siguiente ejemplo de código de C++ se usa la función DialogBox para crear un cuadro de diálogo modal. La plantilla de cuadro de diálogo de **IDD \_ contraseña** se pasa como parámetro. Define, entre otras cosas, los estilos de ventana, los botones y las dimensiones del cuadro de diálogo contraseña.


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a>Paso 2: inicializar el cuadro de diálogo y procesar los datos proporcionados por el usuario.

El procedimiento de ventana del siguiente ejemplo inicializa el cuadro de diálogo contraseña y procesa los mensajes de notificación y los datos proporcionados por el usuario.

Durante la inicialización, el procedimiento de ventana cambia el carácter de contraseña predeterminado a un **+** signo y establece el método predeterminado para **Cancelar**.

Durante el procesamiento de los datos proporcionados por el usuario, el procedimiento de ventana cambia el botón de opción predeterminado de **Cancelar** a **correcto** en cuanto el usuario escribe texto en el control de edición. Si el usuario presiona el botón **Aceptar** , el procedimiento de ventana utiliza los mensajes [**em \_ LINELENGTH**](em-linelength.md) y [**em \_ GETLINE**](em-getline.md) para recuperar el texto.



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

[Acerca de los controles de edición](about-edit-controls.md)
</dt> <dt>

[Editar referencia de control](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Usar controles de edición](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Control de edición](edit-controls.md)
</dt> </dl>

 

 