---
title: UI_PKEY_FontProperties_Family
description: Identifica la propiedad de familia \_ FontProperties de PKEY \_ de la interfaz de \_ usuario.
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0574ea4fb104cff29b58c8b1f649bd9287672acef677e3ea4cdc6ad5f91367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438664"
---
# <a name="ui_pkey_fontproperties_family"></a>Familia \_ FontProperties de PKEY de interfaz \_ de \_ usuario

Identifica la propiedad de familia \_ FontProperties de PKEY \_ de la interfaz de \_ usuario.

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

Una aplicación usa la familia FontProperties de ui PKEY para consultar el valor de la galería desplegable \_ \_ Familia de \_ fuentes. 

El valor de ui PKEY FontProperties Family coincide con un nombre de familias de fuentes GDI de Windows recuperado con la función \_ \_ \_ [EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) o la función [EnumFontFamiliesEx](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa). [](../gdi/font-families.md)

El valor predeterminado es una cadena vacía.

Si se proporciona una cadena vacía para el valor de la familia FontProperties de PKEY de la interfaz de usuario, se borra \_ \_ la selección de \_ fuente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 