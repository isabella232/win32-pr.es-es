---
title: Personalizar los colores de la cinta de opciones
description: El marco de la cinta de opciones de Windows expone un conjunto de propiedades de color que permiten a una aplicación personalizar la apariencia de varios elementos de la interfaz de usuario de la cinta en tiempo de ejecución.
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Cinta de Windows, personalizar colores
- Cinta, personalizar colores
- personalizar los colores de la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ff6527dc67ee18df4723fc33e4b764e20127e8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103789004"
---
# <a name="customizing-ribbon-colors"></a>Personalizar los colores de la cinta de opciones

El marco de la cinta de opciones de Windows expone un conjunto de propiedades de color que permiten a una aplicación personalizar la apariencia de varios elementos de la interfaz de usuario de la cinta en tiempo de ejecución.

-   [Introducción](#introduction)
-   [Especificar los colores de la cinta](#specify-ribbon-colors)
-   [Convertir RGB en HSB](#convert-rgb-to-hsb)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Las [claves de propiedad de marco](windowsribbon-reference-properties-framework.md) enumeradas en la tabla siguiente se usan para establecer el color de varios elementos de la interfaz de usuario en una aplicación de cinta. Estas propiedades permiten que el marco de cinta admita la personalización, los requisitos de identidad y las especificaciones de personalización de marca entre las aplicaciones.

| Color de la cinta                     | Clave de propiedad de marco de trabajo                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color de fondo                 | [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| Color de resaltado (solo Windows 7) | [Interfaz de usuario \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)* * * * incluido en Windows 8 * *: * * [UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) no se puede establecer independientemente de la [interfaz de usuario \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).<br/> <br/>                                                              |
| Color del texto                       | [Interfaz de usuario \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)* * * * introducido en Windows 8 **:** los cambios en el valor predeterminado de la [interfaz de usuario \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) en Windows 8 podrían requerir un ajuste a la [interfaz de usuario \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) en aplicaciones de cinta diseñadas para Windows 7.<br/> <br/> |



 

## <a name="specify-ribbon-colors"></a>Especificar los colores de la cinta

El marco de la cinta de opciones usa un modelo de color Hue, saturación, luminosidad (HSB), que difiere de los espacios de colores de matiz, saturación, luminosidad (HSL) o Hue, saturación, valor (HSV) más comunes. En concreto, B representa un nivel de brillo o luminosidad general en lugar de la luminosidad de un color determinado.

Para especificar el color de los elementos de la interfaz de usuario en el marco de cinta, una aplicación asigna valores HSB a cada una de las propiedades de color globales. Estos valores se aplican de forma universal a todos los elementos de la cinta de opciones según lo requiera la aplicación de cinta (el marco no admite la asignación de valores HSB a elementos y controles individuales).

Introducido en Windows 8 * *: * *[UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) tiene asignado el mismo valor que la [interfaz de usuario \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

En la tabla siguiente se describen los parámetros HSB del marco de cinta.



Componente

Descripción

Valores ajustados\*

Matiz (H)

El color de pigmento, o real, se identifica normalmente como un valor de un intervalo de circlular de 0 a 359 grados.

0 (rojo) a 255 (rojo)

Saturación (S)

La pureza, o saturación, del color que se mide como un porcentaje del 0 al 100%.

0 (gris) a 255 (completamente saturado)

Brillo (B)

Brillo o oscuridad general del color medido como porcentaje del 0 al 100%.

0 (oscuro) a 255 (claro)

\* El intervalo original de cada valor de parámetro se convierte en un intervalo de 0 a 255 para el marco.



 

Los valores HSB no identifican colores específicos. En su lugar, la combinación de valores de propiedad HSB influye en cómo se ajustan entre sí los degradados de color a lo largo de la interfaz de usuario.

Al asignar valores HSB personalizados a la [interfaz de usuario \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) y a la interfaz de [usuario \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), se recomienda que estos valores sean de contraste suficiente para garantizar la legibilidad. En concreto, el color del texto debe ser más oscuro que el sombreado más claro de la interfaz de usuario de la cinta de opciones. Cuando sea necesario, el marco de trabajo ajusta automáticamente el valor HSB de la interfaz de usuario \_ PKEY \_ GlobalTextColor para proporcionar un contraste suficiente con cualquier sombreado de fondo o degradado derivado de la interfaz de usuario \_ PKEY \_ GlobalBackgroundColor.

> [!Note]  
> En Windows 7, la [interfaz de usuario \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) se puede establecer independientemente de la [interfaz de usuario \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

 

En el ejemplo siguiente se muestra cómo especificar un color personalizado para las propiedades [UI \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)y [UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) .


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



## <a name="convert-rgb-to-hsb"></a>Convertir RGB en HSB

En esta sección se describe la fórmula necesaria para hacer coincidir dinámicamente un valor HSB del marco de cinta, la [interfaz de usuario \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) en este ejemplo, a un color RGB específico en tiempo de ejecución.

El fondo de la fila de pestañas se usa como punto de referencia porque se representa como una superficie de color plano en comparación con el degradado de brillo del fondo de la cinta de opciones.

Es necesaria una conversión preliminar para obtener un valor HSL intermedio. A continuación, este valor HSL se puede convertir a un valor HSB.

> [!Note]  
> La conversión de RGB a HSL se realiza fácilmente con la mayoría del software de edición de fotos.

 

La conversión de HSL (con cada componente en el intervalo de 0,0 a 1,0) a un valor de la cinta de opciones HSB se realiza a través de las siguientes fórmulas:

-   H<sub>background</sub> = Round (255.0 H)
-   S<sub>background</sub> = Round (255.0 S)
-   B<sub>background</sub> = Round (257.7 + 149,9 LN (L)) si 0,1793 <= L <= 0,9821

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones de color](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[Propiedades de Framework](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





