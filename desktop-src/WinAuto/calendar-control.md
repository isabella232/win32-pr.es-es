---
title: Control Calendar (Referencia de elementos de la interfaz de usuario de MSAA)
description: Los controles de calendario proporcionan una manera sencilla e intuitiva para que un usuario seleccione una fecha de una interfaz conocida.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f41daf9e86f178f4b22a7908e4d9d10d1dab1a2f867ca2d09c62d111cbc806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899565"
---
# <a name="calendar-control-msaa-ui-element-reference"></a>Control Calendar (Referencia de elementos de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos de control** de calendario para fines de referencia de elementos de la interfaz de usuario de MSAA. Aquí no se describe **cómo crear objetos de control** de calendario en varios marcos de interfaz de usuario. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Los controles de calendario proporcionan una manera sencilla e intuitiva para que un usuario seleccione una fecha de una interfaz conocida.

El nombre de clase de ventana para un control de calendario mensual es MONTHCAL CLASS, que se define como \_ "SysMonthCal32" en Commctrl.h. La información de este tema se aplica al control de calendario mensual de la versión 5 de Commctrl.h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los controles de calendario admiten los [**siguientes métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Los controles de calendario admiten las [**siguientes propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La **propiedad ChildCount** es cero.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La **propiedad Name** se obtiene del control de texto estático que etiqueta el control de calendario. Al crear controles, los desarrolladores de servidores deben asegurarse de que un control de texto estático precede inmediatamente al control que etiqueta dentro del orden de tabulación.                                                                                                                                                                                                                 |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La **propiedad Parent** es una ventana ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) que rodea el control y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                             |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La **propiedad Role** es ROLE SYSTEM [**\_ \_ CLIENT.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La **propiedad State** es una combinación de [](object-state-constants.md)uno o varios de los valores siguientes STATE [**SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| FOCUSED STATE SYSTEM [**\_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





