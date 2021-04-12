---
title: UI_PKEY_ColorType
description: Identifica la propiedad de la interfaz de usuario \_ PKEY \_ ColorType.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313d2a657d889a7c582d86d8f8c9e4ebd2cfd01e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359162"
---
# <a name="ui_pkey_colortype"></a>Interfaz de usuario \_ PKEY \_ ColorType

Identifica la propiedad de la interfaz de usuario \_ PKEY \_ ColorType.

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Observaciones

\_ \_ Una aplicación usa la interfaz de usuario PKEY ColorType para consultar la configuración de color del control [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .

El valor de la propiedad es de la enumeración [**\_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) de la interfaz de usuario.



|                                |                                                                                                                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SWATCHCOLORTYPE de IU \_ \_ nocolor   | La aplicación debe tratar la configuración de color como transparente. Normalmente, se usa junto con la configuración de color **sin** color.                                                   |
| UI \_ SWATCHCOLORTYPE \_ automática | La aplicación debe consultar [GetSysColor (color \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor). Normalmente, se usa junto con la configuración de color **automática** . |
| UI \_ SWATCHCOLORTYPE \_ RGB       | La aplicación debe consultar el [ \_ \_ color PKEY](windowsribbon-reference-properties-uipkey-color.md) de la interfaz de usuario para la configuración de color.                                                          |



 

La interfaz de usuario \_ PKEY \_ ColorType se pasa al método de devolución de llamada [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) cuando se selecciona una muestra de color en una [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del selector de colores](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 