---
title: UI_PKEY_FontProperties_Italic
description: Identifica la propiedad \_ Ui PKEY \_ FontProperties \_ Italic.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bb72e1ba43b29f5e3815fe42d0ace454ff0219a188a128b422e4a621af210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438540"
---
# <a name="ui_pkey_fontproperties_italic"></a>UI \_ PKEY \_ FontProperties \_ Italic

Identifica la propiedad \_ Ui PKEY \_ FontProperties \_ Italic.

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

Una aplicación usa la cursiva PKEY FontProperties de la interfaz de usuario \_ para consultar el estado del botón \_ \_ **Cursiva.**

El valor de propiedad es de la [**\_ enumeración FONTPROPERTIES de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) interfaz de usuario.

El valor predeterminado es `UI_FONTPROPERTIES_NOTSET`.

En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.



|    Propiedad                      |       Resultado de la interfaz de usuario                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **El** botón Cursiva está deshabilitado y solo la aplicación puede establecerlo. |
| `UI_FONTPROPERTIES_NOTSET`       | **El** botón Cursiva no está seleccionado.                                    |
| `UI_FONTPROPERTIES_SET`          | **El** botón Cursiva está seleccionado.                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**FONTPROPERTIES \_ de la interfaz de usuario**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 