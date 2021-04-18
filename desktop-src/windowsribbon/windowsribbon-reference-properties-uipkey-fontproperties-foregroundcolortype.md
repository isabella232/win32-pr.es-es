---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ ForegroundColorType.
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5589e9b21fc7ab0884a3cac51eba114ee77036b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420971"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a>UI \_ PKEY \_ FontProperties \_ ForegroundColorType

Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ ForegroundColorType.

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Observaciones

La \_ interfaz \_ de usuario PKEY FontProperties \_ ForegroundColorType se usa en una aplicación, junto con la [interfaz de usuario \_ PKEY \_ FontProperties \_ foregroundcolor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), para consultar la configuración de la galería de **colores de texto** .

El valor de la propiedad es de la enumeración [**\_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) de la interfaz de usuario.

El valor predeterminado es `UI_SWATCHCOLORTYPE_RGB`.

En la tabla siguiente se describen los valores de propiedad.



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | No es compatible con [**FontControl**](windowsribbon-element-fontcontrol.md).                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | La aplicación debe consultar la métrica del sistema adecuada para el valor de color normalmente el **color de texto** del tema de Windows actual que se recupera con GETSYSCOLOR (color \_ WINDOWTEXT).                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | La aplicación debe consultar la [interfaz de usuario \_ PKEY \_ FontProperties \_ foregroundcolor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) para obtener el valor de color. El valor de color de la [interfaz de usuario \_ PKEY \_ FontProperties \_ foregroundcolor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) se muestra en el botón **color del texto** y se selecciona en la Galería color de **texto** .<br/> |



 

La interfaz de usuario \_ PKEY \_ FontProperties \_ ForegroundColorType se pasa al método de devolución de llamada [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) cuando se selecciona una muestra de color en una galería de **colores de texto** [**FontControl**](windowsribbon-element-fontcontrol.md) .

> [!Note]  
> Se recomienda encarecidamente que la aplicación solo establezca un valor de **color de texto** inicial y no vuelva a establecer este valor cuando el cursor se cambie de posición dentro de un documento. La última selección debe mantenerse para evitar la necesidad de volver a seleccionar el color deseado.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de control de fuente](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Control de fuente](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

