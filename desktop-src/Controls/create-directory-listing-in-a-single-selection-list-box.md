---
title: Creación de una lista de directorios en un ListBox
description: En este tema se muestra cómo usar un cuadro de lista de selección única para mostrar y acceder al contenido de un directorio.
ms.assetid: 11C0DB10-59BA-47C4-8687-101A2A85D660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03829990605271574a2030486ac5aba428867ec3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062218"
---
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a>Creación de una lista de directorios en un listBox de selección única

En este tema se muestra cómo usar un cuadro de lista de selección única para mostrar y acceder al contenido de un directorio. El cuadro de lista de selección única es el tipo de cuadro de lista predeterminado. Un usuario solo puede seleccionar un elemento a la vez en un cuadro de lista de selección única.

El ejemplo de código de C++ de este tema permite a un usuario ver una lista de archivos en el directorio actual, seleccionar un archivo de la lista y eliminarlo.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


La aplicación de lista de directorios debe realizar las siguientes tareas relacionadas con el cuadro de lista:

-   Inicialice el cuadro de lista.
-   Recupere la selección del usuario del cuadro de lista.
-   Quite el nombre de archivo del cuadro de lista después de eliminar el archivo seleccionado.

En el siguiente ejemplo de código de C++, el procedimiento del cuadro de diálogo inicializa el cuadro de lista de selección única (IDC FILELIST) mediante la función \_ [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) para rellenar el cuadro de lista con los nombres de todos los archivos del directorio actual. Cuando el usuario selecciona un archivo  y elige el botón Eliminar, la función [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) recupera el nombre del archivo seleccionado. El código elimina el archivo mediante la función [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) y actualiza el cuadro de lista de directorios mediante el envío del [**mensaje \_ DELETESTRING de LB.**](lb-deletestring.md)



```C++
INT_PTR CALLBACK DlgDelFileProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int iLBItem; 
    int cStringsRemaining; 
    int iRet; 
    TCHAR achBuffer[MAX_PATH]; 
    TCHAR achTemp[MAX_PATH]; 
    BOOL fResult;     
 
    switch (message) 
    { 
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
                    // first retrieve the selected file. 
                    pszFileToDelete = achBuffer; 
                    DlgDirSelectEx(hDlg, pszFileToDelete, MAX_PATH, 
                        IDC_FILELIST); 

                    // Make sure the user really wants to delete the file.
                    achTemp[MAX_PATH];
                    StringCbPrintf (achTemp, ARRAYSIZE(achTemp),  
                            TEXT("Are you sure you want to delete %s?"), 
                            pszFileToDelete);
                    iRet = MessageBox(hDlg, achTemp, L"Deleting Files", 
                        MB_YESNO | MB_ICONEXCLAMATION);
                    if (iRet == IDNO)
                        return TRUE;;

                    // Delete the file.
                    fResult = DeleteFile(pszFileToDelete); 
                    if (!fResult) 
                    { 
                        MessageBox(hDlg, L"Could not delete file.", 
                            NULL, MB_OK); 
                    } 
                    else // Remove the filename from the list box.
                    { 
                        // Get the selected item.
                        iLBItem = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_GETCURSEL, 0, 0); 
 
                        // Delete the selected item.
                        cStringsRemaining = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_DELETESTRING, iLBItem, 0); 
 
                        // If this is not the last item, set the selection to 
                        // the item immediately following the one just deleted.
                        // Otherwise, set the selection to the last item.
                         if (cStringsRemaining > iLBItem) 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, iLBItem, 0); 
                        } 
                        else 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, cStringsRemaining, 0); 
                        } 
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

[Referencia del control List Box](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Acerca de los cuadros de lista](about-list-boxes.md)
</dt> <dt>

[Usar cuadros de lista](using-list-boxes.md)
</dt> </dl>

 

 