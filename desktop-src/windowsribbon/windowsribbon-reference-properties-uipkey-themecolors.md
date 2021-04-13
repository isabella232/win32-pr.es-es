---
title: UI_PKEY_ThemeColors
description: Identifica la propiedad ThemeColors de PKEY de la interfaz de usuario \_ \_ .
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5991ce5058de5a6f49ca8929de02e19657a610
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359048"
---
# <a name="ui_pkey_themecolors"></a>UI \_ PKEY \_ ThemeColors

Identifica la propiedad ThemeColors de PKEY de la interfaz de usuario \_ \_ .

```
propertyDescription
   name = UI_PKEY_ThemeColors
   shellPKey = UI_PKEY_ThemeColors
   formatID = 00000409-7363-696e-8441798acf5aebb7
   propID = 409
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>Observaciones

\_ \_ Una aplicación usa la interfaz de usuario PKEY ThemeColors para consultar los valores del muestrario de colores de un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

Cada valor de [COLORREF](../gdi/colorref.md) corresponde a una muestra de color de un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) donde `ThemeColors` se especifica como el valor del atributo **ColorTemplate** .

El valor de propiedad es una matriz de valores [COLORREF](../gdi/colorref.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del selector de colores](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 