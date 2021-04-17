---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifica la \_ propiedad PKEY \_ FontProperties StrikeThrough de la interfaz de usuario \_ .
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07804a74671bb219b34b1c67580af083fd5c34c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421250"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a>PKEY de IU \_ \_ FontProperties \_ tachado

Identifica la \_ propiedad PKEY \_ FontProperties StrikeThrough de la interfaz de usuario \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Observaciones

\_La interfaz de usuario PKEY \_ FontProperties \_ StrikeThrough se usa en una aplicación para consultar el estado del botón de **tachado** .

El valor de la propiedad es de la enumeración [**\_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) de la interfaz de usuario.

El valor predeterminado es `UI_FONTPROPERTIES_NOTSET`.

En la captura de pantalla siguiente se muestra el botón **tachado** de la cinta de opciones [**FontControl**](windowsribbon-element-fontcontrol.md).

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/markup/fontcontrol-strikethrough.png)

En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.



|                                  |                                                                              |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | El botón **tachado** está deshabilitado y solo la aplicación puede establecerlo. |
| `UI_FONTPROPERTIES_NOTSET`       | El botón **tachado** no está seleccionado.                                    |
| `UI_FONTPROPERTIES_SET`          | El botón **tachado** está seleccionado.                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de control de fuente](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Control de fuente](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 