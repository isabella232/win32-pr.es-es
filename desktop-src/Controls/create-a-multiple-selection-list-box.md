---
title: Cómo crear un cuadro de lista de Multiple-Selection
description: En este tema se muestra cómo mostrar y obtener acceso al contenido de un directorio en un cuadro de lista de selección múltiple.
ms.assetid: 5192E171-8CEF-4921-9378-A7C3A52A9024
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd47b1d582d53a66bc77284927aef4230043e92
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078619"
---
# <a name="how-to-create-a-multiple-selection-list-box"></a>Cómo crear un cuadro de lista de Multiple-Selection

En este tema se muestra cómo mostrar y obtener acceso al contenido de un directorio en un cuadro de lista de selección múltiple. En un cuadro de lista de selección múltiple, el usuario puede seleccionar más de un elemento a la vez.

El ejemplo de código de C++ de este tema permite a un usuario ver una lista de archivos en el directorio actual, seleccionar un grupo de archivos de la lista y eliminarlos.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


La aplicación de lista de directorios debe realizar las siguientes tareas relacionadas con el cuadro de lista:

-   Inicializa el cuadro de lista.
-   Recupere las selecciones del usuario del cuadro de lista.
-   Quite los nombres de archivo del cuadro de lista una vez eliminados los archivos seleccionados.

En el siguiente ejemplo de código de C++, el procedimiento de cuadro de diálogo inicializa el cuadro de lista de selección múltiple (IDC \_ FileList) mediante la función [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) para rellenar el cuadro de lista con los nombres de todos los archivos del directorio actual.

Cuando el usuario selecciona un grupo de archivos y elige el botón **eliminar** , el procedimiento de cuadro de diálogo envía el mensaje [**lb \_ GETSELCOUNT**](lb-getselcount.md) , para recuperar el número de archivos seleccionados y el [**mensaje \_ lb GETSELITEMS**](lb-getselitems.md) , para recuperar una matriz de elementos de cuadro de lista seleccionados. Después de eliminar un archivo, el procedimiento de diálogo quita el elemento correspondiente del cuadro de lista mediante el envío del mensaje [**lb \_ DELETESTRING**](lb-deletestring.md) .



```C++
#define BIGBUFF 8192 
 
INT_PTR CALLBACK DlgDelFilesProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int cSelItems; 
    int cSelItemsInBuffer; 
    TCHAR achBuffer[MAX_PATH]; 
    int aSelItems[BIGBUFF]; 
    int i; 
    BOOL fResult; 
    HWND hListBox;
    int iRet;
 
    switch (message) { 
 
        case WM_INITDIALOG: 
 
            // Initialize the list box by filling it with files from 
            // the current directory. 
            pszCurDir = achBuffer; 
            GetCurrentDirectory(MAX_PATH, pszCurDir);
            DlgDirList(hDlg, pszCurDir, IDC_FILELIST, IDS_PATHTOFILL, 0); 
            SetFocus(GetDlgItem(hDlg, IDC_FILELIST)); 
 
            return FALSE; 
 
        case WM_COMMAND: 
 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
 
                    // When the user presses the DEL (IDOK) button, 
                    // first retrieve the list of selected files. 
                    pszFileToDelete = achBuffer; 
                    hListBox = GetDlgItem(hDlg, IDC_FILELIST); 
                    cSelItems = SendMessage(hListBox, 
                            LB_GETSELCOUNT, 0, 0); 
 
                    cSelItemsInBuffer = SendMessage(hListBox, 
                            LB_GETSELITEMS, 512, (LPARAM) aSelItems); 
 
                    if (cSelItems > cSelItemsInBuffer) 
                    { 
                        MessageBox(hDlg, L"Too many items selected.", 
                                NULL, MB_OK); 
                    } 
                    else 
                    { 

                        // Make sure the user really wants to delete the files.
                        iRet = MessageBox(hDlg, 
                            L"Are you sure you want to delete these files?", 
                            L"Deleting Files", MB_YESNO | MB_ICONEXCLAMATION);
                        if (iRet == IDNO)
                            return TRUE;

                        // Go through the list backward because after deleting
                        // an item the indices change for every subsequent 
                        // item. By going backward, the indices are never 
                        // invalidated. 
                        for (i = cSelItemsInBuffer - 1; i >= 0; i--) 
                        { 
                            SendMessage(hListBox, LB_GETTEXT, 
                                        aSelItems[i], 
                                        (LPARAM) pszFileToDelete); 
 
                            fResult = DeleteFile(pszFileToDelete); 
                            if (!fResult) 
                            {                     
                                MessageBox(hDlg, L"Could not delete file.", 
                                    NULL, MB_OK);     
                            } 
                            else 
                            { 
                                SendMessage(hListBox, LB_DELETESTRING, 
                                        aSelItems[i], 0); 
                            } 
                        } 
                        SendMessage(hListBox, LB_SETCARETINDEX, 0, 0); 
                    } 
                    return TRUE; 
 
                case IDCANCEL: 
 
                    // Destroy the dialog box. 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    return FALSE; 
            } 
 
        default: 
                return FALSE; 
    } 
} 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control de cuadro de lista](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Acerca de los cuadros de lista](about-list-boxes.md)
</dt> <dt>

[Usar cuadros de lista](using-list-boxes.md)
</dt> </dl>

 

 




