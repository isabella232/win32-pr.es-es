---
title: UI_PKEY_FontProperties_Bold
description: Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ Bold.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dca8a58b9c5bfa51cfba8d80a477dafb744dfb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705007"
---
# <a name="ui_pkey_fontproperties_bold"></a>UI \_ PKEY \_ FontProperties \_ Bold

Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ Bold.

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Observaciones

\_ \_ \_ Una aplicación usa la interfaz de usuario PKEY FontProperties Bold para consultar el estado del botón **negrita** .

El valor de la propiedad es de la enumeración [**\_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) de la interfaz de usuario.

El valor predeterminado es `UI_FONTPROPERTIES_NOTSET`.

En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.



|                                  |                                                                     |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | El botón **negrita** está deshabilitado y solo la aplicación puede establecerlo. |
| `UI_FONTPROPERTIES_NOTSET`       | El botón **negrita** no está seleccionado.                                    |
| `UI_FONTPROPERTIES_SET`          | El botón **negrita** está seleccionado.                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de control de fuente](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Control de fuente](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 