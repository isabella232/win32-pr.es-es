---
title: Personalización de los colores de la cinta de opciones
description: El Windows de cinta de opciones expone un conjunto de propiedades de color que permiten a una aplicación personalizar la apariencia de varios elementos de la interfaz de usuario de la cinta en tiempo de ejecución.
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Windows Cinta de opciones, personalizar colores
- Cinta de opciones, personalizar colores
- personalizar los colores Windows cinta de opciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ef83c40d49656c82aabfbf41c4ec5375f7f3f54f063ccf30d917e740f87408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710895"
---
# <a name="customizing-ribbon-colors"></a>Personalización de los colores de la cinta de opciones

El Windows de cinta de opciones expone un conjunto de propiedades de color que permiten a una aplicación personalizar la apariencia de varios elementos de la interfaz de usuario de la cinta en tiempo de ejecución.

-   [Introducción](#introduction)
-   [Especificación de los colores de la cinta](#specify-ribbon-colors)
-   [Conversión de RGB a HSB](#convert-rgb-to-hsb)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Las [claves de propiedad de marco](windowsribbon-reference-properties-framework.md) enumeradas en la tabla siguiente se usan para establecer el color de varios elementos de la interfaz de usuario en una aplicación de cinta de opciones. Estas propiedades permiten al marco de la cinta admitir la personalización, los requisitos de identidad y las especificaciones de personalización de marca en todas las aplicaciones.

| Color de la cinta de opciones                     | Clave de propiedad del marco                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color de fondo                 | [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| Color de resaltado (solo Windows 7) | [Interfaz de usuario \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)**Introduced in Windows 8**: ** [UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) no se puede establecer independientemente de la interfaz de usuario [ \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).<br/> <br/>                                                              |
| Color del texto                       | [Interfaz de usuario \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)**Introducido en **Windows 8:** los cambios en el valor predeterminado de la interfaz de usuario [ \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) en Windows 8 pueden requerir un ajuste en la interfaz de usuario [ \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) en aplicaciones de cinta diseñadas para Windows 7.<br/> <br/> |



 

## <a name="specify-ribbon-colors"></a>Especificación de los colores de la cinta

El marco de cinta usa un modelo de color Matiz, Saturación, Brillo (HSB), que difiere de los espacios de color de matiz, saturación, luminosidad (HSL) o matiz, saturación, valor (HSV) más comunes. En concreto, B representa un nivel de luminosidad o brillo general en lugar de la lumez de un color determinado.

Para especificar el color de los elementos de la interfaz de usuario en el marco de la cinta de opciones, una aplicación asigna valores HSB a cada una de las propiedades de color global. A continuación, estos valores se aplican universalmente en todos los elementos de la cinta de opciones según lo requiera la aplicación ribbon (el marco no admite la asignación de valores HSB a controles y elementos individuales).

Introducido en Windows 8**: ** A la clave PKEY de interfaz de usuario[ \_ \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) se le asigna el mismo valor que la interfaz de usuario [ \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

En la tabla siguiente se describen los parámetros HSB del marco de la cinta de opciones.



Componente

Descripción

Valores ajustados\*

Hue (H)

El color, o real, se identifica normalmente como un valor de un intervalo circlular de 0 a 359 grados.

De 0 (rojo) a 255 (rojo)

Saturación (S)

La purga, o saturación, del color medido como un porcentaje de 0 a 100 %.

De 0 (gris) a 255 (totalmente saturado)

Brillo (B)

Brillo total o brillo del color medido como porcentaje de 0 a 100 %.

De 0 (oscuro) a 255 (claro)

\* El intervalo original para cada valor de parámetro se traduce en un intervalo de 0 a 255 para el marco.



 

Los valores HSB no identifican colores específicos. En su lugar, la combinación de valores de propiedad HSB influye en cómo se ajustan los degradados de color en toda la interfaz de usuario en relación entre sí.

Al asignar valores HSB personalizados a la interfaz de usuario [ \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) y ui [ \_ PKEY \_ GlobalBackgroundColor,](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)se recomienda que estos valores sean de contraste lo suficientemente alto como para garantizar la legibilidad. En concreto, el color del texto debe ser más oscuro que el tono más claro de la interfaz de usuario de la cinta. Cuando sea necesario, el marco ajusta automáticamente el valor PKEY GlobalTextColor HSB de la interfaz de usuario para proporcionar suficiente contraste con cualquier sombreado o degradado de fondo derivado de la interfaz de usuario \_ \_ \_ PKEY \_ GlobalBackgroundColor.

> [!Note]  
> En Windows 7, [ui \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) se puede establecer independientemente de la interfaz de usuario [ \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

 

En el ejemplo siguiente se muestra cómo especificar un color personalizado para las propiedades [ \_ PKEY \_ GlobalTextColor,](windowsribbon-reference-properties-uipkey-globaltextcolor.md) [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)y [UI \_ PKEY \_ GlobalHighlightColor.](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)


```C++
CComPtr<IPropertyStore> spPropertyStore;

// _spFramework is a pointer to the IUIFramework interface that is assigned 
// when the Ribbon is initialized.
if (SUCCEEDED(_spFramework->QueryInterface(&spPropertyStore)))
{
  PROPVARIANT propvarBackground;
  PROPVARIANT propvarHighlight;
  PROPVARIANT propvarText;
 
  // UI_HSBCOLOR is a type defined in UIRibbon.h that is composed of 
  // three component values: hue, saturation and brightness, respectively.
  UI_HSBCOLOR BackgroundColor = UI_HSB(0x14, 0x38, 0x54);
  UI_HSBCOLOR HighlightColor = UI_HSB(0x00, 0x36, 0x87);
  UI_HSBCOLOR TextColor = UI_HSB(0x2B, 0xD6, 0x00);

  InitPropVariantFromUInt32(BackgroundColor, &propvarBackground);
  InitPropVariantFromUInt32(HighlightColor, &propvarHighlight);
  InitPropVariantFromUInt32(TextColor, &propvarText);
 
  spPropertyStore->SetValue(UI_PKEY_GlobalBackgroundColor, propvarBackground);
  spPropertyStore->SetValue(UI_PKEY_GlobalTextColor, propvarText);
 
  spPropertyStore->Commit();
}
```



## <a name="convert-rgb-to-hsb"></a>Conversión de RGB a HSB

En esta sección se describe la fórmula necesaria para hacer coincidir dinámicamente un valor HSB del marco de cinta de opciones, la interfaz de usuario [ \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) en este ejemplo, con un color RGB específico en tiempo de ejecución.

El fondo de la fila de tabulación se usa como punto de referencia porque se representa como una superficie de color plano en comparación con el degradado de brillo del fondo de la cinta.

Se necesita una conversión preliminar para obtener un valor HSL intermedio. A continuación, este valor de HSL se puede convertir en un valor HSB.

> [!Note]  
> La conversión de RGB a HSL se realiza fácilmente con la mayoría del software de edición de fotos.

 

La conversión de HSL (con cada componente en el intervalo de 0,0 a 1,0) en una configuración HSB de la cinta de opciones se realiza mediante las fórmulas siguientes:

-   Fondo<sub>H</sub> = Round(255.0 H)
-   Fondo<sub>S</sub> = Round(255.0 S)
-   Fondo<sub>B</sub> = Round(257.7 + 149.9 ln(L)) si 0,1793 <= L <= 0,9821

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices de color](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[Propiedades del marco](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





