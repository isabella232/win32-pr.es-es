---
title: Cómo agregar elementos de List-View y subelementos
description: En este tema se muestra cómo agregar elementos y subelementos a un control de vista de lista.
ms.assetid: B7E204DC-FD08-4639-985D-1459A1AC0ED6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b3d20008edc10fda810261427507c77e9cfe34
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104149736"
---
# <a name="how-to-add-list-view-items-and-subitems"></a><span data-ttu-id="4bf0f-103">Cómo agregar elementos de List-View y subelementos</span><span class="sxs-lookup"><span data-stu-id="4bf0f-103">How to Add List-View Items and Subitems</span></span>

<span data-ttu-id="4bf0f-104">En este tema se muestra cómo agregar elementos y subelementos a un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-104">This topic demonstrates how to add items and subitems to a list-view control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4bf0f-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="4bf0f-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4bf0f-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="4bf0f-106">Technologies</span></span>

-   [<span data-ttu-id="4bf0f-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="4bf0f-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="4bf0f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4bf0f-108">Prerequisites</span></span>

-   <span data-ttu-id="4bf0f-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="4bf0f-109">C/C++</span></span>
-   <span data-ttu-id="4bf0f-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="4bf0f-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="4bf0f-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="4bf0f-111">Instructions</span></span>


<span data-ttu-id="4bf0f-112">Para agregar un elemento a un control de vista de lista, una aplicación debe definir primero una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) y, a continuación, enviar un mensaje [**\_ INSERTITEM de LVM**](lvm-insertitem.md) , especificando la dirección de la estructura **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="4bf0f-112">To add an item to a list-view control, an application must first define an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure and then send an [**LVM\_INSERTITEM**](lvm-insertitem.md) message, specifying the address of the **LVITEM** structure.</span></span> <span data-ttu-id="4bf0f-113">Si una aplicación usa la vista de informe, se debe proporcionar el texto del subelemento.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-113">If an application uses report view, subitem text must be provided.</span></span>

<span data-ttu-id="4bf0f-114">En el siguiente ejemplo de código de C++ se rellena una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) y se agregan los elementos de vista de lista mediante el mensaje [**\_ INSERTITEM de LVM**](lvm-insertitem.md) o la macro [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem)correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-114">The following C++ code example fills an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure and adds the list-view items by using the [**LVM\_INSERTITEM**](lvm-insertitem.md) message or the corresponding macro [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem).</span></span> <span data-ttu-id="4bf0f-115">Dado que la aplicación guarda su propio texto, especifica el \_ valor de LPSTR TEXTCALLBACK para el miembro **miembros pszText** de la estructura **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="4bf0f-115">Because the application saves its own text, it specifies the LPSTR\_TEXTCALLBACK value for the **pszText** member of the **LVITEM** structure.</span></span> <span data-ttu-id="4bf0f-116">Especificar el valor de LPSTR \_ TEXTCALLBACK hace que el control envíe un código de notificación de [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) a su ventana propietaria siempre que necesite mostrar un elemento.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-116">Specifying the LPSTR\_TEXTCALLBACK value causes the control to send an [**LVN\_GETDISPINFO**](lvn-getdispinfo.md) notification code to its owner window whenever it needs to display an item.</span></span>


```C++
// InsertListViewItems: Inserts items into a list view. 
// hWndListView:        Handle to the list-view control.
// cItems:              Number of items to insert.
// Returns TRUE if successful, and FALSE otherwise.
BOOL InsertListViewItems(HWND hWndListView, int cItems)
{
    LVITEM lvI;

    // Initialize LVITEM members that are common to all items.
    lvI.pszText   = LPSTR_TEXTCALLBACK; // Sends an LVN_GETDISPINFO message.
    lvI.mask      = LVIF_TEXT | LVIF_IMAGE |LVIF_STATE;
    lvI.stateMask = 0;
    lvI.iSubItem  = 0;
    lvI.state     = 0;

    // Initialize LVITEM members that are different for each item.
    for (int index = 0; index < cItems; index++)
    {
        lvI.iItem  = index;
        lvI.iImage = index;
    
        // Insert items into the list.
        if (ListView_InsertItem(hWndListView, &lvI) == -1)
            return FALSE;
    }

    return TRUE;
}

// HandleWM_NOTIFY - Handles the LVN_GETDISPINFO notification code that is 
//         sent in a WM_NOTIFY to the list view parent window. The function 
//        provides display strings for list view items and subitems.
//
// lParam - The LPARAM parameter passed with the WM_NOTIFY message.
// rgPetInfo - A global array of structures, defined as follows:
//         struct PETINFO
//        {
//            TCHAR szKind[10];
//            TCHAR szBreed[50];
//            TCHAR szPrice[20];
//        };
//
//        PETINFO rgPetInfo[ ] = 
//        {
//            {TEXT("Dog"),  TEXT("Poodle"),     TEXT("$300.00")},
//            {TEXT("Cat"),  TEXT("Siamese"),    TEXT("$100.00")},
//            {TEXT("Fish"), TEXT("Angel Fish"), TEXT("$10.00")},
//            {TEXT("Bird"), TEXT("Parakeet"),   TEXT("$5.00")},
//            {TEXT("Toad"), TEXT("Woodhouse"),  TEXT("$0.25")},
//        };
//
void HandleWM_NOTIFY(LPARAM lParam)
{
    NMLVDISPINFO* plvdi;

    switch (((LPNMHDR) lParam)->code)
    {
        case LVN_GETDISPINFO:

            plvdi = (NMLVDISPINFO*)lParam;

            switch (plvdi->item.iSubItem)
            {
                case 0:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szKind;
                    break;
                      
                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;
                
                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;
                
                default:
                    break;
            }

        break;

    }
    // NOTE: In addition to setting pszText to point to the item text, you could 
    // copy the item text into pszText using StringCchCopy. For example:
    //
    // StringCchCopy(plvdi->item.pszText, 
    //                         plvdi->item.cchTextMax, 
    //                         rgPetInfo[plvdi->item.iItem].szKind);

    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="4bf0f-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4bf0f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bf0f-118">Referencia de control de vista de lista</span><span class="sxs-lookup"><span data-stu-id="4bf0f-118">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="4bf0f-119">Acerca de los controles List-View</span><span class="sxs-lookup"><span data-stu-id="4bf0f-119">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="4bf0f-120">Usar controles List-View</span><span class="sxs-lookup"><span data-stu-id="4bf0f-120">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




