---
title: Grupo (marco de cinta de Windows)
description: El grupo organiza los comandos y controles relacionados en una pestaña.
ms.assetid: 5d098d3f-a4ee-4f76-8c81-832d0c49cb80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903bd422d11fea81ed03a48bf8e9437f9caab699
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421862"
---
# <a name="group-windows-ribbon-framework"></a>Grupo (marco de cinta de Windows)

El grupo organiza los comandos y controles relacionados en una [pestaña](windowsribbon-controls-tab.md).

-   [Detalles](#details)
-   [Propiedades de grupo](#group-properties)
-   [Temas relacionados](#related-topics)

## <a name="details"></a>Detalles

La siguiente captura de pantalla ilustra el control de grupo de la cinta de opciones.

![captura de pantalla con llamadas que muestran un grupo.](images/controls/group.png)

## <a name="group-properties"></a>Propiedades de grupo

El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de grupo.

Normalmente, una propiedad de grupo se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad. Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de grupo.



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
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Solo se puede actualizar a través de la invalidación.
<blockquote>
[!Note]<br />
El marco de trabajo requiere que el valor de <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> para un control de grupo comience con la letra Z en mayúsculas. Si el valor proporcionado por la aplicación en el método de devolución de llamada <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler:: UpdateProperty</strong></a> no comienza con la letra Z, se omite este valor y el marco de trabajo genera un valor en su lugar. El valor de Framework es la letra Z seguido de un valor numérico que empieza en 1 y aumenta secuencialmente, según sea necesario, para los controles de grupo subsiguientes (Z1, Z2,..., ZX).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
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

[**Group, elemento**](windowsribbon-element-group.md)
</dt> </dl>

