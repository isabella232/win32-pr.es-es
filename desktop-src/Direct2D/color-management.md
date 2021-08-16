---
title: Efecto de administración del color
description: Use el efecto de administración de colores para transformar una imagen de un perfil de color DE LA (Consorcio internacional de colores) a otro. El efecto transforma la imagen de acuerdo con la especificación DEI.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- efecto de administración de colores
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 274591312ab110a24fb315d01f72d23a22a938ad41f380620d94a865602e82a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826703"
---
# <a name="color-management-effect"></a>Efecto de administración del color

Use el efecto de administración de colores para transformar una imagen de un perfil de color DE LA (Consorcio internacional de colores) a otro. El efecto transforma la imagen de acuerdo con la [especificación DEI.](https://www.color.org)

El CLSID para este efecto es CLSID \_ D2D1ColorManagement.

- [Propiedades de efecto](#effect-properties)
- [Modos de intención de representación](#rendering-intent-modes)
- [Modos alfa de imagen de entrada](#input-image-alpha-modes)
- [Cumplimiento con la especificación DECTE](#compliance-with-icc-specification)
- [Comportamiento del canal alfa](#alpha-channel-behavior)
- [Modos de calidad](#quality-modes)
- [Código de ejemplo](#sample-code)
- [Requisitos](#requirements)
- [Temas relacionados](#related-topics)

## <a name="effect-properties"></a>Propiedades de efecto

| Enumeración de nombre para mostrar e índice | Descripción |
|-|-|
| SourceContext<br/> CONTEXTO DE COLOR D2D1 \_ COLORMANAGEMENT \_ PROP SOURCE COLOR \_ \_ \_ CONTEXT<br/> | Información del espacio de color de origen. El tipo es [**ID2D1ColorContext.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)<br/> El valor predeterminado es NULL.<br/> |
| SourceIntent<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ SOURCE \_ RENDERING \_ INTENT<br/> | Qué intención de representación de INTENT se va a usar. El tipo es D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT.<br/> El valor predeterminado es D2D1 \_ COLORMANAGEMENT \_ RENDERING INTENT \_ \_ PERCEPTUAL.<br/> |
| DestinationContext<br/> CONTEXTO DE COLOR D2D1 \_ COLORMANAGEMENT \_ PROP DESTINATION COLOR \_ \_ \_ CONTEXT<br/> | Información del espacio de colores de destino. El tipo es [**ID2D1ColorContext.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)<br/> El valor predeterminado es NULL.<br/> |
| DestinationIntent<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ DESTINATION \_ RENDERING \_ INTENT<br/> | Qué intención de representación de INTENT se va a usar. El tipo es D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT.<br/> El valor predeterminado es D2D1 \_ COLORMANAGEMENT \_ RENDERING INTENT \_ \_ PERCEPTUAL.<br/> |
| AlphaMode<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ ALPHA \_ MODE<br/> | Cómo interpretar los datos alfa contenidos en la imagen de entrada. El tipo es D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ MODE.<br/> El valor predeterminado es D2D1 \_ COLORMANAGEMENT \_ ALPHA MODE \_ \_ PREMULTIPLIED.<br/> |
| Calidad<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ QUALITY<br/> | Nivel de calidad de la transformación. El tipo es D2D1 \_ COLORMANAGEMENT \_ QUALITY.<br/> El valor predeterminado es D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ NORMAL.<br/> |

## <a name="rendering-intent-modes"></a>Modos de intención de representación

| Enumeración | Descripción |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT \_ PERCEPTUAL | El efecto comprime o expande la gama de colores completa de la imagen para rellenar la gama de colores del dispositivo, de modo que se conserve el equilibrio de grises, pero es posible que no se conserve la precisión colorimétrica. |
| D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT \_ RELATIVE \_ COLORIMETRIC | El efecto conserva el tono de los colores de la imagen a costa del matiz y la lumíz posibles. |
| SATURACIÓN DE LA INTENCIÓN \_ DE REPRESENTACIÓN DE COLORMANAGEMENT D2D1 \_ \_ \_ | El efecto ajusta los colores que se encuentran fuera del intervalo de colores que el dispositivo de salida representa al color más cercano disponible. No conserva el punto blanco. |
| D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT \_ ABSOLUTE \_ COLORIMETRIC | El efecto ajusta los colores que se encuentran fuera del intervalo que el dispositivo de salida puede representar al color más cercano que se puede representar. El efecto no cambia los demás colores y conserva el punto blanco. |

## <a name="input-image-alpha-modes"></a>Modos alfa de imagen de entrada

| Enumeración | Descripción |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ MODE \_ PREMULTIPLIED | El efecto supone que el modo alfa está premultiplicado. |
| MODO ALFA D2D1 \_ COLORMANAGEMENT \_ \_ \_ STRAIGHT | El efecto supone que el modo alfa es directo. |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a>D2D1_GAMMA1_G2084 cambios de comportamiento
    
Si la aplicación usa el espacio [de D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) o uno de los valores de enumeración [de DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) que usan el espacio de colores SMPTE ST.2084 (Cuantificador perceptual), la aplicación pretende trabajar con datos HDR.

Las API [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) e [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) no tienen en cuenta eso; en su lugar, el contenido HDR se escala para ajustarse al intervalo 0-1 durante la operación G2084 DeGamma.

En la práctica, el contenido que se codifica en este espacio gamma usa un whiteLevel de referencia de 10 000 Nits, que normalmente se representaría enCCIS como 10 000 / 80 = 125.0. Por lo tanto, para facilitar mejor la aplicación, es más sencillo que esta conversión gamma también escale la luminosidad en un factor de 125. A partir Windows 10, versión 1809 (10.0; Compilación 17763), el comportamiento del efecto de administración de colores es tal que aplica este escalado. Esto significa que, como desarrollador, no tiene que aplicar un segundo efecto de ajuste de nivel blanco [en](white-level-adjustment-effect.md) la canalización.

## <a name="compliance-with-icc-specification"></a>Cumplimiento con la especificación DECTE

El efecto de administración de colores es compatible con la especificación DEV V4.3, con estas limitaciones:

- El efecto admite espacios de color de 1, 3 y 4 canales.
- El efecto no admite perfiles ColorSpace ni Named Color.

## <a name="alpha-channel-behavior"></a>Comportamiento del canal alfa

En general, el efecto establece alfa en 1 (opaco) si no hay datos alfa en la imagen de origen y los datos alfa se descartan si no hay espacio en la imagen de destino. En la tabla siguiente se describe el comportamiento alfa.

<table>
<thead>
<tr class="header">
<th>Espacio de colores de origen, formato de píxel</th>
<th>Espacio de colores de destino, formato de píxel</th>
<th>Comportamiento alfa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">1 canal, formato de píxel de R ${REMOVE}$<br />
</td>
<td>1 canal, formato de píxeles de R</td>
<td>(Sin datos alfa)</td>
</tr>
<tr class="even">
<td>1 canal, formato de píxel RGBA</td>
<td>Los datos alfa se establecen en 1 (opaco)</td>

</tr>
<tr class="odd">
<td>3 canales, formato de píxel RGBA</td>
<td>Los datos alfa se establecen en 1 (opaco)</td>

</tr>
<tr class="even">
<td>4 canales, formato de píxel RGBA</td>
<td>(Sin datos alfa)</td>

</tr>
<tr class="odd">
<td rowspan="4">1 canal, formato de píxel RGBA ${REMOVE}$<br />
</td>
<td>1 canal, formato de píxeles de R</td>
<td>Se descartan los datos alfa</td>
</tr>
<tr class="even">
<td>1 canal, formato de píxel RGBA</td>
<td>Los datos alfa se pasan a través de</td>

</tr>
<tr class="odd">
<td>3 canales, formato de píxel RGBA</td>
<td>Los datos alfa se pasan a través de</td>

</tr>
<tr class="even">
<td>4 canales, formato de píxel RGBA</td>
<td>Se descartan los datos alfa</td>

</tr>
<tr class="odd">
<td rowspan="4">3 canales, formato de píxel RGBA ${REMOVE}$<br />
</td>
<td>1 canal, formato de píxeles de R</td>
<td>Se descartan los datos alfa</td>
</tr>
<tr class="even">
<td>1 canal, formato de píxel RGBA</td>
<td>Los datos alfa se pasan a través de</td>

</tr>
<tr class="odd">
<td>3 canales, formato de píxel RGBA</td>
<td>Los datos alfa se pasan a través de</td>

</tr>
<tr class="even">
<td>4 canales, formato de píxel RGBA</td>
<td>Se descartan los datos alfa</td>

</tr>
<tr class="odd">
<td rowspan="4">4 canales, formato de píxel RGBA ${REMOVE}$<br />
</td>
<td>1 canal, formato de píxeles de R</td>
<td>(Sin datos alfa)</td>
</tr>
<tr class="even">
<td>1 canal, formato de píxel RGBA</td>
<td>Los datos alfa se establecen en 1 (opaco)</td>

</tr>
<tr class="odd">
<td>3 canales, formato de píxel RGBA</td>
<td>Los datos alfa se establecen en 1 (opaco)</td>

</tr>
<tr class="even">
<td>4 canales, formato de píxel RGBA</td>
<td>(Sin datos alfa)</td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a>Modos de calidad

| Mode | Descripción |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ PROOF | Modo de calidad más baja. Este modo requiere el nivel de característica 9 \_ 1 o superior. |
| D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ NORMAL | Modo de calidad normal. Este modo requiere el nivel de característica 9 \_ 1 o superior. |
| D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ BEST | El modo de mejor calidad. Este modo requiere el nivel de característica 10 0 o superior, así como \_ búferes de precisión de punto flotante. Este modo admite la precisión de punto flotante, así como el intervalo extendido, tal y como se define en la especificación DEV V4.3. |

Se produce un error en el efecto de administración de colores al dibujar si la aplicación solicita un modo de calidad que no es compatible con el hardware. Puede determinar el nivel de característica al llamar a [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice). Puede comprobar la compatibilidad del búfer de punto flotante llamando a [**ID2D1EffectContext::IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) con el valor [**D2D1 \_ BUFFER PRECISION \_ \_ 32BPC \_ FLOAT.**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision)

## <a name="sample-code"></a>Código de ejemplo

Para obtener un ejemplo de este efecto, descargue el ejemplo de ajuste de fotos efectos de [Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)y vea la lección 4 del ejemplo.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Header | d2d1effects.h |
| Biblioteca | d2d1.lib, dxguid.lib |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
