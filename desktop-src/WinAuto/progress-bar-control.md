---
title: Control barra de progreso (referencia de elemento de la interfaz de usuario de MSAA)
description: Los controles de barra de progreso indican el progreso de una operación larga, como descargar un archivo de Internet. Normalmente, el progreso se expresa como un porcentaje de cero (0) a cien (100).
ms.assetid: 9165d00e-b3f3-41cd-812c-cd39313460fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a96b692de7b4c3992bab82eaa2461ce2826e5117498c24be7d8e40913d8a74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052563"
---
# <a name="progress-bar-control-msaa-ui-element-reference"></a>Control barra de progreso (referencia de elemento de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos de control de barra** de progreso para fines de referencia de elementos de la interfaz de usuario de MSAA. Cómo crear objetos **de control de barra** de progreso en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Los controles de barra de progreso indican el progreso de una operación larga, como descargar un archivo de Internet. Normalmente, el progreso se expresa como un porcentaje de cero (0) a cien (100).

El nombre de clase de ventana de un control de barra de progreso es PROGRESS CLASS, que se define como \_ "msctls \_ progress" en Commctrl.h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los controles de la barra de progreso admiten los [**métodos IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) siguientes:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Los controles de barra de progreso admiten las [**siguientes propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **propiedad ChildCount** es cero.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **propiedad KeyboardShortcut** es la clave de acceso de la barra de progreso, que es un carácter subrayado en el texto de la etiqueta de la barra de progreso. La cadena devuelta contiene el carácter de clave de acceso anexado a la cadena "Alt+".                                                                                                                                                                                                                                 |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **propiedad Name** es el texto de un control de texto estático que etiqueta la barra de progreso.                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **propiedad** Parent es una ventana [**(ROLE SYSTEM \_ \_ WINDOW)**](object-roles.md) que rodea el control y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                              |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **propiedad Role** es ROLE SYSTEM [**\_ \_ PROGRESSBAR.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ FOCUSED**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La **propiedad Value** es una cadena de "0%" a "100%" que describe el progreso.                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





