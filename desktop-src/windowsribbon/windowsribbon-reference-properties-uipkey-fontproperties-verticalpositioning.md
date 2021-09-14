---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifica la propiedad \_ PKEY \_ FontProperties \_ VerticalPositioning de la interfaz de usuario.
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954b01ff3271b9f74fac2c130c697a70e910fc93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267260"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a>UI \_ PKEY \_ FontProperties \_ VerticalPositioning

Identifica la propiedad \_ PKEY \_ FontProperties \_ VerticalPositioning de la interfaz de usuario.

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a>Observaciones

Una \_ aplicación usa la propiedad PKEY FontProperties VerticalPositioning de la interfaz de usuario para consultar el valor de \_ los controles \_ **Superíndice** y **Subíndice.**

El valor de propiedad es de la [**\_ enumeración FONTVERTICALPOSITION de**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) la interfaz de usuario.

El valor predeterminado es `UI_FONTVERTICALPOSITION_NOTSET`.

En la captura de pantalla siguiente se muestran **los botones Superíndice** **y Subíndice** de [**FontControl de la cinta de opciones**](windowsribbon-element-fontcontrol.md).

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/markup/fontcontrol-subsuper.png)

En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.



|     Propiedad.                           |          Resultado de la interfaz de usuario                                                                             |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | **Los botones** **de superíndice** y subíndice están deshabilitados y solo la aplicación puede establecerlo. |
| `UI_FONTVERTICALPOSITION_NOTSET`       | **Los botones** **de superíndice** y subíndice no están seleccionados.                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | **El botón Superíndice** está seleccionado.                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | **El botón De subíndice** está seleccionado.                                                              |



 

> [!Note]  
> Los **botones Superíndice** **y Subíndice** no se pueden seleccionar.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[Control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 