---
title: Botón de expansión
description: El botón de expansión es un control compuesto con el que el usuario puede seleccionar un valor predeterminado enlazado a un botón primario o seleccionarlo en una lista de valores mutuamente excluyentes que se muestran en una lista desplegable enlazada a un botón secundario.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b78aa261eebb24404eeaf8b3fdad7f630331f58
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105695782"
---
# <a name="split-button"></a>Botón de expansión

El botón de expansión es un control compuesto con el que el usuario puede seleccionar un valor predeterminado enlazado a un botón primario o seleccionarlo en una lista de valores mutuamente excluyentes que se muestran en una lista desplegable enlazada a un botón secundario.

-   [Introducción](#introduction)
-   [Propiedades del botón de expansión](#split-button-properties)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Este control es útil para exponer elementos estrechamente relacionados en los casos en los que un valor predeterminado obvio está disponible y donde los elementos individuales se pueden representar mediante una imagen, texto o ambos.

En la captura de pantalla siguiente se muestra el botón de expansión de la cinta de opciones.

![captura de pantalla de un control splitbutton en una cinta de opciones de ejemplo.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a>Propiedades del botón de expansión

El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de botón de expansión.

Normalmente, una propiedad de botón de expansión se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad. Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de botón de expansión.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Clave de propiedad</th>
<th>Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.<br/> Si todos los elementos secundarios están deshabilitados, el marco de trabajo establece <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> en false (0). De lo contrario, si se habilitan uno o más elementos secundarios, UI_PKEY_Enabled se establece en true (-1).
<blockquote>
[!Important]<br />
La propiedad <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> del control de botón de expansión debe invalidarse después de habilitar o deshabilitar uno o varios elementos secundarios. Esto garantiza que el marco de trabajo consulta el valor de propiedad actualizado y actualiza el estado del control de botón de expansión en la interfaz de usuario de la cinta de opciones.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Biblioteca de controles de Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcado SplitButton**](windowsribbon-element-splitbutton.md)
</dt> </dl>