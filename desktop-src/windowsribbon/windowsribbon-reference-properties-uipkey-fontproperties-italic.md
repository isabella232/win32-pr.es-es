---
title: UI_PKEY_FontProperties_Italic
description: Identifica la propiedad Ui \_ PKEY \_ FontProperties \_ Italic.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d0dfa07b5112e91d8c25a4ff8c4f31175adf9b7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443816"
---
# <a name="ui_pkey_fontproperties_italic"></a>UI \_ PKEY \_ FontProperties \_ Italic

Identifica la propiedad Ui \_ PKEY \_ FontProperties \_ Italic.

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Comentarios

Una aplicación usa ui PKEY FontProperties Italic para consultar \_ el estado del botón \_ \_ **Cursiva.**

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

 

 