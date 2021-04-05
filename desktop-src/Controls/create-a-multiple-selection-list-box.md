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
# <a name="how-to-create-a-multiple-selection-list-box"></a><span data-ttu-id="c0038-103">Cómo crear un cuadro de lista de Multiple-Selection</span><span class="sxs-lookup"><span data-stu-id="c0038-103">How to Create a Multiple-Selection List Box</span></span>

<span data-ttu-id="c0038-104">En este tema se muestra cómo mostrar y obtener acceso al contenido de un directorio en un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="c0038-104">This topic demonstrates how to display and access the contents of a directory in a multiple-selection list box.</span></span> <span data-ttu-id="c0038-105">En un cuadro de lista de selección múltiple, el usuario puede seleccionar más de un elemento a la vez.</span><span class="sxs-lookup"><span data-stu-id="c0038-105">In a multiple-selection list box, the user can select more than one item at a time.</span></span>

<span data-ttu-id="c0038-106">El ejemplo de código de C++ de este tema permite a un usuario ver una lista de archivos en el directorio actual, seleccionar un grupo de archivos de la lista y eliminarlos.</span><span class="sxs-lookup"><span data-stu-id="c0038-106">The C++ code example in this topic enables a user to view a list of files in the current directory, select a group of files from the list, and delete them.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c0038-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="c0038-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c0038-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="c0038-108">Technologies</span></span>

-   [<span data-ttu-id="c0038-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="c0038-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c0038-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c0038-110">Prerequisites</span></span>

-   <span data-ttu-id="c0038-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="c0038-111">C/C++</span></span>
-   <span data-ttu-id="c0038-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="c0038-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c0038-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="c0038-113">Instructions</span></span>


<span data-ttu-id="c0038-114">La aplicación de lista de directorios debe realizar las siguientes tareas relacionadas con el cuadro de lista:</span><span class="sxs-lookup"><span data-stu-id="c0038-114">The directory listing application must perform the following list box–related tasks:</span></span>

-   <span data-ttu-id="c0038-115">Inicializa el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="c0038-115">Initialize the list box.</span></span>
-   <span data-ttu-id="c0038-116">Recupere las selecciones del usuario del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="c0038-116">Retrieve the user's selections from the list box.</span></span>
-   <span data-ttu-id="c0038-117">Quite los nombres de archivo del cuadro de lista una vez eliminados los archivos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="c0038-117">Remove the file names from the list box after the selected files have been deleted.</span></span>

<span data-ttu-id="c0038-118">En el siguiente ejemplo de código de C++, el procedimiento de cuadro de diálogo inicializa el cuadro de lista de selección múltiple (IDC \_ FileList) mediante la función [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) para rellenar el cuadro de lista con los nombres de todos los archivos del directorio actual.</span><span class="sxs-lookup"><span data-stu-id="c0038-118">In the following C++ code example, the dialog box procedure initializes the multiple-selection list box (IDC\_FILELIST) by using the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function to fill the list box with the names of all the files in the current directory.</span></span>

<span data-ttu-id="c0038-119">Cuando el usuario selecciona un grupo de archivos y elige el botón **eliminar** , el procedimiento de cuadro de diálogo envía el mensaje [**lb \_ GETSELCOUNT**](lb-getselcount.md) , para recuperar el número de archivos seleccionados y el [**mensaje \_ lb GETSELITEMS**](lb-getselitems.md) , para recuperar una matriz de elementos de cuadro de lista seleccionados.</span><span class="sxs-lookup"><span data-stu-id="c0038-119">When the user selects a group of files and chooses the **Delete** button, the dialog box procedure sends the [**LB\_GETSELCOUNT**](lb-getselcount.md) message, to retrieve the number of files selected, and the [**LB\_GETSELITEMS**](lb-getselitems.md) message, to retrieve an array of selected list box items.</span></span> <span data-ttu-id="c0038-120">Después de eliminar un archivo, el procedimiento de diálogo quita el elemento correspondiente del cuadro de lista mediante el envío del mensaje [**lb \_ DELETESTRING**](lb-deletestring.md) .</span><span class="sxs-lookup"><span data-stu-id="c0038-120">After deleting a file, the dialog procedure removes the corresponding item from the list box by sending the [**LB\_DELETESTRING**](lb-deletestring.md) message.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="c0038-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0038-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0038-122">Referencia de control de cuadro de lista</span><span class="sxs-lookup"><span data-stu-id="c0038-122">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="c0038-123">Acerca de los cuadros de lista</span><span class="sxs-lookup"><span data-stu-id="c0038-123">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="c0038-124">Usar cuadros de lista</span><span class="sxs-lookup"><span data-stu-id="c0038-124">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 




