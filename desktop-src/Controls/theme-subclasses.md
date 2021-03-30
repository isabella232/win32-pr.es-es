---
title: Usar subclases de tema
description: Se pueden crear subclases para las clases de tema que representan controles como ComboBox, Edit, ExplorerBar, Rebar, Tab y Toolbar con el fin de proporcionar variaciones de tema para ese control concreto.
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c5448bb5fea90193beed854e833cd34e7691b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775583"
---
# <a name="using-theme-subclasses"></a>Usar subclases de tema

Se pueden crear subclases para las clases de tema que representan controles como ComboBox, Edit, ExplorerBar, Rebar, Tab y Toolbar con el fin de proporcionar variaciones de tema para ese control concreto. Por ejemplo, la clase **Button** se subclase como `Start::Button` para proporcionar control sobre el tema que se aplica al botón **iniciar** .

> [!Note]  
> Tenga cuidado al crear subclases como las que se describen en este tema. Dado que las subclases podrían modificarse o no estar disponibles en versiones posteriores de Windows, no se recomienda su uso.

 

## <a name="two-ways-to-use-a-theme-subclass"></a>Dos maneras de utilizar una subclase Theme

Una aplicación puede utilizar un tema de subclases de una de estas dos maneras:

-   Puede usar la función [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) con una cadena del formulario `subclass::class` en el parámetro *pszClassList* .
-   Puede llamar a [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) con el nombre de subclase de tema en el parámetro *pszSubAppName* .

## <a name="using-theme-messages-that-set-visual-style"></a>Usar mensajes de tema que establecen el estilo visual

Algunos controles, como rebar y Toolbar, proporcionan mensajes específicos que puede enviar para indicar al control que use una subclase de tema. Para esos controles, proporcione un puntero a un búfer que contenga el nombre de subclase del tema en el parámetro *lParam* del mensaje. Use el mensaje [**\_ SETWINDOWTHEME de CCM**](ccm-setwindowtheme.md) genérico o use una variante específica, como la que se muestra en la tabla siguiente.



| Control    | Message                                             |
|------------|-----------------------------------------------------|
| Información sobre herramientas    | [**TTM \_ SETWINDOWTHEME**](ttm-setwindowtheme.md)   |
| Barra de herramientas    | [**TB \_ SETWINDOWTHEME**](tb-setwindowtheme.md)     |
| Rebar      | [**\_SETWINDOWTHEME RB**](rb-setwindowtheme.md)     |
| ComboBoxEx | [**CBEM \_ SETWINDOWTHEME**](cbem-setwindowtheme.md) |



 

En la tabla siguiente se enumeran algunas de las subclases que define Windows Vista.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Clase</th>
<th>Subclases </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ComboBox</td>
<td><ul>
<li>Dirección</li>
<li>AddressComposited</li>
<li>InactiveAddress</li>
<li>InactiveAddressComposited</li>
<li>MaxAddress</li>
<li>MaxAddressComposited</li>
<li>MaxInactiveAddress</li>
<li>MaxInactiveAddressComposited</li>
</ul></td>
</tr>
<tr class="even">
<td>Editar</td>
<td><ul>
<li>Dirección</li>
<li>AddressComposited</li>
<li>InactiveAddress</li>
<li>InactiveAddressComposited</li>
<li>InactiveSearchBoxEdit</li>
<li>InactiveSearchBoxEditComposited</li>
<li>MaxAddress</li>
<li>MaxAddressComposited</li>
<li>MaxInactiveAddress</li>
<li>MaxInactiveAddressComposited</li>
<li>MaxInactiveSearchBoxEdit</li>
<li>MaxInactiveSearchBoxEditComposited</li>
<li>MaxSearchBoxEdit</li>
<li>MaxSearchBoxEditComposited</li>
<li>SearchBoxEdit</li>
<li>SearchBoxEditComposited</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rebar</td>
<td><ul>
<li>BrowserTabBar</li>
<li>InactiveNavbar</li>
<li>InactiveNavbarComposited</li>
<li>MaxInactiveNavbar</li>
<li>MaxInactiveNavbarComposited</li>
<li>MaxNavbar</li>
<li>MaxNavbarComposited</li>
<li>Barra de navegación</li>
<li>NavbarComposited</li>
<li>NavbarNonTopmost</li>
</ul></td>
</tr>
<tr class="even">
<td>Pestaña</td>
<td><ul>
<li>BrowserTab</li>
</ul></td>
</tr>
<tr class="odd">
<td>Barra de herramientas</td>
<td><ul>
<li>Go</li>
<li>GoComposited</li>
<li>InactiveGo</li>
<li>InactiveGoComposited</li>
<li>MaxGo</li>
<li>MaxGoComposited</li>
<li>MaxInactiveGo</li>
<li>MaxInactiveGoComposited</li>
<li>SearchButton</li>
<li>SearchButtonComposited</li>
<li>Viajes</li>
<li>TravelComposited</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="internet-explorer-subclasses"></a>Subclases de Internet Explorer

En Windows Vista, las subclases de ciertas clases internas en Windows Internet Explorer y el explorador de Windows están disponibles aunque no sean las propias clases. En la tabla siguiente se enumeran las subclases disponibles.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>AddressBand</td>
<td><ul>
<li>AB</li>
<li>ABGreen</li>
<li>ABGreenComposited</li>
<li>ABRed</li>
<li>ABRedComposited</li>
<li>ABYellow</li>
<li>ABYellowComposited</li>
</ul></td>
</tr>
<tr class="even">
<td>SearchBox</td>
<td><ul>
<li>InactiveSearchBox</li>
<li>InactiveSearchBoxComposited</li>
<li>MaxInactiveSearchBox</li>
<li>MaxInactiveSearchBoxComposited</li>
<li>MaxSearchBox</li>
<li>MaxSearchBoxComposited</li>
<li>SearchBoxComposited</li>
</ul></td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se muestran los detalles de estas clases.



| Control     | Parte         | States                                                 |
|-------------|--------------|--------------------------------------------------------|
| ADDRESSBAND | ABBACKGROUND | NORMAL (0x1), activo (0X2), deshabilitado (0X3), centrado (0x4) |
| CONTROL SEARCHBOX   | SBBACKGROUND | NORMAL (0x1), activo (0X2), deshabilitado (0X3), centrado (0x4) |



 

 

 




