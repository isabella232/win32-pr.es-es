---
title: Control de barra de estado (referencia de elementos de interfaz de usuario de MSAA)
description: Las barras de estado muestran información de estado en una ventana horizontal en la parte inferior de una ventana de la aplicación.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81bddf2898b9b7eca5385d86d6dabc6a50d3d4df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357661"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a>Control de barra de estado (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **control de barra de estado** para fines de referencia de elementos de interfaz de usuario de MSAA. La forma de crear objetos de **control de barra de estado** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Las barras de estado muestran información de estado en una ventana horizontal en la parte inferior de una ventana de la aplicación. Las barras de Estado suelen dividirse en partes, denominadas paneles, y cada panel muestra información de estado diferente. Además, las barras de estado pueden contener objetos de diferentes tipos, incluidos botones y barras de progreso. El nombre de clase de ventana de un control de barra de estado es STATUSCLASSNAME, que se define como "msctls \_ statusbar32" en commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Las barras de estado admiten los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Las barras de estado admiten las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La propiedad **ChildCount** es el número de paneles de la barra de estado.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | El propio objeto de barra de estado no tiene una propiedad **nombre** . La propiedad **nombre** de cada panel de la barra de estado es igual que el texto mostrado.                                                                                                                                                                                                                                                                                                                   |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La propiedad **primaria** del objeto de barra de estado es una ventana [**( \_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene el mismo nombre de clase de ventana que el control. La propiedad **primaria** de los paneles en la barra de estado es el objeto de barra de estado.                                                                                                                                                                           |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La propiedad de **rol** para el propio objeto de barra de estado es la barra de estado [**\_ del sistema \_ de roles**](object-roles.md). El texto que se muestra en una barra de Estado tiene el [**\_ sistema de \_ STATICTEXT de rol**](object-roles.md) como su propiedad de **rol** .                                                                                                                                                                                                 |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): [**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable<br/> |



 

## <a name="notes"></a>Notas

Dado que los métodos abreviados de teclado no se admiten para los controles de barra de estado o las áreas de texto en las barras de estado, no se admite [**Get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





