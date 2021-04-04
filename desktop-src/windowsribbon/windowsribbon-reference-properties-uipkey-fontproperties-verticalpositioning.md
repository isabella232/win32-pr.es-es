---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ VerticalPositioning.
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b67e2a099b7ce02b3c94f7c9d799fcdda5e881
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078220"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a>UI \_ PKEY \_ FontProperties \_ VerticalPositioning

Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ VerticalPositioning.

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

\_ \_ \_ Una aplicación usa la interfaz de usuario PKEY FontProperties VerticalPositioning para consultar el valor de  los controles de superíndice y **subíndice** .

El valor de la propiedad es de la enumeración [**\_ FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) de la interfaz de usuario.

El valor predeterminado es `UI_FONTVERTICALPOSITION_NOTSET`.

En la captura de pantalla siguiente se muestran los botones de superíndice y **subíndice** **de la cinta** de opciones [**FontControl**](windowsribbon-element-fontcontrol.md).

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/markup/fontcontrol-subsuper.png)

En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.



|                                        |                                                                                                |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | Los **botones de superíndice y** **subíndice** están deshabilitados y solo se pueden establecer en la aplicación. |
| `UI_FONTVERTICALPOSITION_NOTSET`       | Los **botones de superíndice** y **subíndice** no están seleccionados.                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | El botón **Superscript** está seleccionado.                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | El botón **subíndice** está seleccionado.                                                              |



 

> [!Note]  
> Los **botones de superíndice y** **subíndice** no se pueden seleccionar a la vez.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de control de fuente](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[Control de fuente](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 