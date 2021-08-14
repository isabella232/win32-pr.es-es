---
title: Control Animation (Referencia de elementos de la interfaz de usuario de MSAA)
description: Los controles de animación muestran de forma silenciosa un clip de vídeo de audio intercalado (AVI). Normalmente, los controles de animación se muestran cuando se copian archivos o cuando se realiza alguna otra tarea que consume mucho tiempo.
ms.assetid: 2a31d4ba-a1bd-478b-86a9-726fa93ab714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c7f134d5acdd3496f76e3399e5aafd1fcb2664aed37e042bb7c2cfca60f922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326859"
---
# <a name="animation-control-msaa-ui-element-reference"></a>Control Animation (Referencia de elementos de la interfaz de usuario de MSAA)

Los controles de animación muestran de forma silenciosa un clip de vídeo de audio intercalado (AVI). Normalmente, los controles de animación se muestran cuando se copian archivos o cuando se realiza alguna otra tarea que consume mucho tiempo.

El nombre de clase de ventana de un control de animación es ANIMATE CLASS, que se define como \_ "SysAnimate32" en Commctrl.h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los controles de animación admiten los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) siguientes:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Los controles de animación admiten las [**siguientes propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **propiedad ChildCount** es cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Los controles de animación no tienen métodos abreviados de teclado. Sin embargo, si la etiqueta del control contiene una clave de acceso (un carácter subrayado en el texto de la etiqueta del control), [**\_ get accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) devuelve una cadena que no es NULL. Esta cadena contiene el carácter de clave de acceso anexado a la cadena "Alt+". Por ejemplo, si la etiqueta es "Descargar archivos", **KeyboardShortcut** es "Alt+d".                                                                                        |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **propiedad Name** se obtiene del control de texto estático que etiqueta el control de animación. Al crear controles, los desarrolladores de servidores deben asegurarse de que un control de texto estático precede inmediatamente al control que etiqueta dentro del orden de tabulación.                                                                                                                                                                                                                                                                                             |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **propiedad** Parent es una ventana [**(ROLE SYSTEM \_ \_ WINDOW)**](object-roles.md) que rodea el control y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **propiedad Role** es ROLE SYSTEM [**\_ \_ ANIMATION.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **propiedad State** es una combinación de una o varias de las siguientes constantes de estado de objeto: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ ANIMATED**](object-state-constants.md)<br/> Para obtener más información, vea [Constantes de estado de objeto](object-state-constants.md).<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





