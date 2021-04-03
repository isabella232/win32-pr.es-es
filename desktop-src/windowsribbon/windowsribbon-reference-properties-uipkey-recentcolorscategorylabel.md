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
# <a name="ui_pkey_recentcolorscategorylabel"></a>UI \_ PKEY \_ RecentColorsCategoryLabel

Identifica la propiedad RecentColorsCategoryLabel de PKEY de la interfaz de usuario \_ \_ .

```
propertyDescription
   name = UI_PKEY_RecentColorsCategoryLabel
   shellPKey = UI_PKEY_RecentColorsCategoryLabel
   formatID = 00000405-7363-696e-8441798acf5aebb7
   propID = 405
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Observaciones

\_ \_ Una aplicación usa la interfaz de usuario PKEY RecentColorsCategoryLabel para consultar el valor de la etiqueta asociada a la categoría de **colores recientes** de una [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

La \_ interfaz \_ de usuario PKEY RecentColorsCategoryLabel solo es válida para un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) donde `ThemeColors` se especifica como el valor del atributo **ColorTemplate** (esta es la única plantilla que contiene categorías etiquetadas).

En la captura de pantalla siguiente se muestra un `ThemeColors`  [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

![captura de pantalla del elemento dropdowncolorpicker con el atributo colortemplate establecido en ThemeColors.](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del selector de colores](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




