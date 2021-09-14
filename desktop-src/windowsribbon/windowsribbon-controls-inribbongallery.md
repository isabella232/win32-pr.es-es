---
title: In-Ribbon Gallery
description: La In-Ribbon galería de aplicaciones es un control que muestra una colección de elementos relacionados o comandos en la cinta de opciones. Si hay demasiados elementos en la galería, se proporciona una flecha de expansión para mostrar el resto de la colección en un panel expandido.
ms.assetid: d608dd0d-a0af-49a6-a129-7115195c0df2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713455e962996e2cc1a70b418000d0f94a383174
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251738"
---
# <a name="in-ribbon-gallery"></a>In-Ribbon Gallery

La In-Ribbon galería de aplicaciones es un control que muestra una colección de elementos relacionados o comandos en la cinta de opciones. Si hay demasiados elementos en la galería, se proporciona una flecha de expansión para mostrar el resto de la colección en un panel expandido.

-   [Detalles](#details)
-   [Propiedades de la Galería en la cinta de opciones](#in-ribbon-gallery-properties)
-   [Temas relacionados](#related-topics)

## <a name="details"></a>Detalles

En la siguiente captura de pantalla se muestra el control Ribbon In-Ribbon Gallery en Microsoft Paint.

![captura de pantalla de un control inribbongallery en la cinta de microsoft paint.](images/controls/inribbongallery.png)

## <a name="in-ribbon-gallery-properties"></a>In-Ribbon de la galería de aplicaciones

El marco de la cinta de opciones define una colección [de claves de propiedad](windowsribbon-reference-properties.md) para el control In-Ribbon Galería de aplicaciones.

Normalmente, una propiedad In-Ribbon Gallery se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control mediante una llamada al método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) El evento de invalidación se controla y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) no se ejecuta y la aplicación ha consultado un valor de propiedad actualizado, hasta que el marco requiere la propiedad . Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar mediante el método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control galería In-Ribbon datos.




| Clave de propiedad | Notas | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(solo válido para una galería de elementos)<br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.<blockquote>[!Note]<br />Si el comando asociado al control se invalida mediante una llamada a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, el marco consulta esta propiedad cuando se pasa como el valor de <code>UI_INVALIDATIONS_VALUE</code> <em>las marcas</em>.</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Solo se puede actualizar a través de la invalidación. | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento InRibbonGallery**](windowsribbon-element-inribbongallery.md)
</dt> <dt>

[Trabajar con galerías](ribbon-controls-galleries.md)
</dt> <dt>

[Ejemplo de galería](windowsribbon-gallerysample.md)
</dt> </dl>

