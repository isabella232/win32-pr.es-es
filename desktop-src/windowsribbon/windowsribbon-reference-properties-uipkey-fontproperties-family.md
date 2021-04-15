---
title: UI_PKEY_FontProperties_Family
description: Identifica la propiedad de la familia de PKEY de interfaz de usuario \_ \_ FontProperties \_ .
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7183e51105a397f14154639512ca11f7c03d44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714387"
---
# <a name="ui_pkey_fontproperties_family"></a>Familia de FontProperties de UI \_ PKEY \_ \_

Identifica la propiedad de la familia de PKEY de interfaz de usuario \_ \_ FontProperties \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Observaciones

\_ \_ \_ Una aplicación usa la familia de UI PKEY FontProperties para consultar el valor de la Galería desplegable de la **familia de fuentes** .

El valor de la familia de PKEY de interfaz de usuario \_ \_ FontProperties \_ coincide con un nombre de [familias de fuentes de Windows GDI](../gdi/font-families.md) recuperado con la función [EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) o [EnumFontFamiliesEx](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).

El valor predeterminado es una cadena vacía.

Si se proporciona una cadena vacía para el valor de la PKEY de la interfaz de usuario \_ \_ FontProperties \_ Family, se borra la selección de fuente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de control de fuente](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Control de fuente](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 