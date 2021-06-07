---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifica la propiedad \_ BackgroundColorType de la interfaz de usuario \_ \_ PKEY FontProperties.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bbd2056087d584663c8ca716c4021554098dfa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443826"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a>UI \_ PKEY \_ FontProperties \_ BackgroundColorType

Identifica la propiedad \_ BackgroundColorType de la interfaz de usuario \_ \_ PKEY FontProperties.

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Comentarios

Una \_ aplicación usa ui PKEY FontProperties BackgroundColorType, junto con la interfaz de usuario \_ \_ [ \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor),  para consultar la configuración de la galería de colores de resaltado de texto.

El valor de propiedad es de la [**\_ enumeración SWATCHCOLORTYPE de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) interfaz de usuario.

El valor predeterminado es `UI_SWATCHCOLORTYPE_RGB`.

En la tabla siguiente se describen los valores de propiedad.



|   Propiedad                             |   Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | La aplicación debe consultar la métrica del sistema adecuada para el valor de color normalmente el **color** de fondo actual de la ventana de tema de Windows que se recupera con GetSysColor(COLOR \_ WINDOW).                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | No es compatible con [**FontControl**](windowsribbon-element-fontcontrol.md).                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | La aplicación debe consultar [la interfaz de usuario \_ \_ PKEY FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) para el valor de color. El valor de color de [ui \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) se muestra en el botón Color de resaltado de texto y se selecciona en la galería de **colores de resaltado de** texto. <br/> |



 

Ui PKEY FontProperties BackgroundColorType se pasa al método de devolución de llamada \_ \_ \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)  cuando se selecciona una muestra de color en una galería de colores de resaltado de texto de [**FontControl.**](windowsribbon-element-fontcontrol.md)

> [!Note]  
> Se recomienda encarecidamente que la aplicación solo establezca un valor de **color** de resaltado de texto inicial y no vuelva a establecer este valor cuando el cursor se cambia de posición dentro de un documento. Se debe mantener la última selección para evitar la necesidad de volver a seleccionar el color deseado.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

