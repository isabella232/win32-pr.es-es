---
title: Control ToolTip (Referencia del elemento de interfaz de usuario de MSAA)
description: Un control de información sobre herramientas muestra una pequeña ventana emergente que contiene una línea de texto que describe el propósito de una herramienta, representada como un objeto gráfico, en una aplicación.
ms.assetid: d3a65d7b-b882-4a1a-bac2-6995b64cf4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37557fd116084fc9ac53e8567afc90eda339750d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070597"
---
# <a name="tooltip-control-msaa-ui-element-reference"></a>Control ToolTip (Referencia del elemento de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos de control de información** sobre herramientas para fines de referencia de elementos de interfaz de usuario de MSAA. Aquí no se describe cómo crear objetos **de control** de información sobre herramientas en varios marcos de interfaz de usuario. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Un control de información sobre herramientas muestra una pequeña ventana emergente que contiene una línea de texto que describe el propósito de una herramienta, representada como un objeto gráfico, en una aplicación.

El nombre de clase de ventana para una información sobre herramientas es TOOLTIPS CLASS, que se define como "clase de información sobre \_ \_ herramientas" en Commctrl.h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un control de información sobre herramientas admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Un control de información sobre herramientas admite las [**siguientes propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La **propiedad ChildCount** es cero.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La **propiedad Name** es el texto contenido en el control de información sobre herramientas.                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La **propiedad Parent** es una ventana ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) que rodea el control y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                               |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La **propiedad Role** es ROLE SYSTEM [**\_ \_ TOOLTIP**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| FOCUSED STATE SYSTEM [**\_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





