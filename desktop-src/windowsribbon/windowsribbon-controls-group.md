---
title: Group (Windows Ribbon Framework)
description: El grupo organiza los comandos y controles relacionados dentro de una pestaña.
ms.assetid: 5d098d3f-a4ee-4f76-8c81-832d0c49cb80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c153f8cd9d1fc0d2d2bdbaabab0b2e15e099e50d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467422"
---
# <a name="group-windows-ribbon-framework"></a>Group (Windows Ribbon Framework)

El grupo organiza los comandos y controles relacionados dentro de una [pestaña](windowsribbon-controls-tab.md).

-   [Detalles](#details)
-   [Propiedades de grupo](#group-properties)
-   [Temas relacionados](#related-topics)

## <a name="details"></a>Detalles

En la siguiente captura de pantalla se muestra el control Grupo de la cinta de opciones.

![captura de pantalla con llamadas que muestran un grupo.](images/controls/group.png)

## <a name="group-properties"></a>Propiedades de grupo

El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control Grupo.

Normalmente, una propiedad Group se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control mediante una llamada al método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) controla el evento de invalidación y las actualizaciones de propiedad definidas.

El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) no se ejecuta y la aplicación consulta un valor de propiedad actualizado, hasta que el marco de trabajo requiera la propiedad . Por ejemplo, cuando se activa una pestaña y se muestra un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar mediante el método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

En la tabla siguiente se enumeran las claves de propiedad asociadas al control Grupo.




| Clave de propiedad | Notas | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Solo se puede actualizar a través de la invalidación.<blockquote>[!Note]<br />El marco requiere que el valor de <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> para un control Group comience con la letra Z en mayúsculas. Si el valor proporcionado por la aplicación en el método de devolución de llamada <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler::UpdateProperty</strong></a> no comienza con la letra Z, este valor se omite y el marco genera un valor en su lugar. El valor del marco es la letra Z seguida de un valor numérico a partir de 1 y que aumenta secuencialmente, según sea necesario, para los controles group subsiguientes (Z1, Z2, ..., Zx).</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Solo se puede actualizar a través de la invalidación. | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento Group**](windowsribbon-element-group.md)
</dt> </dl>

