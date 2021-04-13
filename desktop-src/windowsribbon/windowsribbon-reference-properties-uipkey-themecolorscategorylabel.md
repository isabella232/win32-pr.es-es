---
title: UI_PKEY_ThemeColorsCategoryLabel
description: Identifica la propiedad ThemeColorsCategoryLabel de PKEY de la interfaz de usuario \_ \_ .
ms.assetid: 704f5c3f-f222-4d98-8a1b-e18a2e094a41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6ecd1bf3a3150a8ed1de30b299ca785ad271f69
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356893"
---
# <a name="ui_pkey_themecolorscategorylabel"></a><span data-ttu-id="f428b-103">UI \_ PKEY \_ ThemeColorsCategoryLabel</span><span class="sxs-lookup"><span data-stu-id="f428b-103">UI\_PKEY\_ThemeColorsCategoryLabel</span></span>

<span data-ttu-id="f428b-104">Identifica la propiedad ThemeColorsCategoryLabel de PKEY de la interfaz de usuario \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f428b-104">Identifies the UI\_PKEY\_ThemeColorsCategoryLabel property.</span></span>

```
propertyDescription
   name = UI_PKEY_ThemeColorsCategoryLabel
   shellPKey = UI_PKEY_ThemeColorsCategoryLabel
   formatID = 00000403-7363-696e-8441798acf5aebb7
   propID = 403
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="f428b-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f428b-105">Remarks</span></span>

<span data-ttu-id="f428b-106">\_ \_ Una aplicación usa la interfaz de usuario PKEY ThemeColorsCategoryLabel para consultar el valor de la etiqueta asociada a la categoría **colores del tema** de una [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="f428b-106">UI\_PKEY\_ThemeColorsCategoryLabel is used by an application to query the value of the label associated with the **Theme Colors** category of a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="f428b-107">La \_ interfaz \_ de usuario PKEY ThemeColorsCategoryLabel solo es válida para un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) donde `ThemeColors` se especifica como el valor del atributo **ColorTemplate** (esta es la única plantilla que contiene categorías etiquetadas).</span><span class="sxs-lookup"><span data-stu-id="f428b-107">UI\_PKEY\_ThemeColorsCategoryLabel is valid only for a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) where `ThemeColors` is specified as the value of the **ColorTemplate** attribute (this is the only template that contains labeled categories).</span></span>

<span data-ttu-id="f428b-108">En la captura de pantalla siguiente se muestra un `ThemeColors`  [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="f428b-108">The following screen shot shows a `ThemeColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

![captura de pantalla del elemento dropdowncolorpicker con el atributo colortemplate establecido en ThemeColors.](images/markup/colortemplate.themedcolors.1.png)

## <a name="related-topics"></a><span data-ttu-id="f428b-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f428b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f428b-111">Propiedades del selector de colores</span><span class="sxs-lookup"><span data-stu-id="f428b-111">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




