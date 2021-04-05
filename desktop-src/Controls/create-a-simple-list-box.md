---
title: Cómo crear un cuadro de lista simple
description: En este tema se muestra cómo inicializar y recuperar elementos de un cuadro de lista simple.
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca2230b265d61e9a59a8892e14127d25bf2cfd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078613"
---
# <a name="how-to-create-a-simple-list-box"></a><span data-ttu-id="cc9b3-103">Cómo crear un cuadro de lista simple</span><span class="sxs-lookup"><span data-stu-id="cc9b3-103">How to Create a Simple List Box</span></span>

<span data-ttu-id="cc9b3-104">En este tema se muestra cómo inicializar y recuperar elementos de un cuadro de lista simple.</span><span class="sxs-lookup"><span data-stu-id="cc9b3-104">This topic demonstrates how to initialize and retrieve items from a simple list box.</span></span>

<span data-ttu-id="cc9b3-105">El ejemplo de código de C++ de este tema incluye un procedimiento de cuadro de diálogo que rellena un cuadro de lista con información sobre jugadores en un equipo deportivo.</span><span class="sxs-lookup"><span data-stu-id="cc9b3-105">The C++ code example in this topic includes a dialog box procedure that fills a list box with information about players on a sports team.</span></span> <span data-ttu-id="cc9b3-106">Cuando el usuario selecciona el nombre de un reproductor de la lista, se muestra información sobre el reproductor en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cc9b3-106">When the user selects the name of a player from the list, information about the player is displayed in the dialog box.</span></span> <span data-ttu-id="cc9b3-107">El estilo de ventana del cuadro de lista incluye la [**\_ ordenación lbs**](list-box-styles.md), lo que da como resultado una lista ordenada de elementos.</span><span class="sxs-lookup"><span data-stu-id="cc9b3-107">The window style for the list box includes [**LBS\_SORT**](list-box-styles.md), which results in a sorted list of items.</span></span> <span data-ttu-id="cc9b3-108">En la captura de pantalla siguiente se muestra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cc9b3-108">The following screen shot shows the dialog box.</span></span>

![captura de pantalla de un cuadro de diálogo que contiene un cuadro de lista con etiqueta, texto sobre el elemento de cuadro de lista seleccionado y un botón Aceptar](images/lb-roster.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="cc9b3-110">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="cc9b3-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cc9b3-111">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="cc9b3-111">Technologies</span></span>

-   [<span data-ttu-id="cc9b3-112">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="cc9b3-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cc9b3-113">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cc9b3-113">Prerequisites</span></span>

-   <span data-ttu-id="cc9b3-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="cc9b3-114">C/C++</span></span>
-   <span data-ttu-id="cc9b3-115">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="cc9b3-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cc9b3-116">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="cc9b3-116">Instructions</span></span>


<span data-ttu-id="cc9b3-117">La aplicación debe realizar las siguientes tareas relacionadas con el cuadro de lista:</span><span class="sxs-lookup"><span data-stu-id="cc9b3-117">The application must perform the following list box–related tasks:</span></span>

-   <span data-ttu-id="cc9b3-118">Inicializar el cuadro de lista</span><span class="sxs-lookup"><span data-stu-id="cc9b3-118">Initialize the list box</span></span>
-   <span data-ttu-id="cc9b3-119">Recuperar la selección del usuario del cuadro de lista</span><span class="sxs-lookup"><span data-stu-id="cc9b3-119">Retrieve the user's selection from the list box</span></span>

<span data-ttu-id="cc9b3-120">En el siguiente ejemplo de código de C++, la información acerca de los reproductores se almacena en una matriz de estructuras.</span><span class="sxs-lookup"><span data-stu-id="cc9b3-120">In the following C++ code example, information about players is stored in an array of structures.</span></span> <span data-ttu-id="cc9b3-121">Durante la inicialización, el procedimiento de cuadro de diálogo utiliza el mensaje de [**lb en lb \_**](lb-addstring.md) para agregar a la vez los nombres de los miembros del equipo al cuadro de lista (ejemplo de un **\_ control \_ IDC**).</span><span class="sxs-lookup"><span data-stu-id="cc9b3-121">During initialization, the dialog box procedure uses the [**LB\_ADDSTRING**](lb-addstring.md) message to add the names of team members to the list box (**IDC\_LISTBOX\_EXAMPLE**) one at a time.</span></span> <span data-ttu-id="cc9b3-122">También usa el mensaje [**lb \_ SETITEMDATA**](lb-setitemdata.md) para agregar el índice de la matriz del reproductor al cuadro de lista como datos de elemento.</span><span class="sxs-lookup"><span data-stu-id="cc9b3-122">It also uses the [**LB\_SETITEMDATA**](lb-setitemdata.md) message to add the array index of the player to the list box as item data.</span></span> <span data-ttu-id="cc9b3-123">Más adelante, cuando el usuario selecciona un reproductor en el cuadro de lista, el procedimiento de cuadro de diálogo utiliza el mensaje [**lb \_ GETITEMDATA**](lb-getitemdata.md) para recuperar el índice de la matriz correspondiente.</span><span class="sxs-lookup"><span data-stu-id="cc9b3-123">Later, when the user selects a player from the list box, the dialog box procedure uses the [**LB\_GETITEMDATA**](lb-getitemdata.md) message to retrieve the corresponding array index.</span></span> <span data-ttu-id="cc9b3-124">A continuación, usa el índice de la matriz para recuperar la información del reproductor de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cc9b3-124">It then uses the array index to retrieve player information from the array.</span></span>



```C++
typedef struct 
{ 
    TCHAR achName[MAX_PATH]; 
    TCHAR achPosition[12]; 
    int nGamesPlayed; 
    int nGoalsScored; 
} Player; 

Player Roster[] = 
{ 
    {TEXT("Haas, Jonathan"), TEXT("Midfield"), 18, 4 }, 
    {TEXT("Pai, Jyothi"), TEXT("Forward"), 36, 12 }, 
    {TEXT("Hanif, Kerim"), TEXT("Back"), 26, 0 }, 
    {TEXT("Anderberg, Michael"), TEXT("Back"), 24, 2 }, 
    {TEXT("Jelitto, Jacek"), TEXT("Midfield"), 26, 3 }, 
    {TEXT("Raposo, Rui"), TEXT("Back"), 24, 3}, 
    {TEXT("Joseph, Brad"), TEXT("Forward"), 13, 3 }, 
    {TEXT("Bouchard, Thomas"), TEXT("Forward"), 28, 5 }, 
    {TEXT("Salmre, Ivo "), TEXT("Midfield"), 27, 7 }, 
    {TEXT("Camp, David"), TEXT("Midfield"), 22, 3 }, 
    {TEXT("Kohl, Franz"), TEXT("Goalkeeper"), 17, 0 }, 
}; 


INT_PTR CALLBACK ListBoxExampleProc(HWND hDlg, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_INITDIALOG:
        {
            // Add items to list. 
            HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE);  
            for (int i = 0; i < ARRAYSIZE(Roster); i++) 
            { 
                int pos = (int)SendMessage(hwndList, LB_ADDSTRING, 0, 
                    (LPARAM) Roster[i].achName); 
                // Set the array index of the player as item data.
                // This enables us to retrieve the item from the array
                // even after the items are sorted by the list box.
                SendMessage(hwndList, LB_SETITEMDATA, pos, (LPARAM) i); 
            } 
            // Set input focus to the list box.
            SetFocus(hwndList); 
            return TRUE;               
        } 

    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case IDOK:
        case IDCANCEL:
            EndDialog(hDlg, LOWORD(wParam));
            return TRUE;

        case IDC_LISTBOX_EXAMPLE:
            {
                switch (HIWORD(wParam)) 
                { 
                case LBN_SELCHANGE:
                    {
                        HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE); 

                        // Get selected index.
                        int lbItem = (int)SendMessage(hwndList, LB_GETCURSEL, 0, 0); 

                        // Get item data.
                        int i = (int)SendMessage(hwndList, LB_GETITEMDATA, lbItem, 0);

                        // Do something with the data from Roster[i]
                        TCHAR buff[MAX_PATH];
                        StringCbPrintf (buff, ARRAYSIZE(buff),  
                            TEXT("Position: %s\nGames played: %d\nGoals: %d"), 
                            Roster[i].achPosition, Roster[i].nGamesPlayed, 
                            Roster[i].nGoalsScored);

                        SetDlgItemText(hDlg, IDC_STATISTICS, buff); 
                        return TRUE; 
                    } 
                }
            }
            return TRUE;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="cc9b3-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc9b3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc9b3-126">Referencia de control de cuadro de lista</span><span class="sxs-lookup"><span data-stu-id="cc9b3-126">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="cc9b3-127">Acerca de los cuadros de lista</span><span class="sxs-lookup"><span data-stu-id="cc9b3-127">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="cc9b3-128">Usar cuadros de lista</span><span class="sxs-lookup"><span data-stu-id="cc9b3-128">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 




