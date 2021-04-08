---
title: Botón ayuda
description: El botón ayuda es un control en el que el usuario puede hacer clic para mostrar el sistema de ayuda de la aplicación.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc44c9f9a03561f1627067849272509838d7a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995273"
---
# <a name="help-button"></a>Botón ayuda

El botón ayuda es un control en el que el usuario puede hacer clic para mostrar el sistema de ayuda de la aplicación.

-   [Detalles](#details)
-   [Propiedades del botón ayuda](#help-button-properties)
-   [Temas relacionados](#related-topics)

## <a name="details"></a>Detalles

En la captura de pantalla siguiente se muestra el botón ayuda de la cinta de opciones.

![captura de pantalla que muestra el botón ayuda.](images/controls/helpbutton.png)

## <a name="help-button-properties"></a>Propiedades del botón ayuda

El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de botón de ayuda.

Normalmente, una propiedad del botón ayuda se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad. Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de botón de ayuda.



| Clave de propiedad                                                                                     | Notas                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [KeyTip de UI \_ PKEY \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Solo se puede actualizar a través de la invalidación. |
| [\_Etiqueta PKEY de IU \_](windowsribbon-reference-properties-uipkey-label.md)                           | Solo se puede actualizar a través de la invalidación. |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Solo se puede actualizar a través de la invalidación. |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Solo se puede actualizar a través de la invalidación. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Biblioteca de controles de Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento HelpButton**](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 