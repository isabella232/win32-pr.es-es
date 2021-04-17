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
# <a name="ui_pkey_standardcolors"></a><span data-ttu-id="aaae9-103">UI \_ PKEY \_ StandardColors</span><span class="sxs-lookup"><span data-stu-id="aaae9-103">UI\_PKEY\_StandardColors</span></span>

<span data-ttu-id="aaae9-104">Identifica la propiedad StandardColors de PKEY de la interfaz de usuario \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="aaae9-104">Identifies the UI\_PKEY\_StandardColors property.</span></span>

```
propertyDescription
   name = UI_PKEY_StandardColors
   shellPKey = UI_PKEY_StandardColors
   formatID = 00000410-7363-696e-8441798acf5aebb7
   propID = 410
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a><span data-ttu-id="aaae9-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aaae9-105">Remarks</span></span>

<span data-ttu-id="aaae9-106">\_ \_ Una aplicación usa la interfaz de usuario PKEY StandardColors para consultar los valores del muestrario de colores de un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="aaae9-106">UI\_PKEY\_StandardColors is used by an application to query the color swatch values of a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="aaae9-107">Cada valor de [COLORREF](../gdi/colorref.md) corresponde a una muestra de color de un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) independientemente del valor especificado para el atributo **ColorTemplate** .</span><span class="sxs-lookup"><span data-stu-id="aaae9-107">Each [COLORREF](../gdi/colorref.md) value corresponds to a color swatch in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) regardless of the value specified for the **ColorTemplate** attribute.</span></span>

<span data-ttu-id="aaae9-108">El valor de propiedad es una matriz de valores [COLORREF](../gdi/colorref.md) .</span><span class="sxs-lookup"><span data-stu-id="aaae9-108">The property value is an array of [COLORREF](../gdi/colorref.md) values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaae9-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aaae9-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaae9-110">Propiedades del selector de colores</span><span class="sxs-lookup"><span data-stu-id="aaae9-110">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 