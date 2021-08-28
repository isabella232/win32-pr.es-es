---
title: Cuadro combinado (marco Windows cinta de opciones)
description: El cuadro combinado consta de un cuadro de lista de una sola columna que contiene una colección de elementos o comandos mutuamente excluyentes combinados con un control estático o de edición y una flecha desplegable.
ms.assetid: 6b7de2ec-dcb7-44cb-b01f-db1ba0643499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4b6620e436cfaa1a8ed657c647c6881293b24d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474331"
---
# <a name="combo-box-windows-ribbon-framework"></a>Cuadro combinado (marco Windows cinta de opciones)

El cuadro combinado consta de un cuadro de lista de una sola columna que contiene una colección de elementos o comandos mutuamente excluyentes combinados con un control estático o de edición y una flecha desplegable. La parte del cuadro de lista del control se muestra cuando el usuario hace clic en la flecha desplegable.

-   [Detalles](#details)
-   [Propiedades de cuadro combinado](#combo-box-properties)
-   [Temas relacionados](#related-topics)

## <a name="details"></a>Detalles

El elemento o comando seleccionado actualmente (si existe) en el cuadro de lista se muestra en el control estático o de edición. Con un control de edición, si el usuario escriba los caracteres iniciales de un elemento o comando existentes, el cuadro de lista resaltará el primer elemento con esos caracteres iniciales y autocompletará la entrada en el control de edición.

Solo admite una barra de control vertical o un identificador de tamaño.

Este control es útil para exponer elementos de texto simples y estrechamente relacionados.

En la siguiente captura de pantalla se muestra el cuadro combinado de la cinta de opciones en live Movie Maker.

![captura de pantalla de un control de cuadro combinado en la cinta de microsoft paint.](images/controls/combobox.png)

## <a name="combo-box-properties"></a>Propiedades de cuadro combinado

El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control Cuadro combinado.

Normalmente, una propiedad Cuadro combinado se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control mediante una llamada al método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) El evento de invalidación se controla y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) no se ejecuta y la aplicación ha consultado un valor de propiedad actualizado, hasta que el marco requiere la propiedad . Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar mediante el método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

En la tabla siguiente se enumeran las claves de propiedad asociadas al control Cuadro combinado.




| Clave de propiedad | Notas | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-stringvalue.md">UI_PKEY_StringValue</a> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.<blockquote>[!Note]<br />Si el comando asociado al control se invalida mediante una llamada a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, el marco consulta esta propiedad cuando se pasa como el valor de <code>UI_INVALIDATIONS_VALUE</code> <em>las marcas</em>.</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Solo se puede actualizar a través de la invalidación. | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcado ComboBox**](windowsribbon-element-combobox.md)
</dt> <dt>

[Trabajar con galerías](ribbon-controls-galleries.md)
</dt> <dt>

[Ejemplo de galería](windowsribbon-gallerysample.md)
</dt> </dl>

