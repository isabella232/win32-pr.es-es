---
title: Crear una lista de directorios en un cuadro de lista
description: En este tema se muestra cómo usar un cuadro de lista de selección única para mostrar y obtener acceso al contenido de un directorio.
ms.assetid: 11C0DB10-59BA-47C4-8687-101A2A85D660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03829990605271574a2030486ac5aba428867ec3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995738"
---
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a><span data-ttu-id="b7f17-103">Cómo crear una lista de directorios en un cuadro de lista de selección única</span><span class="sxs-lookup"><span data-stu-id="b7f17-103">How to create a directory listing in a single-selection ListBox</span></span>

<span data-ttu-id="b7f17-104">En este tema se muestra cómo usar un cuadro de lista de selección única para mostrar y obtener acceso al contenido de un directorio.</span><span class="sxs-lookup"><span data-stu-id="b7f17-104">This topic demonstrates how to use a single-selection list box to display and access the contents of a directory.</span></span> <span data-ttu-id="b7f17-105">El cuadro de lista de selección única es el tipo de cuadro de lista predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b7f17-105">The single-selection list box is the default list box type.</span></span> <span data-ttu-id="b7f17-106">Un usuario solo puede seleccionar un elemento cada vez desde un cuadro de lista de selección única.</span><span class="sxs-lookup"><span data-stu-id="b7f17-106">A user can only select one item at a time from a single-selection list box.</span></span>

<span data-ttu-id="b7f17-107">El ejemplo de código de C++ de este tema permite a un usuario ver una lista de archivos en el directorio actual, seleccionar un archivo de la lista y eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="b7f17-107">The C++ code example in this topic enables a user to view a list of files in the current directory, select a file from the list, and delete it.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b7f17-108">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="b7f17-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b7f17-109">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="b7f17-109">Technologies</span></span>

-   [<span data-ttu-id="b7f17-110">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="b7f17-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b7f17-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b7f17-111">Prerequisites</span></span>

-   <span data-ttu-id="b7f17-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="b7f17-112">C/C++</span></span>
-   <span data-ttu-id="b7f17-113">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="b7f17-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b7f17-114">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="b7f17-114">Instructions</span></span>


<span data-ttu-id="b7f17-115">La aplicación de lista de directorios debe realizar las siguientes tareas relacionadas con el cuadro de lista:</span><span class="sxs-lookup"><span data-stu-id="b7f17-115">The directory listing application must perform the following list box related tasks:</span></span>

-   <span data-ttu-id="b7f17-116">Inicializa el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b7f17-116">Initialize the list box.</span></span>
-   <span data-ttu-id="b7f17-117">Recupere la selección del usuario del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b7f17-117">Retrieve the user's selection from the list box.</span></span>
-   <span data-ttu-id="b7f17-118">Quitar el nombre de archivo del cuadro de lista una vez eliminado el archivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="b7f17-118">Remove the file name from the list box after the selected file has been deleted.</span></span>

<span data-ttu-id="b7f17-119">En el siguiente ejemplo de código de C++, el procedimiento de cuadro de diálogo inicializa el cuadro de lista de selección única ( \_ nombre de archivo de IDC) mediante la función [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) para rellenar el cuadro de lista con los nombres de todos los archivos del directorio actual.</span><span class="sxs-lookup"><span data-stu-id="b7f17-119">In the following C++ code example, the dialog box procedure initializes the single-selection list box (IDC\_FILELIST) by using the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function to fill the list box with the names of all the files in the current directory.</span></span> <span data-ttu-id="b7f17-120">Cuando el usuario selecciona un archivo y elige el botón **eliminar** , la función [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) recupera el nombre del archivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="b7f17-120">When the user selects a file and chooses the **Delete** button, the [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) function retrieves the name of the selected file.</span></span> <span data-ttu-id="b7f17-121">El código elimina el archivo mediante la función [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) y actualiza el cuadro de lista de directorios mediante el envío del mensaje [**lb \_ DELETESTRING**](lb-deletestring.md) .</span><span class="sxs-lookup"><span data-stu-id="b7f17-121">The code deletes the file by using the [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) function and updates the directory list box by sending the [**LB\_DELETESTRING**](lb-deletestring.md) message.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="b7f17-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b7f17-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7f17-123">Referencia de control de cuadro de lista</span><span class="sxs-lookup"><span data-stu-id="b7f17-123">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b7f17-124">Acerca de los cuadros de lista</span><span class="sxs-lookup"><span data-stu-id="b7f17-124">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="b7f17-125">Usar cuadros de lista</span><span class="sxs-lookup"><span data-stu-id="b7f17-125">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 