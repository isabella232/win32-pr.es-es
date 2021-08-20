---
title: Editar control (referencia de elemento de la interfaz de usuario de MSAA)
description: Los controles de edición permiten a un usuario ver y editar texto.
ms.assetid: a42c73f2-4005-4db9-84bc-637c9c4310f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3844dcdf99f925813765ae46494b0ff70345c086f3845304fff0e53d70f07d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829849"
---
# <a name="edit-control-msaa-ui-element-reference"></a>Editar control (referencia de elemento de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos Edit Control** para fines de referencia de elementos de la interfaz de usuario de MSAA. Aquí no se describe **cómo crear objetos de control** de edición en varios marcos de interfaz de usuario. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Los controles de edición permiten a un usuario ver y editar texto. Los controles de edición se crean con muchos estilos diferentes, como ES \_ MULTILINE. Este estilo crea un control de edición multilínea, como el área de cliente de Bloc de notas, y ES READONLY, que crea un control de edición \_ de solo lectura.

Microsoft Active Accessibility hace una distinción entre los controles de edición creados con el nombre de clase de ventana "EDIT" y los controles de edición enriquecidos creados con el nombre de clase de ventana "RichEdit" o "RichEdit20A".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los controles Edit admiten los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Los controles De edición admiten las [**siguientes propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **propiedad KeyboardShortcut** es la tecla de acceso del control de edición, que es un carácter subrayado en el texto de la etiqueta del control de edición. Por ejemplo, en un cuadro de diálogo Estándar Abrir archivo, como en WordPad, **keyboardShortcut** para el control de edición con la etiqueta "Filename:" es "Alt+n".                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **propiedad Name** es el texto de un control de texto estático que etiqueta el control de edición. Por ejemplo, en un cuadro de diálogo Estándar Abrir archivo, como en WordPad, la propiedad **Nombre** del control de edición es "Nombre de archivo:".                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **propiedad Parent** es una ventana ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) que rodea el control y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **propiedad Role** es ROLE SYSTEM [**\_ \_ TEXT.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| FOCUSABLE STATE SYSTEM [**\_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ READONLY**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ PROTECTED**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ NORMAL**](object-state-constants.md)<br/> |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La **propiedad Value** es una sola cadena que contiene el texto del control de edición. Sin embargo, si el control está protegido con contraseña, la **propiedad Value** devuelve E \_ ACCESSDENIED. Para los controles de edición multilínea, la cadena contiene un retorno de carro y un carácter de nueva línea al final de cada línea.                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Notas

-   Microsoft Active Accessibility no admite la selección del texto contenido en los controles de edición y edición enriquezca porque el texto se expone como una cadena en la propiedad **Value del** objeto.
-   El control de edición enriquecido proporcionado por Riched20.dll (que se usa en editores de texto como WordPad en Windows 98) no envía ningún WinEvents cuando se cambia la posición del cursor de cursor durante la selección de texto. Cuando los usuarios presionan MAYÚS y las teclas de dirección para seleccionar texto, el objeto de cursor no desencadena [**el evento EVENT OBJECT \_ \_ LOCATIONCHANGE**](event-constants.md) WinEvent. Cuando la selección se establece mediante programación a través de mensajes de edición enriquecidos, el objeto de cursor no envía ningún evento para indicar su nueva posición.

    Todas las aplicaciones que usan Riched20.dll muestran este problema. Las aplicaciones que usan versiones anteriores del control rich edit envían correctamente eventos en función de la selección.

-   El **valor Estado** de los controles de edición de contraseñas siempre incluye la marca de bits STATE SYSTEM [**\_ \_ PROTECTED**](object-state-constants.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





