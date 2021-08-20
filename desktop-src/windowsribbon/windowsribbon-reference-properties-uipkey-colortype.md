---
title: UI_PKEY_ColorType
description: Identifica la propiedad \_ PKEY \_ ColorType de la interfaz de usuario.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e676db37c0ac6c868c3bbbe20145b171fd63a88d1a704717be58cb5d71b6a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118031772"
---
# <a name="ui_pkey_colortype"></a>UI \_ PKEY \_ ColorType

Identifica la propiedad \_ PKEY \_ ColorType de la interfaz de usuario.

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Comentarios

Una aplicación usa ui PKEY ColorType para consultar la configuración \_ de color del control \_ [**DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)

El valor de propiedad es de la [**\_ enumeración SWATCHCOLORTYPE de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) interfaz de usuario.



|    Propiedad                            |    Descripción                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UI \_ SWATCHCOLORTYPE \_ NOCOLOR   | La aplicación debe tratar la configuración de color como transparente. Normalmente se usa junto con la **opción Sin color.**                                                   |
| UI \_ SWATCHCOLORTYPE \_ AUTOMATIC | La aplicación debe [consultar GetSysColor(COLOR \_ WINDOWTEXT).](/windows/win32/api/winuser/nf-winuser-getsyscolor) Normalmente se usa junto con la **configuración de** color Automático. |
| UI \_ SWATCHCOLORTYPE \_ RGB       | La aplicación debe consultar [ui \_ PKEY \_ Color para](windowsribbon-reference-properties-uipkey-color.md) la configuración de color.                                                          |



 

Ui PKEY ColorType se pasa al método de devolución de llamada \_ \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) cuando se selecciona una muestra de color [**en DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Selector de colores propiedades](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 