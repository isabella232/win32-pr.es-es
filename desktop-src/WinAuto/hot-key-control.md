---
title: Control de teclas de acceso rápido (referencia de elementos de interfaz de usuario de MSAA)
description: Los controles de tecla de acceso rápido permiten a los usuarios escribir una combinación de pulsaciones de teclas usadas como tecla de acceso rápido, lo que les permite realizar una acción rápidamente. Un control de tecla de acceso rápido muestra las pulsaciones de teclas especificadas por el usuario y garantiza que el usuario selecciona una combinación de teclas válida.
ms.assetid: 56c9fee4-f3d3-4f61-8587-bf80186aa5b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aed12ce64fe25c091f6204d9143a0c6ebefb65a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357462"
---
# <a name="hot-key-control-msaa-ui-element-reference"></a>Control de teclas de acceso rápido (referencia de elementos de interfaz de usuario de MSAA)

Los controles de tecla de acceso rápido permiten a los usuarios escribir una combinación de pulsaciones de teclas usadas como tecla de acceso rápido, lo que les permite realizar una acción rápidamente. Un control de tecla de acceso rápido muestra las pulsaciones de teclas especificadas por el usuario y garantiza que el usuario selecciona una combinación de teclas válida.

El nombre de clase de ventana de un control de tecla de acceso rápido es la \_ clase Hotkey, que se define como "msctls \_ hotkey32" en commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los controles de tecla de acceso rápido admiten los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Los controles de tecla de acceso rápido admiten las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propiedad **ChildCount** siempre es cero.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propiedad **KeyboardShortcut** es la tecla de acceso del control de teclas de acceso rápido, que es un carácter subrayado en el texto de la etiqueta del control de tecla de acceso rápido. La cadena devuelta contiene el carácter de tecla de acceso anexado a la cadena "Alt +".                                                                                                                                                                                                                                 |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propiedad **Name** es el texto de un control de texto estático que etiqueta el control de tecla de acceso rápido.                                                                                                                                                                                                                                                                                                                                                                            |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                              |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propiedad **role** es [**\_ \_ HOTKEYFIELD del sistema de roles**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                      |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md):[**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable<br/> |
| [**obtener \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La propiedad **Value** es una cadena que contiene el texto del campo de tecla de acceso rápido.                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





