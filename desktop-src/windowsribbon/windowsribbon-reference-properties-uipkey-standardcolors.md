---
title: UI_PKEY_StandardColors
description: Identifica la propiedad StandardColors de PKEY de la interfaz de usuario \_ \_ .
ms.assetid: fbdce7ba-4417-4f7f-928b-fba6af6eb396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc3c3b991e798406736e87d594d09be92d89512
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704969"
---
# <a name="ui_pkey_standardcolors"></a>UI \_ PKEY \_ StandardColors

Identifica la propiedad StandardColors de PKEY de la interfaz de usuario \_ \_ .

```
propertyDescription
   name = UI_PKEY_StandardColors
   shellPKey = UI_PKEY_StandardColors
   formatID = 00000410-7363-696e-8441798acf5aebb7
   propID = 410
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>Observaciones

\_ \_ Una aplicación usa la interfaz de usuario PKEY StandardColors para consultar los valores del muestrario de colores de un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

Cada valor de [COLORREF](../gdi/colorref.md) corresponde a una muestra de color de un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) independientemente del valor especificado para el atributo **ColorTemplate** .

El valor de propiedad es una matriz de valores [COLORREF](../gdi/colorref.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del selector de colores](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 