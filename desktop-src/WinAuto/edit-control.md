---
title: Control de edición (referencia de elementos de interfaz de usuario de MSAA)
description: Los controles de edición permiten a un usuario ver y editar texto.
ms.assetid: a42c73f2-4005-4db9-84bc-637c9c4310f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dde6e562b651b91376bc7d675b2b71ac999cf48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532482"
---
# <a name="edit-control-msaa-ui-element-reference"></a>Control de edición (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **control de edición** para la referencia de elementos de interfaz de usuario de MSAA. La forma de crear objetos de **control de edición** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Los controles de edición permiten a un usuario ver y editar texto. Los controles de edición se crean con muchos estilos diferentes como ES \_ multilínea. Este estilo crea un control de edición multilínea, como el área cliente del Bloc de notas y ES \_ ReadOnly, que crea un control de edición de solo lectura.

Microsoft Active Accessibility no realiza una distinción entre los controles de edición creados con el nombre de clase de ventana "EDIT" y los controles Rich Edit creados con el nombre de clase de ventana "RichEdit" o "RichEdit20A".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los controles de edición admiten los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Los controles de edición admiten las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**obtener \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propiedad **KeyboardShortcut** es la tecla de acceso del control de edición, que es un carácter subrayado en el texto de la etiqueta del control de edición. Por ejemplo, en un cuadro de diálogo Abrir archivo estándar, como en WordPad, el **KeyboardShortcut** del control de edición con la etiqueta "Filename:" es "Alt + n".                                                                                                                                                                                                                                                                                                                                        |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propiedad **Name** es el texto de un control de texto estático que etiqueta el control de edición. Por ejemplo, en un cuadro de diálogo Abrir archivo estándar, como en WordPad, la propiedad **nombre** del control de edición es "nombre de archivo:".                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propiedad **role** es [**el \_ \_ texto del sistema de roles**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obtener \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md):[**sistema de estado \_ \_ invisible**](object-state-constants.md) sistema de estado de \| [**\_ \_ foco**](object-state-constants.md) de sistema de estado sistema de estado de \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ solo lectura**](object-state-constants.md) sistema estado de sistema \| [**\_ \_ protegido**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)<br/> |
| [**obtener \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La propiedad **Value** es una sola cadena que contiene el texto del control de edición. Sin embargo, si el control está protegido por contraseña, la propiedad **Value** devuelve E \_ ACCESSDENIED. En el caso de los controles de edición multilínea, la cadena contiene un retorno de carro y un carácter de nueva línea al final de cada línea.                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Notas

-   Microsoft Active Accessibility no admite la selección del texto contenido en los controles de edición y edición enriquecida porque el texto se expone como una cadena en la propiedad **Value** del objeto.
-   El control Rich Edit proporcionado por Riched20.dll (que se usa en los editores de texto como WordPad en Windows 98) no envía ningún WinEvents cuando se cambia la posición del símbolo de intercalación durante la selección de texto. Cuando los usuarios presionan Mayús y las teclas de dirección para seleccionar texto, el objeto de símbolo de intercalación no desencadena el [**objeto de evento \_ \_ LOCATIONCHANGE**](event-constants.md) WinEvent. Cuando la selección se establece mediante programación a través de mensajes Rich Edit, el objeto de símbolo de intercalación no envía ningún evento para indicar su nueva posición.

    Todas las aplicaciones que usan Riched20.dll muestran este problema. Las aplicaciones que usan versiones anteriores del control Rich Edit envían correctamente los eventos en función de la selección.

-   El valor de **Estado** de los controles de edición de contraseñas incluye siempre el estado de marca de bits [**\_ \_ protegido**](object-state-constants.md)por el sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





