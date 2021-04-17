---
title: Control Up-Down (referencia de elementos de interfaz de usuario de MSAA)
description: Un control de flechas, también conocido como control de número, combina un par de botones que se muestran como flechas con un control de edición de amigos. Al hacer clic en las flechas, se incrementa o disminuye el valor en el control de edición.
ms.assetid: 45e56c0f-4ac6-4731-b9a6-be4613bf40ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd2d28acc4c14a89ec73f5994ed0af47202145a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704651"
---
# <a name="up-down-control-msaa-ui-element-reference"></a>Control Up-Down (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **control** de flechas para fines de referencia de elementos de interfaz de usuario de MSAA. Aquí no se describe cómo crear objetos de **control** de flechas en varios marcos de interfaz de usuario. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Un control de flechas, también conocido como control de número, combina un par de botones que se muestran como flechas con un control de edición de amigos. Al hacer clic en las flechas, se incrementa o disminuye el valor en el control de edición.

El nombre de clase de ventana de un control de flechas es la \_ clase UpDown, que se define como "msctls \_ updown32" en commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un control de flechas admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Un control de flechas admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La propiedad **ChildCount** es "2" (los botones de flecha arriba y abajo).                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**obtener \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**obtener \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La propiedad **Name** del objeto de control de flechas se obtiene del texto (o título) de la ventana del control. Este texto no se muestra con el control de flechas, por lo que los desarrolladores del servidor deben proporcionar texto significativo en la instrucción de definición de recursos del control para ayudar a los usuarios de las utilidades de cliente a identificar el control. La propiedad de **nombre** para el botón de flecha superior del control de flechas es "más" y la propiedad de **nombre** para el botón de flecha inferior es "menor que". |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La propiedad **primaria** del control de flechas es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el control. La propiedad **primaria** de los botones de flecha arriba y abajo es el objeto de control de flechas.                                                                                                                                                    |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La propiedad de **rol** para el objeto de control de flechas es el [**\_ \_ SPINBUTTON del sistema de funciones**](object-roles.md). La propiedad **role** de los botones de flecha es botón [**\_ del sistema \_ de funciones**](object-roles.md).                                                                                                                                                                                                                          |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propiedad de estado para el objeto de control de flechas es uno de los siguientes [valores](object-state-constants.md): sistema de estado [**\_ \_ centrado**](object-state-constants.md) en el sistema de estado \| [**\_ \_**](object-state-constants.md) enfocable<br/>                                                                                                                                                                                      |
| [**obtener \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Notas

Microsoft Active Accessibility expone el control de edición de amigos como un objeto independiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





