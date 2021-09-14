---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifica la propiedad \_ \_ ForegroundColorType de PKEY de la interfaz de \_ usuario.
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f261256a36ee7a387c6c3a695d8c1182898690c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256413"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a>UI \_ PKEY \_ FontProperties \_ ForegroundColorType

Identifica la propiedad \_ \_ ForegroundColorType de PKEY de la interfaz de \_ usuario.

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

Una \_ aplicación usa ui PKEY FontProperties ForegroundColorType, junto con la interfaz de usuario \_ \_ [ \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md),  para consultar la configuración de la galería de colores de texto.

El valor de propiedad es de la [**\_ enumeración SWATCHCOLORTYPE de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) interfaz de usuario.

El valor predeterminado es `UI_SWATCHCOLORTYPE_RGB`.

En la tabla siguiente se describen los valores de propiedad.



|     Value                           |     Descripción                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | No es compatible con [**FontControl**](windowsribbon-element-fontcontrol.md).                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | La aplicación debe consultar la métrica del sistema adecuada para el valor de color normalmente el color Windows texto del **tema** actual que se recupera con GetSysColor(COLOR \_ WINDOWTEXT).                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | La aplicación debe consultar la [interfaz \_ de usuario \_ PKEY FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) para el valor de color. El valor de color de ui [ \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) se muestra en el botón **Color** de texto y se selecciona en la **Galería de colores de** texto.<br/> |



 

Ui PKEY FontProperties ForegroundColorType se pasa al método de devolución de llamada \_ \_ \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)  cuando se selecciona una muestra de color en una galería de colores [**de texto FontControl.**](windowsribbon-element-fontcontrol.md)

> [!Note]  
> Se recomienda encarecidamente que la aplicación solo establezca un valor de color text **inicial** y no vuelva a establecer este valor cuando el cursor se cambia de posición dentro de un documento. Se debe mantener la última selección para evitar la necesidad de volver a seleccionar el color deseado.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

