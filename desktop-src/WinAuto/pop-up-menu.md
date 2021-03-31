---
title: Menú emergente (referencia de elementos de interfaz de usuario de MSAA)
description: Un menú emergente muestra una lista de comandos de menú.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903650"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a>Menú emergente (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **menú emergente** a efectos de la referencia de elementos de la interfaz de usuario de MSAA. La forma de crear objetos de **menú emergente** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Un menú emergente muestra una lista de comandos de menú. Microsoft Active Accessibility crea un objeto emergente de menú cuando se abre un elemento de menú en una barra de menús. Microsoft Active Accessibility también crea objetos emergentes de menú para los menús contextuales, que se muestran cuando el usuario hace clic con el botón secundario en un elemento de la interfaz de usuario.

El nombre de la clase de ventana de un menú emergente es " \# 32768".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un menú emergente admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Un menú emergente admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Recupera [**IDispatch**](idispatch-interface.md) para el elemento de menú especificado. Los identificadores secundarios de los elementos de menú se numeran secuencialmente de arriba abajo a partir de uno.                                                                                                                                                                                                                                                                                      |
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La propiedad **ChildCount** es el número de elementos de menú en el menú, incluidos los separadores de menús.                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La propiedad **nombre** de un menú emergente es el mismo nombre que el menú. La propiedad **Name** de un menú contextual es "context".                                                                                                                                                                                                                                                                                                                                              |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el menú emergente y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el menú emergente.                                                                                                                                                                                                                                                      |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La propiedad **role** es [**\_ \_ MENUPOPUP del sistema de roles**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): [**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable<br/> |



 

## <a name="notes"></a>Notas

-   Los objetos de menú emergente no desencadenan eventos de [**\_ \_ creación**](event-constants.md) y [**\_ \_ destrucción**](event-constants.md) de objetos de eventos.
-   Los menús de varias columnas no admiten las marcas [**NAVDIR \_ left**](navigation-constants.md) o [**NAVDIR \_ right**](navigation-constants.md) del método [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) .
-   Los eventos [**Event \_ System \_ MENUPOPUPSTART**](event-constants.md) y [**Event \_ System \_ MENUPOPUPEND**](event-constants.md) no se envían de forma coherente. Se trata de un problema conocido y se está solucionando.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra de menús**](menu-bar.md)
</dt> <dt>

[**Elemento de menú**](menu-item.md)
</dt> </dl>

 

 





