---
title: Usar dibujo personalizado
description: Esta sección contiene ejemplos que muestran cómo implementar el dibujo personalizado.
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0b8a2585103aa27a27f0138a49885cc726d3b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165342"
---
# <a name="using-custom-draw"></a>Usar dibujo personalizado

Esta sección contiene ejemplos que muestran cómo implementar el dibujo personalizado.

El fragmento de código siguiente es una parte de un controlador [**WM \_ NOTIFY**](wm-notify.md) que muestra cómo controlar las notificaciones de dibujo personalizadas enviadas a un control de vista de lista.


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



La primera [notificación \_ NM CUSTOMDRAW](nm-customdraw.md) tiene el **miembro dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) establecido en **CDDS \_ PREPAINT**. El controlador devuelve [**CDRF \_ NOTIFYITEMDRAW para**](cdrf-constants.md) indicar que desea modificar uno o varios elementos individualmente.

Si [**se devolvió \_ CDRF NOTIFYITEMDRAW**](cdrf-constants.md) en el paso anterior, la siguiente notificación [NM \_ CUSTOMDRAW](nm-customdraw.md) tiene **dwDrawStage** establecido en **CDDS \_ ITEMPREPAINT**. El controlador recupera los valores de color y fuente actuales. En este punto, puede especificar nuevos valores para los modos de icono pequeño, icono grande y lista. Si el control está en modo de informe, también puede especificar nuevos valores que se aplicarán a todos los subelementos del elemento. Si ha cambiado algo, devuelva [**CDRF \_ NEWFONT**](cdrf-constants.md). Si el control está en modo de informe y desea controlar los subelementos individualmente, devuelva **CDRF \_ NOTIFYSUBITEMDRAW**.

La notificación final solo se envía si el control está en modo de informe y devolvió **CDRF \_ NOTIFYSUBITEMDRAW** en el paso anterior. El procedimiento para cambiar las fuentes y los colores es el mismo que en ese paso, pero solo se aplica a un subelemento único. Devuelve [**CDRF \_ NEWFONT para**](cdrf-constants.md) notificar al control si se ha cambiado el color o la fuente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Acerca del dibujo personalizado](about-custom-draw.md)
</dt> <dt>

[Referencia de dibujo personalizado](custom-draw-reference.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[EJEMPLO: CustDTv ilustra el dibujo personalizado en treeview (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




