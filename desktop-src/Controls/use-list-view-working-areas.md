---
title: Cómo usar áreas de trabajo de List-View
description: En este tema se muestra cómo trabajar con áreas de trabajo de la vista de lista. Las áreas de trabajo son áreas virtuales rectangulares que se pueden utilizar para organizar los elementos en un control List-vista.
ms.assetid: 7A803B66-7827-49A3-8D87-6A037C09A19A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d3ed4142e6933e662f03f268723db145c7eb00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075554"
---
# <a name="how-to-use-list-view-working-areas"></a><span data-ttu-id="12ace-104">Cómo usar áreas de trabajo de List-View</span><span class="sxs-lookup"><span data-stu-id="12ace-104">How to Use List-View Working Areas</span></span>

<span data-ttu-id="12ace-105">En este tema se muestra cómo trabajar con áreas de trabajo de la vista de lista.</span><span class="sxs-lookup"><span data-stu-id="12ace-105">This topic demonstrates how to work with list-view working areas.</span></span> <span data-ttu-id="12ace-106">Las áreas de trabajo son áreas virtuales rectangulares que se pueden utilizar para organizar los elementos en un control List-vista.</span><span class="sxs-lookup"><span data-stu-id="12ace-106">Working areas are rectangular virtual areas that can be used to arrange items in a list-vew control.</span></span> <span data-ttu-id="12ace-107">Un área de trabajo no es una ventana y no puede tener un borde visible.</span><span class="sxs-lookup"><span data-stu-id="12ace-107">A working area is not a window and cannot have a visible border.</span></span> <span data-ttu-id="12ace-108">De forma predeterminada, el control de vista de lista no tiene áreas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="12ace-108">By default, the list-view control has no working areas.</span></span> <span data-ttu-id="12ace-109">Al crear un área de trabajo, puede crear un borde vacío en la parte izquierda, superior o derecha de los elementos, o hacer que se muestre una barra de desplazamiento horizontal cuando normalmente no hubiera ninguno.</span><span class="sxs-lookup"><span data-stu-id="12ace-109">By creating a working area, you can create an empty border on the left, top, or right of the items or cause a horizontal scroll bar to be displayed when there normally would not be one.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="12ace-110">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="12ace-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="12ace-111">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="12ace-111">Technologies</span></span>

-   [<span data-ttu-id="12ace-112">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="12ace-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="12ace-113">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="12ace-113">Prerequisites</span></span>

-   <span data-ttu-id="12ace-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="12ace-114">C/C++</span></span>
-   <span data-ttu-id="12ace-115">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="12ace-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="12ace-116">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="12ace-116">Instructions</span></span>

### <a name="create-a-working-area"></a><span data-ttu-id="12ace-117">Crear un área de trabajo</span><span class="sxs-lookup"><span data-stu-id="12ace-117">Create a Working Area</span></span>

<span data-ttu-id="12ace-118">En el ejemplo de código de C++ siguiente se muestra cómo crear un área de trabajo con un borde vacío de 25 píxeles en los lados superior, izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="12ace-118">The following C++ code example demonstrates how to create a working area with a 25-pixel empty border on its top, left, and right sides.</span></span>


```C++
void SetWorkAreas1(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    
    GetClientRect(hWndListView, &rcClient);
    
    rcClient.left  +=  EMPTY_SPACE;
    rcClient.top   +=  EMPTY_SPACE;
    rcClient.right -= (EMPTY_SPACE * 2);
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 1, (LPARAM)&rcClient);

    return;
}
```



### <a name="create-multiple-working-areas"></a><span data-ttu-id="12ace-119">Crear varias áreas de trabajo</span><span class="sxs-lookup"><span data-stu-id="12ace-119">Create Multiple Working Areas</span></span>

<span data-ttu-id="12ace-120">En el ejemplo de código de C++ siguiente se muestra cómo crear dos áreas de trabajo en un control.</span><span class="sxs-lookup"><span data-stu-id="12ace-120">The following C++ code example demonstrates how to create two working areas in a control.</span></span> <span data-ttu-id="12ace-121">Cada área de trabajo utiliza aproximadamente la mitad del área cliente y está rodeada por un borde vacío de 25 píxeles.</span><span class="sxs-lookup"><span data-stu-id="12ace-121">Each working area uses about half of the client area, and is surrounded by a 25-pixel empty border.</span></span>


```C++
void SetWorkAreas2(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    RECT  rcWork[2];
    
    GetClientRect(hWndListView, &rcClient);
    
    rcWork[0].left   = rcClient.left +      EMPTY_SPACE;
    rcWork[0].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[0].right  = (rcClient.right/2) - EMPTY_SPACE;
    rcWork[0].bottom = rcClient.bottom;
    
    rcWork[1].left   = (rcClient.right/2) + EMPTY_SPACE;
    rcWork[1].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[1].right  = rcClient.right -     EMPTY_SPACE;
    rcWork[1].bottom = rcClient.bottom;
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 2, (LPARAM)rcWork);

    return;
}
```



### <a name="determine-the-working-area-to-which-an-item-belongs"></a><span data-ttu-id="12ace-122">Determinar el área de trabajo a la que pertenece un elemento</span><span class="sxs-lookup"><span data-stu-id="12ace-122">Determine the Working Area to Which an Item Belongs</span></span>

<span data-ttu-id="12ace-123">Una manera de determinar el área de trabajo a la que pertenece un elemento es hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="12ace-123">One way to determine which working area an item belongs is to do the following:</span></span>

-   <span data-ttu-id="12ace-124">Recupere la lista de coordenadas de todas las áreas de trabajo en el control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="12ace-124">Retrieve the list of coordinates of all of the working areas in the list-view control.</span></span>
-   <span data-ttu-id="12ace-125">Recupera las coordenadas del elemento.</span><span class="sxs-lookup"><span data-stu-id="12ace-125">Retrieve the coordinates of the item.</span></span>
-   <span data-ttu-id="12ace-126">Determine si las coordenadas del elemento se encuentran dentro de las coordenadas de una de las áreas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="12ace-126">Determine whether the item coordinates lie within the coordinates of one of the working areas.</span></span>

<span data-ttu-id="12ace-127">La función definida por la aplicación en el siguiente ejemplo de código de C++ devuelve el índice del área de trabajo al que pertenece el elemento.</span><span class="sxs-lookup"><span data-stu-id="12ace-127">The application-defined function in the following C++ code example returns the index of the working area to which the item belongs.</span></span> <span data-ttu-id="12ace-128">Si se produce un error en la función, devuelve – 1.</span><span class="sxs-lookup"><span data-stu-id="12ace-128">If the function fails, it returns –1.</span></span> <span data-ttu-id="12ace-129">Si la función se ejecuta correctamente, pero el elemento no está dentro de ninguna de las áreas de trabajo, la función devuelve 0, porque todos los elementos que no están dentro de un área de trabajo se convierten automáticamente en un miembro del área de trabajo cero.</span><span class="sxs-lookup"><span data-stu-id="12ace-129">If the function succeeds, but the item is not inside any of the working areas, the function returns 0, because all items that are not inside a working area automatically become a member of working area zero.</span></span>


```C++
int GetItemWorkingArea(HWND hWndListView, int iItem)
{
    UINT     uWorkAreas = 0;
    int      nReturn = -1;
    LPRECT   pRects;
    POINT    pt;
    
    if(!ListView_GetItemPosition(hWndListView, iItem, &pt))
        return nReturn;
    
    ListView_GetNumberOfWorkAreas(hWndListView, &uWorkAreas);
    
    if(uWorkAreas)
    {
        pRects = (LPRECT)GlobalAlloc(GPTR, sizeof(RECT) * uWorkAreas);
        
        if(pRects)
        {
            UINT  i;
            nReturn = 0;
    
            ListView_GetWorkAreas(hWndListView, uWorkAreas, pRects);
          
            for(i = 0; i < uWorkAreas; i++)
            {
                if(PtInRect((pRects + i), pt))
                {
                    nReturn = i;
                    break;
                }
            }
            GlobalFree((HGLOBAL)pRects);
        }
    }
    return nReturn;
}

```



## <a name="related-topics"></a><span data-ttu-id="12ace-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12ace-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12ace-131">Referencia de control de vista de lista</span><span class="sxs-lookup"><span data-stu-id="12ace-131">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="12ace-132">Acerca de los controles List-View</span><span class="sxs-lookup"><span data-stu-id="12ace-132">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="12ace-133">Usar controles List-View</span><span class="sxs-lookup"><span data-stu-id="12ace-133">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




