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
# <a name="ui_pkey_themecolors"></a><span data-ttu-id="236af-103">UI \_ PKEY \_ ThemeColors</span><span class="sxs-lookup"><span data-stu-id="236af-103">UI\_PKEY\_ThemeColors</span></span>

<span data-ttu-id="236af-104">Identifica la propiedad ThemeColors de PKEY de la interfaz de usuario \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="236af-104">Identifies the UI\_PKEY\_ThemeColors property.</span></span>

```
propertyDescription
   name = UI_PKEY_ThemeColors
   shellPKey = UI_PKEY_ThemeColors
   formatID = 00000409-7363-696e-8441798acf5aebb7
   propID = 409
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a><span data-ttu-id="236af-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="236af-105">Remarks</span></span>

<span data-ttu-id="236af-106">\_ \_ Una aplicación usa la interfaz de usuario PKEY ThemeColors para consultar los valores del muestrario de colores de un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="236af-106">UI\_PKEY\_ThemeColors is used by an application to query the color swatch values of a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="236af-107">Cada valor de [COLORREF](../gdi/colorref.md) corresponde a una muestra de color de un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) donde `ThemeColors` se especifica como el valor del atributo **ColorTemplate** .</span><span class="sxs-lookup"><span data-stu-id="236af-107">Each [COLORREF](../gdi/colorref.md) value corresponds to a color swatch in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) where `ThemeColors` is specified as the value of the **ColorTemplate** attribute.</span></span>

<span data-ttu-id="236af-108">El valor de propiedad es una matriz de valores [COLORREF](../gdi/colorref.md) .</span><span class="sxs-lookup"><span data-stu-id="236af-108">The property value is an array of [COLORREF](../gdi/colorref.md) values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="236af-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="236af-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="236af-110">Propiedades del selector de colores</span><span class="sxs-lookup"><span data-stu-id="236af-110">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 