---
title: Casilla
description: La casilla es un control en el que el usuario puede hacer clic para proporcionar datos de entrada a una aplicación. El control proporciona un estado de alternancia que se representa visualmente.
ms.assetid: fe07aa5c-1818-41e2-b48d-5fefe50d733f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b68e850d86bd9b15a354cfa41789406e328a57
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478891"
---
# <a name="check-box"></a>Casilla

La casilla es un control en el que el usuario puede hacer clic para proporcionar datos de entrada a una aplicación. El control proporciona un estado de alternancia que se representa visualmente.

-   [Detalles](#details)
-   [Propiedades de casilla](#check-box-properties)
-   [Temas relacionados](#related-topics)

## <a name="details"></a>Detalles

La casilla no admite un estado terciario o indeterminado.

En la siguiente captura de pantalla se muestra el elemento de la casilla de la cinta de opciones.

![captura de pantalla de un control de casilla en la cinta de microsoft paint.](images/controls/checkbox.png)

## <a name="check-box-properties"></a>Propiedades de casilla

El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control Casilla.

Normalmente, una propiedad Check Box se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control mediante una llamada al método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) controla el evento de invalidación y las actualizaciones de propiedad definidas.

El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) no se ejecuta y la aplicación consulta un valor de propiedad actualizado, hasta que el marco de trabajo requiera la propiedad . Por ejemplo, cuando se activa una pestaña y se muestra un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar mediante el método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

En la tabla siguiente se enumeran las claves de propiedad asociadas al control Casilla.




| Clave de propiedad | Notas | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.<blockquote>[!Note]<br />Si el comando asociado al control se invalida mediante una llamada a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, el marco consulta esta propiedad cuando se pasa como el valor de <code>UI_INVALIDATIONS_VALUE</code> <em>las marcas</em>.</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a> | Solo se puede actualizar a través de la invalidación. | 
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

[**Elemento de marcado CheckBox**](windowsribbon-element-checkbox.md)
</dt> </dl>

