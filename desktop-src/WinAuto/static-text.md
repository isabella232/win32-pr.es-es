---
title: Texto estático (referencia de elemento de la interfaz de usuario de MSAA)
description: Los controles de texto estático proporcionan una manera cómoda de mostrar texto en cuadros de diálogo y otras ventanas. Los controles de texto estático suelen actuar como etiquetas para otros controles.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da892a102caa8a1af1729bdb4fc2258f461828adf1f7622e8ff5abf8a2a0bc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052493"
---
# <a name="static-text-msaa-ui-element-reference"></a>Texto estático (referencia de elemento de la interfaz de usuario de MSAA)

Los controles de texto estático proporcionan una manera cómoda de mostrar texto en cuadros de diálogo y otras ventanas. Los controles de texto estático suelen actuar como etiquetas para otros controles.

El nombre de clase de ventana para un control de texto estático es "STATIC".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los controles de texto estático admiten los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Los controles de texto estático admiten las [**siguientes propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **propiedad ChildCount** es cero.                                                                                                                                                                                                                                                          |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **propiedad KeyboardShortcut** es la tecla de acceso, que es el carácter subrayado en el texto que activa el control asociado al texto estático. La cadena devuelta contiene el carácter de clave de acceso anexado a la cadena "Alt+".                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **propiedad Name** es la misma que la del texto del control de texto estático.                                                                                                                                                                                                                     |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **propiedad Parent** es una ventana ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) que rodea el control y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana que el control.                                                                                   |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **propiedad Role** es ROLE SYSTEM [**\_ \_ STATICTEXT.**](object-roles.md)                                                                                                                                                                                             |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **propiedad State** es una combinación de uno o varios de los valores [siguientes:](object-state-constants.md) [**STATE SYSTEM \_ \_ READONLY**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notas

-   El [**método accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) devuelve DISP E MEMBERNOTFOUND cuando se llama con \_ \_ [**SELFFUND \_ TAKEFOCUS**](selflag.md) en un objeto de texto estático.
-   Los controles estáticos con el estilo ICONO de SS \_ devuelven datos no válidos en la **propiedad** Name.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





