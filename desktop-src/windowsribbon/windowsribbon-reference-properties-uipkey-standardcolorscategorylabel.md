---
title: UI_PKEY_StandardColorsCategoryLabel
description: Identifica la propiedad StandardColorsCategoryLabel de PKEY de la interfaz de usuario \_ \_ .
ms.assetid: 59452d4b-acc9-4a5f-a06c-a67b0e676a57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcaecc19213ab82ebafaa76dc2e88a0db836a97a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777562"
---
# <a name="ui_pkey_standardcolorscategorylabel"></a><span data-ttu-id="4c61c-103">UI \_ PKEY \_ StandardColorsCategoryLabel</span><span class="sxs-lookup"><span data-stu-id="4c61c-103">UI\_PKEY\_StandardColorsCategoryLabel</span></span>

<span data-ttu-id="4c61c-104">Identifica la propiedad StandardColorsCategoryLabel de PKEY de la interfaz de usuario \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4c61c-104">Identifies the UI\_PKEY\_StandardColorsCategoryLabel property.</span></span>

```
propertyDescription
   name = UI_PKEY_StandardColorsCategoryLabel
   shellPKey = UI_PKEY_StandardColorsCategoryLabel
   formatID = 00000404-7363-696e-8441798acf5aebb7
   propID = 404
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="4c61c-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c61c-105">Remarks</span></span>

<span data-ttu-id="4c61c-106">\_ \_ Una aplicación usa la interfaz de usuario PKEY StandardColorsCategoryLabel para consultar el valor de la etiqueta asociada a la categoría de **colores estándar** de un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="4c61c-106">UI\_PKEY\_StandardColorsCategoryLabel is used by an application to query the value of the label associated with the **Standard Colors** category of a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="4c61c-107">La \_ interfaz \_ de usuario PKEY StandardColorsCategoryLabel solo es válida para un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) donde `ThemeColors` se especifica como el valor del atributo **ColorTemplate** (esta es la única plantilla que contiene categorías etiquetadas).</span><span class="sxs-lookup"><span data-stu-id="4c61c-107">UI\_PKEY\_StandardColorsCategoryLabel is valid only for a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) where `ThemeColors` is specified as the value of the **ColorTemplate** attribute (this is the only template that contains labeled categories).</span></span>

<span data-ttu-id="4c61c-108">En la captura de pantalla siguiente se muestra un `ThemeColors`  [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="4c61c-108">The following screen shot shows a `ThemeColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

![captura de pantalla del elemento dropdowncolorpicker con el atributo colortemplate establecido en ThemeColors.](images/markup/colortemplate.themedcolors.1.png)

## <a name="related-topics"></a><span data-ttu-id="4c61c-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c61c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c61c-111">Propiedades del selector de colores</span><span class="sxs-lookup"><span data-stu-id="4c61c-111">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




