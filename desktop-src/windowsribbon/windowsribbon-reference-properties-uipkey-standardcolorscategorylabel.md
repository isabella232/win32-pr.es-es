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
# <a name="ui_pkey_standardcolorscategorylabel"></a>UI \_ PKEY \_ StandardColorsCategoryLabel

Identifica la propiedad StandardColorsCategoryLabel de PKEY de la interfaz de usuario \_ \_ .

```
propertyDescription
   name = UI_PKEY_StandardColorsCategoryLabel
   shellPKey = UI_PKEY_StandardColorsCategoryLabel
   formatID = 00000404-7363-696e-8441798acf5aebb7
   propID = 404
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Observaciones

\_ \_ Una aplicación usa la interfaz de usuario PKEY StandardColorsCategoryLabel para consultar el valor de la etiqueta asociada a la categoría de **colores estándar** de un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

La \_ interfaz \_ de usuario PKEY StandardColorsCategoryLabel solo es válida para un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) donde `ThemeColors` se especifica como el valor del atributo **ColorTemplate** (esta es la única plantilla que contiene categorías etiquetadas).

En la captura de pantalla siguiente se muestra un `ThemeColors`  [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

![captura de pantalla del elemento dropdowncolorpicker con el atributo colortemplate establecido en ThemeColors.](images/markup/colortemplate.themedcolors.1.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del selector de colores](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




