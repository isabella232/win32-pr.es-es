---
title: UI_PKEY_RecentColorsCategoryLabel
description: Identifica la propiedad \_ PKEY \_ RecentColorsCategoryLabel de la interfaz de usuario.
ms.assetid: e9336b98-59ae-4118-8535-009fc0fda4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f3a7a513afb50f01ee3a03c3a3240a2eae7a6ed7b6b8228c4a49e7343e052e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118031484"
---
# <a name="ui_pkey_recentcolorscategorylabel"></a>UI \_ PKEY \_ RecentColorsCategoryLabel

Identifica la propiedad \_ PKEY \_ RecentColorsCategoryLabel de la interfaz de usuario.

```
propertyDescription
   name = UI_PKEY_RecentColorsCategoryLabel
   shellPKey = UI_PKEY_RecentColorsCategoryLabel
   formatID = 00000405-7363-696e-8441798acf5aebb7
   propID = 405
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Comentarios

Una aplicación usa la clase PKEY RecentColorsCategoryLabel de la interfaz de usuario para consultar el valor de la etiqueta asociada a la categoría Colores recientes de \_ \_ una clase [**DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md) 

Ui PKEY RecentColorsCategoryLabel solo es válido para \_ \_ [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) donde se especifica como el valor del atributo `ThemeColors` **ColorTemplate** (esta es la única plantilla que contiene categorías etiquetadas).

En la siguiente captura de pantalla se `ThemeColors` [**muestra dropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)

![captura de pantalla del elemento dropdowncolorpicker con el atributo colortemplate establecido en themecolors.](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Selector de colores propiedades](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




