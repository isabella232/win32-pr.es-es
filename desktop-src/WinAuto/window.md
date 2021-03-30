---
title: Window (referencia de elementos de interfaz de usuario de MSAA)
description: Microsoft Active Accessibility crea un objeto de ventana genérico como contenedor para otro objeto. Los desarrolladores de cliente no transmiten la información de los objetos de ventana a los usuarios finales porque estos objetos no contienen información útil.
ms.assetid: cc32528f-c454-4522-91b9-06f87cff8bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87c8601ecd6344dc82bbdb416055c694687e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774808"
---
# <a name="window-msaa-ui-element-reference"></a>Window (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **ventana** para la referencia de elementos de interfaz de usuario de MSAA. La forma de crear objetos de **ventana** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Microsoft Active Accessibility crea un objeto de ventana genérico como contenedor para otro objeto. Los desarrolladores de cliente no transmiten la información de los objetos de ventana a los usuarios finales porque estos objetos no contienen información útil.

Si una aplicación de servidor crea un control personalizado, Microsoft Active Accessibility crea un objeto de ventana que contiene el control personalizado, pero el servidor crea un objeto accesible para proporcionar información sobre el contenido del control. El sistema genera eventos de nivel de objeto para el objeto Window, pero el servidor debe enviar eventos para el objeto accesible que proporciona información sobre el control.

## <a name="iaccessible-methods"></a>Métodos IAccessible

El objeto Window admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

El objeto Window admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera la interfaz [IDispatch](idispatch-interface.md) del elemento secundario especificado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propiedad **ChildCount** es 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**obtener \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | El propio objeto Window no tiene una propiedad **Description** . La propiedad **Description** del objeto secundario se puede recuperar a través del objeto Window.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | El propio objeto Window no tiene una propiedad **KeyboardShortcut** . La propiedad **KeyboardShortcut** del objeto secundario se recupera a través del objeto Window.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propiedad **Name** del objeto Window es igual que el objeto secundario.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propiedad **role** es [**la \_ \_ ventana del sistema de roles**](object-roles.md). El **rol** del objeto secundario se recupera a través del objeto Window.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): [**estado \_ \_ invisible**](object-state-constants.md) del sistema de estado no disponible del sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) \| [**sistema \_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) de \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) estado de reactivación sistema centrado<br/> |



 

## <a name="notes"></a>Notas

El objeto de ventana no envía los eventos [**\_ \_ DRAGDROPSTART**](event-constants.md), Event [**\_ System \_ DRAGDROPEND**](event-constants.md)y Event Event [**\_ \_ Hide**](event-constants.md)y [**\_ \_ PARENTCHANGE de objeto de evento**](event-constants.md) . Se trata de un problema conocido y se está solucionando.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





