---
title: Texto estático (referencia de elementos de interfaz de usuario de MSAA)
description: Los controles de texto estático proporcionan una manera cómoda de mostrar texto en los cuadros de diálogo y en otras ventanas. Los controles de texto estáticos suelen servir como etiquetas para otros controles.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f35581a9b305f28782d8faeac81105afb0d5147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903831"
---
# <a name="static-text-msaa-ui-element-reference"></a>Texto estático (referencia de elementos de interfaz de usuario de MSAA)

Los controles de texto estático proporcionan una manera cómoda de mostrar texto en los cuadros de diálogo y en otras ventanas. Los controles de texto estáticos suelen servir como etiquetas para otros controles.

El nombre de clase de ventana de un control de texto estático es "STATIC".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los controles de texto estático admiten los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Los controles de texto estático admiten las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propiedad **ChildCount** es cero.                                                                                                                                                                                                                                                          |
| [**obtener \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [**obtener \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [**obtener \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propiedad **KeyboardShortcut** es la tecla de acceso, que es el carácter subrayado del texto que activa el control asociado al texto estático. La cadena devuelta contiene el carácter de tecla de acceso anexado a la cadena "Alt +".                                           |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propiedad **Name** es igual que el texto del control de texto estático.                                                                                                                                                                                                                     |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el control.                                                                                   |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propiedad **role** es [**\_ \_ STATICTEXT del sistema de roles**](object-roles.md).                                                                                                                                                                                             |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): sistema de estado de [**\_ \_ solo lectura**](object-state-constants.md) sistema de estado \| [**\_ \_ invisible**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notas

-   El método [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) devuelve el \_ \_ MEMBERNOTFOUND cuando se llama con [**SELFLAG \_ TAKEFOCUS**](selflag.md) en un objeto de texto estático.
-   Los controles estáticos con el \_ estilo de icono SS devuelven datos no válidos en la propiedad **Name** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





