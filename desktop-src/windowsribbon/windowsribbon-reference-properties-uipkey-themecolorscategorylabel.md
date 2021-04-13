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
# <a name="ui_pkey_themecolorscategorylabel"></a>UI \_ PKEY \_ ThemeColorsCategoryLabel

Identifica la propiedad ThemeColorsCategoryLabel de PKEY de la interfaz de usuario \_ \_ .

```
propertyDescription
   name = UI_PKEY_ThemeColorsCategoryLabel
   shellPKey = UI_PKEY_ThemeColorsCategoryLabel
   formatID = 00000403-7363-696e-8441798acf5aebb7
   propID = 403
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Observaciones

\_ \_ Una aplicación usa la interfaz de usuario PKEY ThemeColorsCategoryLabel para consultar el valor de la etiqueta asociada a la categoría **colores del tema** de una [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

La \_ interfaz \_ de usuario PKEY ThemeColorsCategoryLabel solo es válida para un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) donde `ThemeColors` se especifica como el valor del atributo **ColorTemplate** (esta es la única plantilla que contiene categorías etiquetadas).

En la captura de pantalla siguiente se muestra un `ThemeColors`  [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

![captura de pantalla del elemento dropdowncolorpicker con el atributo colortemplate establecido en ThemeColors.](images/markup/colortemplate.themedcolors.1.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del selector de colores](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




