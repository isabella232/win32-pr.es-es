---
title: Menú emergente (Referencia del elemento de la interfaz de usuario de MSAA)
description: Un menú emergente muestra una lista de comandos de menú.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070665"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a>Menú emergente (Referencia del elemento de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos de menú** emergente para fines de referencia de elementos de la interfaz de usuario de MSAA. Cómo crear objetos **de menú emergente en** varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Un menú emergente muestra una lista de comandos de menú. Microsoft Active Accessibility crea un objeto emergente de menú cuando se abre un elemento de menú en una barra de menús. Microsoft Active Accessibility también crea objetos emergentes de menú para menús contextuales, que se muestran cuando el usuario hace clic con el botón derecho en un elemento de la interfaz de usuario.

El nombre de clase de ventana de un menú emergente es \# "32768".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un menú emergente admite los siguientes métodos [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Un menú emergente admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Recupera el [**IDispatch para**](idispatch-interface.md) el elemento de menú especificado. Los identificaciónes secundarios de los elementos de menú se numeran secuencialmente de arriba abajo a partir de uno.                                                                                                                                                                                                                                                                                      |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La **propiedad ChildCount** es el número de elementos de menú del menú, incluidos los separadores de menú.                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La **propiedad** Nombre de un menú emergente tiene el mismo nombre que el menú. La **propiedad** Name de un menú contextual es "Context".                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La **propiedad** Parent es una ventana [**(ROLE \_ SYSTEM \_ WINDOW)**](object-roles.md) que rodea  el menú emergente y tiene la misma propiedad Nombre y el mismo nombre de clase de ventana que el menú emergente .                                                                                                                                                                                                                                                      |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La **propiedad Role** es ROLE SYSTEM [**\_ \_ MENUPOPUP.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ FOCUSED**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notas

-   Los objetos de menú emergente no desencadenan [**eventos EVENT \_ OBJECT \_ CREATE**](event-constants.md) [**y EVENT OBJECT \_ \_ DESTROY.**](event-constants.md)
-   Los menús de varias columnas no admiten las marcas [**NAVDIR \_ LEFT**](navigation-constants.md) o [**NAVDIR \_ RIGHT**](navigation-constants.md) del [**método accNavigate.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   Los eventos [**EVENT \_ SYSTEM \_ MENUPOPUPSTART**](event-constants.md) y [**EVENT SYSTEM \_ \_ MENUPOPUPEND**](event-constants.md) no se envían de forma coherente. Se trata de un problema conocido que se está abordando.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra de menús**](menu-bar.md)
</dt> <dt>

[**Elemento de menú**](menu-item.md)
</dt> </dl>

 

 





