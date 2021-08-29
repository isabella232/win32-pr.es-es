---
title: UI_PKEY_FontProperties_Bold
description: Identifica la propiedad \_ PKEY FontProperties Bold de la \_ interfaz de \_ usuario.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a55b722a7305c9814148cc69d3c34fa8a31eb1fe17f01526a269591a29925ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118031762"
---
# <a name="ui_pkey_fontproperties_bold"></a>UI \_ PKEY \_ FontProperties \_ Bold

Identifica la propiedad \_ PKEY FontProperties Bold de la \_ interfaz de \_ usuario.

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Comentarios

La \_ interfaz de usuario \_ PKEY FontProperties \_ Bold se usa en una aplicación para consultar el estado del botón **Negrita.**

El valor de propiedad es de la [**\_ enumeración FONTPROPERTIES de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) interfaz de usuario.

El valor predeterminado es `UI_FONTPROPERTIES_NOTSET`.

En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.



|      Propiedad                    |    Resultado de la interfaz de usuario                                                        |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **El** botón negrita está deshabilitado y solo la aplicación puede establecerlo. |
| `UI_FONTPROPERTIES_NOTSET`       | **El** botón Negrita no está seleccionado.                                    |
| `UI_FONTPROPERTIES_SET`          | **El** botón Negrita está seleccionado.                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**FONTPROPERTIES \_ de la interfaz de usuario**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 