---
title: Control Animation (referencia de elementos de interfaz de usuario de MSAA)
description: Los controles de animación muestran un clip de audio de vídeo intercalado (AVI) en modo silencioso. Normalmente, los controles de animación se muestran cuando se copian archivos o cuando se realiza otra tarea que consume mucho tiempo.
ms.assetid: 2a31d4ba-a1bd-478b-86a9-726fa93ab714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ca7cf7e4b8a2174dae81b1770b2d877f749502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776230"
---
# <a name="animation-control-msaa-ui-element-reference"></a>Control Animation (referencia de elementos de interfaz de usuario de MSAA)

Los controles de animación muestran un clip de audio de vídeo intercalado (AVI) en modo silencioso. Normalmente, los controles de animación se muestran cuando se copian archivos o cuando se realiza otra tarea que consume mucho tiempo.

El nombre de clase de ventana de un control de animación es ANIMAte \_ Class, que se define como "SysAnimate32" en commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los controles de animación admiten los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Los controles de animación admiten las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propiedad **ChildCount** es cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Los controles de animación no tienen métodos abreviados de teclado. Sin embargo, si la etiqueta del control contiene una tecla de acceso (un carácter subrayado en el texto de la etiqueta del control), [**Get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) devuelve una cadena que no es NULL. Esta cadena contiene el carácter de tecla de acceso anexado a la cadena "Alt +". Por ejemplo, si la etiqueta es "downloading files", **KeyboardShortcut** es "Alt + d".                                                                                        |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propiedad **Name** se obtiene del control de texto estático que etiqueta el control Animation. Al crear controles, los programadores de servidor deben asegurarse de que un control de texto estático precede inmediatamente al control que etiqueta dentro del orden de tabulación.                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propiedad **role** es [**la \_ \_ animación del sistema de roles**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propiedad **Estado** es una combinación de una o varias de las siguientes constantes de estado de objeto: sistema de estado [**\_ \_ invisible**](object-state-constants.md) sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) sistema de estado con sistema de estado activo \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ animado**](object-state-constants.md)<br/> Para obtener más información, vea [constantes de estado de objeto](object-state-constants.md).<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





