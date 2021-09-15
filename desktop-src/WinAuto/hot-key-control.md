---
title: Control de clave rápida (referencia de elemento de la interfaz de usuario de MSAA)
description: Los controles de tecla de acceso rápido permiten a los usuarios escribir una combinación de pulsaciones de teclas que se usan como tecla de acceso rápido, lo que les permite realizar una acción rápidamente. Un control de tecla de acceso remoto muestra las pulsaciones de tecla especificadas por el usuario y garantiza que el usuario selecciona una combinación de teclas válida.
ms.assetid: 56c9fee4-f3d3-4f61-8587-bf80186aa5b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aed12ce64fe25c091f6204d9143a0c6ebefb65a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465703"
---
# <a name="hot-key-control-msaa-ui-element-reference"></a>Control de clave rápida (referencia de elemento de la interfaz de usuario de MSAA)

Los controles de tecla de acceso rápido permiten a los usuarios escribir una combinación de pulsaciones de teclas que se usan como tecla de acceso rápido, lo que les permite realizar una acción rápidamente. Un control de tecla de acceso remoto muestra las pulsaciones de tecla especificadas por el usuario y garantiza que el usuario selecciona una combinación de teclas válida.

El nombre de clase de ventana para un control de tecla de acceso rápido es HOTKEY CLASS, que se define como \_ "msctls \_ hotkey32" en Commctrl.h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los controles de tecla de acceso activo admiten los [**siguientes métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Los controles de tecla de acceso activo admiten las [**siguientes propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **propiedad ChildCount** siempre es cero.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **propiedad KeyboardShortcut** es la tecla de acceso del control de tecla de acceso rápido, que es un carácter subrayado en el texto de la etiqueta del control de tecla de acceso rápido. La cadena devuelta contiene el carácter de clave de acceso anexado a la cadena "Alt+".                                                                                                                                                                                                                                 |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **propiedad Name** es el texto de un control de texto estático que etiqueta el control de tecla de acceso.                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **propiedad Parent** es una ventana ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) que rodea el control y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                              |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **propiedad Role** es ROLE SYSTEM [**\_ \_ HOTKEYFIELD**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| FOCUSED STATE SYSTEM [**\_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La **propiedad Value** es una cadena que contiene el texto del campo de tecla de acceso.                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





