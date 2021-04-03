---
title: UI_PKEY_RecentColorsCategoryLabel
description: Identifica la propiedad RecentColorsCategoryLabel de PKEY de la interfaz de usuario \_ \_ .
ms.assetid: e9336b98-59ae-4118-8535-009fc0fda4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bcb2e3f5df1ba66204a8df6b088ca3a2808ced
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777568"
---
# <a name="ui_pkey_recentcolorscategorylabel"></a><span data-ttu-id="79ae1-103">UI \_ PKEY \_ RecentColorsCategoryLabel</span><span class="sxs-lookup"><span data-stu-id="79ae1-103">UI\_PKEY\_RecentColorsCategoryLabel</span></span>

<span data-ttu-id="79ae1-104">Identifica la propiedad RecentColorsCategoryLabel de PKEY de la interfaz de usuario \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="79ae1-104">Identifies the UI\_PKEY\_RecentColorsCategoryLabel property.</span></span>

```
propertyDescription
   name = UI_PKEY_RecentColorsCategoryLabel
   shellPKey = UI_PKEY_RecentColorsCategoryLabel
   formatID = 00000405-7363-696e-8441798acf5aebb7
   propID = 405
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="79ae1-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79ae1-105">Remarks</span></span>

<span data-ttu-id="79ae1-106">\_ \_ Una aplicación usa la interfaz de usuario PKEY RecentColorsCategoryLabel para consultar el valor de la etiqueta asociada a la categoría de **colores recientes** de una [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="79ae1-106">UI\_PKEY\_RecentColorsCategoryLabel is used by an application to query the value of the label associated with the **Recent Colors** category of a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="79ae1-107">La \_ interfaz \_ de usuario PKEY RecentColorsCategoryLabel solo es válida para un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) donde `ThemeColors` se especifica como el valor del atributo **ColorTemplate** (esta es la única plantilla que contiene categorías etiquetadas).</span><span class="sxs-lookup"><span data-stu-id="79ae1-107">UI\_PKEY\_RecentColorsCategoryLabel is valid only for a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) where `ThemeColors` is specified as the value of the **ColorTemplate** attribute (this is the only template that contains labeled categories).</span></span>

<span data-ttu-id="79ae1-108">En la captura de pantalla siguiente se muestra un `ThemeColors`  [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="79ae1-108">The following screen shot shows a `ThemeColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

![captura de pantalla del elemento dropdowncolorpicker con el atributo colortemplate establecido en ThemeColors.](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a><span data-ttu-id="79ae1-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79ae1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79ae1-111">Propiedades del selector de colores</span><span class="sxs-lookup"><span data-stu-id="79ae1-111">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




