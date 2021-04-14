---
title: UI_PKEY_FontProperties_Underline
description: Identifica la \_ propiedad de \_ subrayado PKEY FontProperties de la interfaz de usuario \_ .
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 380c3fdadb636775f80b789a585c42ff2369234a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487955"
---
# <a name="ui_pkey_fontproperties_underline"></a>Subrayado de UI \_ PKEY \_ FontProperties \_

Identifica la \_ propiedad de \_ subrayado PKEY FontProperties de la interfaz de usuario \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a>Observaciones

\_ \_ \_ Una aplicación usa el subrayado FontProperties PKEY de interfaz de usuario para consultar el estado del botón de **subrayado** .

El valor de la propiedad es de la enumeración [**\_ FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) de la interfaz de usuario.

El valor predeterminado es `UI_FONTUNDERLINE_NOTSET`.

En la captura de pantalla siguiente se muestra el botón **subrayado** de la cinta de opciones [**FontControl**](windowsribbon-element-fontcontrol.md).

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/markup/fontcontrol-underline.png)

En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.



|                                 |                                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | El botón **subrayado** está deshabilitado y solo la aplicación puede establecerlo. |
| `UI_FONTUNDERLINE_NOTSET`       | El botón **subrayado** no está seleccionado.                                    |
| `UI_FONTUNDERLINE_SET`          | El botón **subrayado** está seleccionado.                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de control de fuente](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[Control de fuente](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 