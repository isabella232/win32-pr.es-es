---
title: Efecto de administración del color
description: Use el efecto administración del color para transformar una imagen de un perfil de color ICC (International color Consortium) en otro. El efecto transforma la imagen según la especificación de ICC.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- efecto de administración del color
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 5f3783132e0e2af511a99fd8c44d5f899e577a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422233"
---
# <a name="color-management-effect"></a>Efecto de administración del color

Use el efecto administración del color para transformar una imagen de un perfil de color ICC (International color Consortium) en otro. El efecto transforma la imagen según la [especificación de ICC](https://www.color.org).

El CLSID para este efecto es CLSID \_ D2D1ColorManagement.

- [Propiedades del efecto](#effect-properties)
- [Modos de intención de representación](#rendering-intent-modes)
- [Modos alfa de imagen de entrada](#input-image-alpha-modes)
- [Compatibilidad con la especificación de ICC](#compliance-with-icc-specification)
- [Comportamiento del canal alfa](#alpha-channel-behavior)
- [Modos de calidad](#quality-modes)
- [Código de ejemplo](#sample-code)
- [Requisitos](#requirements)
- [Temas relacionados](#related-topics)

## <a name="effect-properties"></a>Propiedades del efecto

| Enumeración de índice y nombre para mostrar | Descripción |
|-|-|
| SourceContext<br/> D2D1 \_ COLORMANAGEMENT \_ prop \_ \_ contexto de color de origen \_<br/> | Información del espacio de colores de origen. El tipo es [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).<br/> El valor predeterminado es NULL.<br/> |
| SourceIntent<br/> Intención de representación de origen de D2D1 \_ COLORMANAGEMENT \_ prop \_ \_ \_<br/> | La intención de representación de ICC que se va a usar. El tipo es D2D1 \_ COLORMANAGEMENT \_ Rendering \_ Intent.<br/> El valor predeterminado es D2D1 \_ COLORMANAGEMENT \_ \_ \_ .<br/> |
| DestinationContext<br/> Contexto de color de destino de D2D1 \_ COLORMANAGEMENT \_ prop \_ \_ \_<br/> | La información del espacio de colores de destino. El tipo es [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).<br/> El valor predeterminado es NULL.<br/> |
| DestinationIntent<br/> Objetivo de representación de destino de D2D1 \_ COLORMANAGEMENT \_ prop \_ \_ \_<br/> | La intención de representación de ICC que se va a usar. El tipo es D2D1 \_ COLORMANAGEMENT \_ Rendering \_ Intent.<br/> El valor predeterminado es D2D1 \_ COLORMANAGEMENT \_ \_ \_ .<br/> |
| AlphaMode<br/> D2D1 \_ COLORMANAGEMENT \_ prop \_ \_ modo alfa<br/> | Cómo interpretar los datos alfa contenidos en la imagen de entrada. El tipo es D2D1 \_ COLORMANAGEMENT \_ \_ modo alfa.<br/> El valor predeterminado es D2D1 \_ COLORMANAGEMENT \_ \_ modo alfa \_ premultiplicado.<br/> |
| Calidad<br/> Calidad de la D2D1 \_ COLORMANAGEMENT \_ \_<br/> | Nivel de calidad de la transformación. El tipo es D2D1 \_ COLORMANAGEMENT \_ Quality.<br/> El valor predeterminado es D2D1 \_ COLORMANAGEMENT \_ Quality \_ normal.<br/> |

## <a name="rendering-intent-modes"></a>Modos de intención de representación

| Enumeración | Descripción |
|-|-|
| D2D1 \_ COLORMANAGEMENT de \_ representación del intento de representación \_ \_ | El efecto comprime o expande la gama de colores completa de la imagen para rellenar la gama de colores del dispositivo, de modo que se conserva el saldo de gris, pero no se puede conservar la precisión de la colorimétrico. |
| D2D1 \_ COLORMANAGEMENT de \_ representación \_ \_ con referencia \_ colorimétrica relativa | El efecto conserva el croma de los colores de la imagen con el posible gasto de matiz y luminosidad. |
| \_Saturación del \_ objetivo de \_ representación \_ de D2D1 COLORMANAGEMENT | El efecto ajusta los colores que quedan fuera del intervalo de colores que el dispositivo de salida representa en el color más cercano disponible. No conserva el punto blanco. |
| D2D1 \_ COLORMANAGEMENT de representación de la \_ \_ intención \_ absoluta \_ colorimétrica | El efecto ajusta los colores que se encuentran fuera del intervalo que el dispositivo de salida puede representar en el color más cercano que se puede representar. El efecto no cambia los demás colores y conserva el punto blanco. |

## <a name="input-image-alpha-modes"></a>Modos alfa de imagen de entrada

| Enumeración | Descripción |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ \_ modo alfa \_ premultiplicado | El efecto presupone que el modo alfa está premultiplicado. |
| D2D1 \_ \_ modo alfa \_ COLORMANAGEMENT \_ recto | El efecto presupone que el modo alfa es recto. |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a>Cambios de comportamiento de D2D1_GAMMA1_G2084
    
Si la aplicación usa el espacio de [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) , o uno de los valores de enumeración de [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) que usan el espacio de colores SMPTE St. 2084 (cuantificador perceptual), la aplicación intenta trabajar con datos HDR.

Las API [**ID2D1DeviceContext5:: CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) y [**ID2D1DeviceContext5:: CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) no tienen en cuenta esto; en su lugar, el contenido de HDR se escala para ajustarse al intervalo 0-1 durante la operación de desgamma de G2084.

En la práctica, el contenido que se codifica en este espacio de gamma usa una WhiteLevel de referencia de 10.000 Nits, que normalmente se representaría en CCCS como 10.000/80 = 125,0. Por lo tanto, para facilitar mejor la aplicación, es más sencillo para esta conversión gamma escalar también la luminancia en un factor de 125. A partir de Windows 10, versión 1809 (10,0; Compilación 17763), el comportamiento del efecto de administración del color es tal que aplica este ajuste de escala. Esto significa que usted, como desarrollador, no tiene que aplicar un segundo [efecto de ajuste de nivel blanco](white-level-adjustment-effect.md) a la canalización.

## <a name="compliance-with-icc-specification"></a>Compatibilidad con la especificación de ICC

El efecto de administración del color es compatible con la especificación de ICC v 4.3, con estas limitaciones:

- El efecto es compatible con los espacios de colores de canal 1, 3 y 4.
- El efecto no admite ColorSpace o perfiles de color con nombre.

## <a name="alpha-channel-behavior"></a>Comportamiento del canal alfa

En general, el efecto establece Alpha en 1 (opaco) si no hay ningún dato alfa en la imagen de origen y los datos alfa se descartan si no hay espacio en la imagen de destino. En la tabla siguiente se describe el comportamiento alfa.

<table>
<thead>
<tr class="header">
<th>ColorSpace de origen, formato de píxel</th>
<th>ColorSpace de destino, formato de píxel</th>
<th>Comportamiento alfa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">1 canal, formato de píxeles R $ {REMOVE} $<br />
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
<td rowspan="4">1 canal, formato de píxel RGBA $ {REMOVE} $<br />
</td>
<td>1 canal, formato de píxeles de R</td>
<td>Los datos alfa se descartan</td>
</tr>
<tr class="even">
<td>1 canal, formato de píxel RGBA</td>
<td>Los datos alfa se pasan por</td>

</tr>
<tr class="odd">
<td>3 canales, formato de píxel RGBA</td>
<td>Los datos alfa se pasan por</td>

</tr>
<tr class="even">
<td>4 canales, formato de píxel RGBA</td>
<td>Los datos alfa se descartan</td>

</tr>
<tr class="odd">
<td rowspan="4">3 Channel, formato de píxel RGBA $ {REMOVE} $<br />
</td>
<td>1 canal, formato de píxeles de R</td>
<td>Los datos alfa se descartan</td>
</tr>
<tr class="even">
<td>1 canal, formato de píxel RGBA</td>
<td>Los datos alfa se pasan por</td>

</tr>
<tr class="odd">
<td>3 canales, formato de píxel RGBA</td>
<td>Los datos alfa se pasan por</td>

</tr>
<tr class="even">
<td>4 canales, formato de píxel RGBA</td>
<td>Los datos alfa se descartan</td>

</tr>
<tr class="odd">
<td rowspan="4">4 canales, formato de píxel RGBA $ {REMOVE} $<br />
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
| Prueba de calidad de D2D1 \_ COLORMANAGEMENT \_ \_ | Modo de calidad inferior. Este modo requiere el nivel de característica 9 \_ 1 o superior. |
| D2D1 \_ COLORMANAGEMENT \_ calidad \_ normal | Modo de calidad normal. Este modo requiere el nivel de característica 9 \_ 1 o superior. |
| Calidad de D2D1 \_ COLORMANAGEMENT \_ \_ óptima | El modo de mejor calidad. Este modo requiere el nivel de característica 10 \_ 0 o superior, así como los búferes de precisión de punto flotante. Este modo admite la precisión de punto flotante, así como el intervalo extendido, tal como se define en la especificación de ICC v 4.3. |

Se produce un error en el efecto de administración del color al dibujar si la aplicación solicita un modo de calidad que no es compatible con el hardware. Puede determinar el nivel de característica cuando llame a [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice). Puede comprobar si hay compatibilidad con el búfer de punto flotante mediante una llamada a [**ID2D1EffectContext:: IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) con el valor [**D2D1 \_ buffer \_ Precision \_ 32BPC \_ float**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).

## <a name="sample-code"></a>Código de ejemplo

Para obtener un ejemplo de este efecto, descargue el [ejemplo de ajuste de foto de efectos de Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)y vea la lección 4 del ejemplo.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Cliente mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Servidor mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Encabezado | d2d1effects. h |
| Biblioteca | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
