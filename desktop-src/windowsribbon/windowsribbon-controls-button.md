---
title: Button (marco de cinta de Windows)
description: El botón es un control en el que el usuario puede hacer clic para proporcionar la entrada a una aplicación.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1514a1ae66e383d18f81d1ca0ee1a5a8e453335d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149776"
---
# <a name="button-windows-ribbon-framework"></a>Button (marco de cinta de Windows)

El botón es un control en el que el usuario puede hacer clic para proporcionar la entrada a una aplicación.

-   [Introducción](#introduction)
-   [Propiedades del botón](#button-properties)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

La siguiente captura de pantalla contiene tres ejemplos del elemento botón de la cinta de opciones.

![captura de pantalla de los controles de botón en la cinta de opciones de WordPad de Microsoft.](images/controls/button.png)

## <a name="button-properties"></a>Propiedades del botón

El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de botón.

Normalmente, una propiedad de botón se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad. Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de botón.



| Clave de propiedad                                                                                             | Notas                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PKEY de IU \_ \_ habilitada](windowsribbon-reference-properties-uipkey-enabled.md)                               | Admite [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [KeyTip de UI \_ PKEY \_](windowsribbon-reference-properties-uipkey-keytip.md)                                 | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [\_Etiqueta PKEY de IU \_](windowsribbon-reference-properties-uipkey-label.md)                                   | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)             | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [UI \_ PKEY \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [UI \_ PKEY \_ LargeImage](windowsribbon-reference-properties-uipkey-largeimage.md)                         | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [UI \_ PKEY \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [UI \_ PKEY \_ SmallImage](windowsribbon-reference-properties-uipkey-smallimage.md)                         | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Biblioteca de controles de Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcado de botón**](windowsribbon-element-button.md)
</dt> </dl>

 

 
