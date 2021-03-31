---
title: Cómo agregar un elemento a un control de encabezado
description: En este tema se muestra cómo agregar un elemento a un control de encabezado.
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cf020c95a9dfe06bb06370533fdfd9416ddfef
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995757"
---
# <a name="how-to-add-an-item-to-a-header-control"></a><span data-ttu-id="92ad1-103">Cómo agregar un elemento a un control de encabezado</span><span class="sxs-lookup"><span data-stu-id="92ad1-103">How to Add an Item to a Header Control</span></span>

<span data-ttu-id="92ad1-104">En este tema se muestra cómo agregar un elemento a un control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="92ad1-104">This topic demonstrates how to add an item to a header control.</span></span> <span data-ttu-id="92ad1-105">Normalmente, un control de encabezado tiene varios elementos de encabezado que definen las columnas del control.</span><span class="sxs-lookup"><span data-stu-id="92ad1-105">A header control typically has several header items that define the columns of the control.</span></span> <span data-ttu-id="92ad1-106">Puede Agregar un elemento a un control de encabezado enviando el mensaje de [**HDM \_ INSERTITEM**](hdm-insertitem.md) al control.</span><span class="sxs-lookup"><span data-stu-id="92ad1-106">You can add an item to a header control by sending the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="92ad1-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="92ad1-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="92ad1-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="92ad1-108">Technologies</span></span>

-   [<span data-ttu-id="92ad1-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="92ad1-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="92ad1-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="92ad1-110">Prerequisites</span></span>

-   <span data-ttu-id="92ad1-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="92ad1-111">C/C++</span></span>
-   <span data-ttu-id="92ad1-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="92ad1-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="92ad1-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="92ad1-113">Instructions</span></span>


<span data-ttu-id="92ad1-114">Use el mensaje [**HDM \_ INSERTITEM**](hdm-insertitem.md) para agregar un elemento al control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="92ad1-114">Use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to add an item to the header control.</span></span> <span data-ttu-id="92ad1-115">El mensaje debe incluir la dirección de una estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) .</span><span class="sxs-lookup"><span data-stu-id="92ad1-115">The message must include the address of an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="92ad1-116">Esta estructura define las propiedades del elemento de encabezado, que puede incluir una cadena, una imagen de mapa de bits, un tamaño inicial y un valor de bit 32 definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="92ad1-116">This structure defines the properties of the header item, which can include a string, a bitmapped image, an initial size, and an application-defined 32-bit value.</span></span>

<span data-ttu-id="92ad1-117">En el ejemplo siguiente se muestra cómo usar el mensaje [**HDM \_ INSERTITEM**](hdm-insertitem.md) y la estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) para agregar un elemento a un control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="92ad1-117">The following example illustrates how to use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message and the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure to add an item to a header control.</span></span> <span data-ttu-id="92ad1-118">El nuevo elemento se compone de una cadena justificada a la izquierda en el rectángulo del elemento.</span><span class="sxs-lookup"><span data-stu-id="92ad1-118">The new item consists of a string that is left-justified within the item rectangle.</span></span>



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a><span data-ttu-id="92ad1-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92ad1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92ad1-120">Acerca de los controles de encabezado</span><span class="sxs-lookup"><span data-stu-id="92ad1-120">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="92ad1-121">Referencia de control de encabezado</span><span class="sxs-lookup"><span data-stu-id="92ad1-121">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="92ad1-122">Usar controles de encabezado</span><span class="sxs-lookup"><span data-stu-id="92ad1-122">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 




