---
title: UI_PKEY_FontProperties_Italic
description: Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ cursiva.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00825807c57632b1bbea69c47bc9b90d705efa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420855"
---
# <a name="ui_pkey_fontproperties_italic"></a>UI \_ PKEY \_ FontProperties \_ cursiva

Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ cursiva.

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Observaciones

\_ \_ \_ Una aplicación usa la interfaz de usuario PKEY FontProperties cursiva para consultar el estado del botón **cursiva** .

El valor de la propiedad es de la enumeración [**\_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) de la interfaz de usuario.

El valor predeterminado es `UI_FONTPROPERTIES_NOTSET`.

En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.



|                                  |                                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | El botón **cursiva** está deshabilitado y solo la aplicación puede establecerlo. |
| `UI_FONTPROPERTIES_NOTSET`       | El botón **cursiva** no está seleccionado.                                    |
| `UI_FONTPROPERTIES_SET`          | El botón **cursiva** está seleccionado.                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de control de fuente](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Control de fuente](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 