---
title: Efecto de mapa de tono HDR
description: Este efecto ajusta el intervalo dinámico de una imagen para adaptar mejor su contenido a la funcionalidad de la pantalla de salida.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 4c9234e1b50e155173630a2ff7d94756c5be6130
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163245"
---
# <a name="hdr-tone-map-effect"></a>Efecto de mapa de tono HDR

Este efecto ajusta el intervalo dinámico de una imagen para adaptar mejor su contenido a la funcionalidad de la pantalla de salida.

Las propiedades de este efecto se identifican mediante la enumeración [**D2D1_HDRTONEMAP_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop), y el CLSID **se CLSID_D2D1HdrToneMap**.

## <a name="effect-properties"></a>Propiedades de efecto

| Enumeración de nombre para mostrar e índice | Tipo y valor predeterminado | Descripción |
|-|-|-|
| InputMaxLuminance, D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE | FLOAT | El nivel de luz máximo (o MaxCLL) de la imagen, en nits. |
| OutputMaxLuminance, D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE | FLOAT | MaxCLL compatible con el destino de salida, en nits &mdash; normalmente establecido en el MaxCLL de la pantalla. |
| DisplayMode, D2D1_HDRTONEMAP_PROP_DISPLAY_MODE | [**D2D1_HDRTONEMAP_DISPLAY_MODE**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_display_mode) | Cuando se establece **en _HDR**, la curva de asignación de tono se ajusta para ajustarse mejor al comportamiento de las pantallas comunes de HDR. |

## <a name="remarks"></a>Observaciones
El valor de `InputMaxLuminance` normalmente se deriva de los metadatos de la imagen. En los casos en los que los metadatos no están presentes, puede usar la función **D2DAdvancedColorImagesRenderer::ComputeHdrMetadata** (en el ejemplo de representación de imágenes de color avanzado de [Direct2D)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)para calcular el nivel de luz máximo (MaxCLL) de una imagen, en nits.

El valor de `OutputMaxLuminance` está diseñado para derivarse de la pantalla, mediante [**DXGI_OUTPUT_DESC1::MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1).

El efecto mapa de tono HDR tiene curvas de mapa de tono diferentes en función de si la pantalla es una pantalla DE HDR o una pantalla SDR/WCG.

Este efecto está pensado para [](white-level-adjustment-effect.md) combinarse con el efecto de ajuste De nivel blanco para permitirle representar imágenes DE HDR en Direct2D con la administración de colores y la asignación de tono adecuadas. Está dirigido a cualquier marco que quiera proporcionar una mejor experiencia de visualización de imágenes DE HDR que controle todos los formatos de imagen de Windows HDR y se adapte a las funcionalidades de la pantalla (ya sea HDR o WCG/SDR). Los efectos están diseñados para encadenados en secuencia, como se describe a continuación.

- Tome la imagen de entrada, cuyo espacio de color definido por su códec. Los metadatos pueden especificar whitePoint. Los metadatos pueden especificar el nivel de luminosidad de entrada.
- Aplique el efecto de administración de colores. Convertir en espacio scRGB (CCIS).
- Aplique el efecto mapa de tono HDR. Reduzca el nivel de luz de la imagen al nivel deseado.
- Aplique el efecto de ajuste de nivel de blanco. Escale el nivel de blanco de la imagen al nivel de blanco requerido por la cadena de intercambio.
- Vuelva a aplicar el efecto de administración de colores. Si se representa a 8bpc, convierta a sRGB.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Cliente mínimo compatible | Windows 10, versión 1809 (10.0; Compilación de aplicaciones de escritorio UWP 17763) \[ \|\] |
| Encabezado | d2d1effects \_ 2.h |
| Biblioteca | d2d1.lib, dxguid.lib |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [D2D1_HDRTONEMAP_PROP enumeración](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)
