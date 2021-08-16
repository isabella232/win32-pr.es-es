---
title: UI_PKEY_ThemeColors
description: Identifica la propiedad \_ PKEY \_ ThemeColors de la interfaz de usuario.
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5c4582561e3c86ba19b2821cf600d0a1da614cfc9fc7144b935665c8af7f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437800"
---
# <a name="ui_pkey_themecolors"></a>UI \_ PKEY \_ ThemeColors

Identifica la propiedad \_ PKEY \_ ThemeColors de la interfaz de usuario.

```
propertyDescription
   name = UI_PKEY_ThemeColors
   shellPKey = UI_PKEY_ThemeColors
   formatID = 00000409-7363-696e-8441798acf5aebb7
   propID = 409
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>Comentarios

Una aplicación usa ui PKEY ThemeColors para consultar los valores de la muestra de \_ \_ color de [**dropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)

Cada [valor COLORREF](../gdi/colorref.md) corresponde a una muestra de color en [**un elemento DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) donde se especifica como el valor `ThemeColors` del atributo **ColorTemplate.**

El valor de propiedad es una matriz de [valores COLORREF.](../gdi/colorref.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Selector de colores propiedades](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 