---
title: Uso de subclases de tema
description: Las clases de tema que representan controles como ComboBox, Edit, ExplorerBar, Rebar, Tab y Toolbar se pueden crear en subclases para proporcionar variaciones de tema para ese control concreto.
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba9d2ad43ebd26c0e28258773b4746c597cfdc93
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480171"
---
# <a name="using-theme-subclasses"></a>Uso de subclases de tema

Las clases de tema que representan controles como ComboBox, Edit, ExplorerBar, Rebar, Tab y Toolbar se pueden crear en subclases para proporcionar variaciones de tema para ese control concreto. Por ejemplo, la **clase Button** se subclasifica como para proporcionar control sobre el tema aplicado `Start::Button` al **botón** Iniciar.

> [!Note]  
> Tenga cuidado al crear subclases como las que se de abordan en este tema. Dado que las subclases podrían modificarse o no estar disponibles en versiones posteriores de Windows, no se recomienda su uso.

 

## <a name="two-ways-to-use-a-theme-subclass"></a>Dos maneras de usar una subclase de tema

Una aplicación puede usar un tema con subclases de una de estas dos maneras:

-   Puede usar la [**función OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) con una cadena del formulario `subclass::class` en el parámetro *pszClassList.*
-   Puede llamar a [**SetWindowTheme con el**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) nombre de la subclase theme en el *parámetro pszSubAppName.*

## <a name="using-theme-messages-that-set-visual-style"></a>Usar mensajes de tema que establecen el estilo visual

Algunos controles, como Rebar y Toolbar, proporcionan mensajes específicos que puede enviar para indicar al control que use una subclase de tema. Para esos controles, proporcione un puntero a un búfer que contenga el nombre de la subclase de tema en el *parámetro lParam* del mensaje. Use el mensaje [**GENÉRICO \_ SETWINDOWTHEME**](ccm-setwindowtheme.md) de CCM o use una variante específica como las que se muestran en la tabla siguiente.



| Control    | Message                                             |
|------------|-----------------------------------------------------|
| Información sobre herramientas    | [**\_SETWINDOWTHEME DE TTM**](ttm-setwindowtheme.md)   |
| Barra de herramientas    | [**TB \_ SETWINDOWTHEME**](tb-setwindowtheme.md)     |
| Rebar      | [**RB \_ SETWINDOWTHEME**](rb-setwindowtheme.md)     |
| ComboBoxEx | [**CBEM \_ SETWINDOWTHEME**](cbem-setwindowtheme.md) |



 

En la tabla siguiente se enumeran algunas de las subclases que Windows Vista define.




| Clase | Subclases  | 
|-------|------------|
| ComboBox | <ul><li>Dirección</li><li>AddressComposited</li><li>InactiveAddress</li><li>InactiveAddressComposited</li><li>MaxAddress</li><li>MaxAddressComposited</li><li>Max(Dirección Max))/</li><li>MaxCiónAddressComposited</li></ul> | 
| Editar | <ul><li>Dirección</li><li>AddressComposited</li><li>InactiveAddress</li><li>InactiveAddressComposited</li><li>InactiveSearchBoxEdit</li><li>InactiveSearchBoxEditComposited</li><li>MaxAddress</li><li>MaxAddressComposited</li><li>Max(Dirección Max))/</li><li>MaxCiónAddressComposited</li><li>Max(SearchBoxEdit)</li><li>Max(SearchBoxEditComposited)</li><li>MaxSearchBoxEdit</li><li>MaxSearchBoxEditComposited</li><li>SearchBoxEdit</li><li>SearchBoxEditComposited</li></ul> | 
| Rebar | <ul><li>BrowserTabBar</li><li>InactiveNavbar</li><li>InactiveNavbarComposited</li><li>MaxCiónNavbar</li><li>MaxCiónNavbarComposited</li><li>MaxNavbar</li><li>MaxNavbarComposited</li><li>Barra de navegación</li><li>NavbarComposited</li><li>NavbarNonTopmost</li></ul> | 
| Pestaña | <ul><li>BrowserTab</li></ul> | 
| Barra de herramientas | <ul><li>Go</li><li>GoComposited</li><li>InactiveGo</li><li>InactiveGoComposited</li><li>MaxGo</li><li>MaxGoComposited</li><li>Max Nogo</li><li>MaxCiónGoComposited</li><li>SearchButton</li><li>SearchButtonComposited</li><li>Viajes</li><li>TravelComposited</li></ul> | 




 

## <a name="internet-explorer-subclasses"></a>Internet Explorer subclases

En Windows Vista, las subclases de determinadas clases internas de Windows Internet Explorer y Windows Explorer están disponibles aunque no lo estén. En la tabla siguiente se enumeran las subclases disponibles.




| | | AddressBand | <ul><li>AB</li><li>ABGreen</li><li>ABGreenComposited</li><li>ABRed</li><li>ABRedComposited</li><li>ABYellow</li><li>ABYellowComposited</li></ul> | | SearchBox | <ul><li>InactiveSearchBox</li><li>InactiveSearchBoxComposited</li><li>Max(SearchBox)</li><li>MaxCiónSearchBoxComposited</li><li>MaxSearchBox</li><li>MaxSearchBoxComposited</li><li>SearchBoxComposited</li></ul> | 




 

En la tabla siguiente se muestran los detalles de estas clases.



| Control     | Parte         | States                                                 |
|-------------|--------------|--------------------------------------------------------|
| ADDRESSBAND | ABBACKGROUND | NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4) |
| SEARCHBOX   | SBBACKGROUND | NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4) |



 

 

 




