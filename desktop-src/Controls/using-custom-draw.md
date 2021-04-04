---
title: Usar Draw personalizado
description: Esta sección contiene ejemplos que muestran cómo implementar Draw personalizado.
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0b8a2585103aa27a27f0138a49885cc726d3b1
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104077374"
---
# <a name="using-custom-draw"></a><span data-ttu-id="6763d-103">Usar Draw personalizado</span><span class="sxs-lookup"><span data-stu-id="6763d-103">Using Custom Draw</span></span>

<span data-ttu-id="6763d-104">Esta sección contiene ejemplos que muestran cómo implementar Draw personalizado.</span><span class="sxs-lookup"><span data-stu-id="6763d-104">This section contains examples that demonstrate how to implement custom draw.</span></span>

<span data-ttu-id="6763d-105">El siguiente fragmento de código es una parte de un controlador de [**\_ notificaciones de WM**](wm-notify.md) que muestra cómo controlar las notificaciones de dibujo personalizadas enviadas a un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="6763d-105">The following code fragment is a portion of a [**WM\_NOTIFY**](wm-notify.md) handler that illustrates how to handle custom draw notifications sent to a list-view control.</span></span>


```C++
        
LPNMLISTVIEW  pnm  = (LPNMLISTVIEW)lParam;

switch (pnm->hdr.code){
...
case NM_CUSTOMDRAW:

    LPNMLVCUSTOMDRAW  lplvcd = (LPNMLVCUSTOMDRAW)lParam;

    switch(lplvcd->nmcd.dwDrawStage) {

    case CDDS_PREPAINT :
        return CDRF_NOTIFYITEMDRAW;

    case CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForItem(lplvcd->nmcd.dwItemSpec,
                                    lplvcd->nmcd.lItemlParam) );
        lplvcd->clrText = GetColorForItem(lplvcd->nmcd.dwItemSpec,
                                          lplvcd->nmcd.lItemlParam);
        lplvcd->clrTextBk = GetBkColorForItem(lplvcd->nmcd.dwItemSpec,
                                              lplvcd->nmcd.lItemlParam);

/* At this point, you can change the background colors for the item
and any subitems and return CDRF_NEWFONT. If the list-view control
is in report mode, you can simply return CDRF_NOTIFYSUBITEMDRAW
to customize the item's subitems individually */
        ...

        return CDRF_NEWFONT;
    //  or return CDRF_NOTIFYSUBITEMDRAW;

    case CDDS_SUBITEM | CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForSubItem(lplvcd->nmcd.dwItemSpec,
                                       lplvcd->nmcd.lItemlParam,
                                       lplvcd->iSubItem));
        lplvcd->clrText = GetColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                             lplvcd->nmcd.lItemlParam,
                                             lplvcd->iSubItem));
        lplvcd->clrTextBk = GetBkColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                                 lplvcd->nmcd.lItemlParam,
                                                 lplvcd->iSubItem));

/* This notification is received only if you are in report mode and
returned CDRF_NOTIFYSUBITEMDRAW in the previous step. At
this point, you can change the background colors for the
subitem and return CDRF_NEWFONT.*/
        ...
        return CDRF_NEWFONT;    
    }
...
}
        
```



<span data-ttu-id="6763d-106">La primera [notificación \_ CUSTOMDRAW de nm](nm-customdraw.md) tiene el miembro **DwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) establecida en **CDDS \_ PREPAINT**.</span><span class="sxs-lookup"><span data-stu-id="6763d-106">The first [NM\_CUSTOMDRAW](nm-customdraw.md) notification has the **dwDrawStage** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure set to **CDDS\_PREPAINT**.</span></span> <span data-ttu-id="6763d-107">El controlador devuelve [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) para indicar que desea modificar uno o más elementos de forma individual.</span><span class="sxs-lookup"><span data-stu-id="6763d-107">The handler returns [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) to indicate that it wishes to modify one or more items individually.</span></span>

<span data-ttu-id="6763d-108">Si [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) se devolvió en el paso anterior, la siguiente notificación de [ \_ CUSTOMDRAW nm](nm-customdraw.md) tiene **dwDrawStage** establecido en **CDDS \_ ITEMPREPAINT**.</span><span class="sxs-lookup"><span data-stu-id="6763d-108">If [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) was returned in the previous step, the next [NM\_CUSTOMDRAW](nm-customdraw.md) notification has **dwDrawStage** set to **CDDS\_ITEMPREPAINT**.</span></span> <span data-ttu-id="6763d-109">El controlador recupera los valores de fuente y color actuales.</span><span class="sxs-lookup"><span data-stu-id="6763d-109">The handler retrieves the current color and font values.</span></span> <span data-ttu-id="6763d-110">Llegados a este punto, puede especificar nuevos valores para los modos de iconos pequeños, iconos grandes y listas.</span><span class="sxs-lookup"><span data-stu-id="6763d-110">At this point, you can specify new values for small icon, large icon, and list modes.</span></span> <span data-ttu-id="6763d-111">Si el control está en modo de informe, también puede especificar nuevos valores que se aplicarán a todos los subelementos del elemento.</span><span class="sxs-lookup"><span data-stu-id="6763d-111">If the control is in report mode, you can also specify new values that will apply to all subitems of the item.</span></span> <span data-ttu-id="6763d-112">Si ha cambiado algo, devuelva [**CDRF \_ NEWFONT**](cdrf-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6763d-112">If you have changed anything, return [**CDRF\_NEWFONT**](cdrf-constants.md).</span></span> <span data-ttu-id="6763d-113">Si el control está en modo de informe y desea controlar los subelementos individualmente, devuelva **CDRF \_ NOTIFYSUBITEMDRAW**.</span><span class="sxs-lookup"><span data-stu-id="6763d-113">If the control is in report mode and you want to handle the subitems individually, return **CDRF\_NOTIFYSUBITEMDRAW**.</span></span>

<span data-ttu-id="6763d-114">La notificación final solo se envía si el control está en modo de informe y ha devuelto **CDRF \_ NOTIFYSUBITEMDRAW** en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="6763d-114">The final notification is only sent if the control is in report mode and you returned **CDRF\_NOTIFYSUBITEMDRAW** in the previous step.</span></span> <span data-ttu-id="6763d-115">El procedimiento para cambiar fuentes y colores es el mismo que el paso, pero solo se aplica a un único subelemento.</span><span class="sxs-lookup"><span data-stu-id="6763d-115">The procedure for changing fonts and colors is the same as that step, but it only applies to a single subitem.</span></span> <span data-ttu-id="6763d-116">Devuelve [**CDRF \_ NEWFONT**](cdrf-constants.md) para notificar al control si se cambió el color o la fuente.</span><span class="sxs-lookup"><span data-stu-id="6763d-116">Return [**CDRF\_NEWFONT**](cdrf-constants.md) to notify the control if the color or font was changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6763d-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6763d-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6763d-118">**Vista**</span><span class="sxs-lookup"><span data-stu-id="6763d-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6763d-119">Acerca de Draw personalizado</span><span class="sxs-lookup"><span data-stu-id="6763d-119">About Custom Draw</span></span>](about-custom-draw.md)
</dt> <dt>

[<span data-ttu-id="6763d-120">Referencia de dibujo personalizada</span><span class="sxs-lookup"><span data-stu-id="6763d-120">Custom Draw Reference</span></span>](custom-draw-reference.md)
</dt> <dt>

<span data-ttu-id="6763d-121">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="6763d-121">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6763d-122">EJEMPLO: CustDTv ilustra el dibujo personalizado en una vista de árbol (Q248496)</span><span class="sxs-lookup"><span data-stu-id="6763d-122">SAMPLE: CustDTv Illustrates Custom Draw in a TreeView (Q248496)</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




