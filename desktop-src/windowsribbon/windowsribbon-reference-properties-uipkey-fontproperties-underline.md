---
title: UI_PKEY_FontProperties_Underline
description: Identifica la propiedad \_ FontProperties Underline de PKEY \_ de la interfaz de \_ usuario.
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066027e5f62416667619937eea7dbe493a3ff279
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443786"
---
# <a name="ui_pkey_fontproperties_underline"></a>Subrayado \_ fontproperties PKEY de la interfaz \_ de \_ usuario

Identifica la propiedad \_ FontProperties Underline de PKEY \_ de la interfaz de \_ usuario.

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a>Comentarios

La \_ interfaz de usuario \_ PKEY FontProperties \_ Underline se usa en una aplicación para consultar el estado del botón **Subrayado.**

El valor de propiedad es de la [**\_ enumeración FONTUNDERLINE de la interfaz de**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) usuario.

El valor predeterminado es `UI_FONTUNDERLINE_NOTSET`.

En la captura de pantalla siguiente se muestra **el botón Subrayado** de [**FontControl de**](windowsribbon-element-fontcontrol.md)la cinta de opciones .

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/markup/fontcontrol-underline.png)

En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.



|      Propiedad                   |       Resultado de la interfaz de usuario                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | **El** botón Subrayado está deshabilitado y solo la aplicación puede establecerlo. |
| `UI_FONTUNDERLINE_NOTSET`       | **El botón** Subrayado no está seleccionado.                                    |
| `UI_FONTUNDERLINE_SET`          | **El botón** Subrayado está seleccionado.                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**\_FONTUNDERLINE de la interfaz de usuario**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[Control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 