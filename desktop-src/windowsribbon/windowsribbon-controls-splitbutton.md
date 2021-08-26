---
title: Botón de expansión
description: El botón Dividir es un control compuesto con el que el usuario puede seleccionar un valor predeterminado enlazado a un botón principal o seleccionar de una lista de valores mutuamente excluyentes mostrados en una lista desplegable enlazada a un botón secundario.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066a2275c49ad8d6dd32dd8ce4fd3d89956f204c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473761"
---
# <a name="split-button"></a>Botón de expansión

El botón Dividir es un control compuesto con el que el usuario puede seleccionar un valor predeterminado enlazado a un botón principal o seleccionar de una lista de valores mutuamente excluyentes mostrados en una lista desplegable enlazada a un botón secundario.

-   [Introducción](#introduction)
-   [Propiedades del botón Dividir](#split-button-properties)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Este control es útil para exponer elementos estrechamente relacionados en casos en los que hay disponible un valor predeterminado obvio y donde los elementos individuales se pueden representar mediante una imagen, texto o ambos.

En la siguiente captura de pantalla se muestra el botón Dividir de la cinta de opciones.

![captura de pantalla de un control splitbutton en una cinta de opciones de ejemplo.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a>Propiedades del botón Dividir

El marco de la cinta de opciones define una colección de claves [de propiedad](windowsribbon-reference-properties.md) para el control Botón de división.

Normalmente, una propiedad Split Button se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control mediante una llamada al método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) controla el evento de invalidación y las actualizaciones de propiedad definidas.

El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) no se ejecuta y la aplicación consulta un valor de propiedad actualizado, hasta que el marco de trabajo requiera la propiedad . Por ejemplo, cuando se activa una pestaña y se muestra un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar mediante el método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

En la tabla siguiente se enumeran las claves de propiedad asociadas al control Botón de división.




| Clave de propiedad | Notas | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.<br /> Si todos los elementos secundarios están deshabilitados, el marco <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> en false (0). De lo contrario, si uno o varios elementos secundarios están habilitados, UI_PKEY_Enabled se establece en true (-1).<blockquote>[!Important]<br />La <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> del control Botón de división debe invalidarse después de habilitar o deshabilitar uno o varios elementos secundarios. Esto garantiza que el marco consulta el valor de propiedad actualizado y actualiza el estado del control Botón de división en la interfaz de usuario de la cinta de opciones.</blockquote><br /><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Solo se puede actualizar a través de la invalidación. | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcado SplitButton**](windowsribbon-element-splitbutton.md)
</dt> </dl>
