---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ BackgroundColorType.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568898cb2706eb932ea708f929aa4791f0643c74
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487795"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a>UI \_ PKEY \_ FontProperties \_ BackgroundColorType

Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ BackgroundColorType.

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Observaciones

La \_ interfaz \_ de usuario PKEY FontProperties \_ BackgroundColorType se usa en una aplicación, junto con la [interfaz de usuario \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), para consultar la configuración de la galería de **colores de resaltado de texto** .

El valor de la propiedad es de la enumeración [**\_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) de la interfaz de usuario.

El valor predeterminado es `UI_SWATCHCOLORTYPE_RGB`.

En la tabla siguiente se describen los valores de propiedad.



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | La aplicación debe consultar la métrica del sistema correspondiente para el valor de color normalmente el **color de fondo** de la ventana de tema de Windows actual que se recupera con GetSysColor (ventana de color \_ ).                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | No es compatible con [**FontControl**](windowsribbon-element-fontcontrol.md).                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | La aplicación debe consultar la [interfaz de usuario \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) para el valor de color. El valor de color de [UI \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) se muestra en el botón color de **resaltado de texto** y se selecciona en la galería de colores de **resaltado de texto** .<br/> |



 

La interfaz de usuario \_ PKEY \_ FontProperties \_ BackgroundColorType se pasa al método de devolución de llamada [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) cuando se selecciona una muestra de color en una galería de **colores de resaltado de texto** [**FontControl**](windowsribbon-element-fontcontrol.md) .

> [!Note]  
> Se recomienda encarecidamente que la aplicación solo establezca un valor de **color de resaltado de texto** inicial y no vuelva a establecer este valor cuando el cursor se cambie de posición dentro de un documento. La última selección debe mantenerse para evitar la necesidad de volver a seleccionar el color deseado.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de control de fuente](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Control de fuente](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

