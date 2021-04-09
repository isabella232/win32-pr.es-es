---
title: Control de calendario (referencia de elementos de interfaz de usuario de MSAA)
description: Los controles de calendario proporcionan una forma sencilla e intuitiva de que un usuario pueda seleccionar una fecha de una interfaz conocida.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63acb3ca83f6b7e71740acee4232e081e11594e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903292"
---
# <a name="calendar-control-msaa-ui-element-reference"></a>Control de calendario (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **control de calendario** para la referencia de elementos de interfaz de usuario de MSAA. La forma de crear objetos de **control de calendario** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Los controles de calendario proporcionan una forma sencilla e intuitiva de que un usuario pueda seleccionar una fecha de una interfaz conocida.

El nombre de clase de ventana de un control de calendario mensual es MONTHCAL \_ Class, que se define como "SysMonthCal32" en commctrl. h. La información de este tema se aplica al control de calendario mensual de la versión 5 de commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los controles de calendario admiten los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Los controles de calendario admiten las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La propiedad **ChildCount** es cero.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La propiedad **Name** se obtiene del control de texto estático que etiqueta el control Calendar. Al crear controles, los programadores de servidor deben asegurarse de que un control de texto estático precede inmediatamente al control que etiqueta dentro del orden de tabulación.                                                                                                                                                                                                                 |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                             |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La propiedad **role** es [**el \_ \_ cliente del sistema de roles**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                               |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md)de estado invisible del sistema de estado [**\_ \_ invisible**](object-state-constants.md) del sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) sistema enfocable \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





