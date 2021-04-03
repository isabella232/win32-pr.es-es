---
title: Efecto de mapa de tono HDR
description: Este efecto ajusta el intervalo dinámico de una imagen para adaptarse mejor a su contenido a la capacidad de la presentación de la salida.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 4c9234e1b50e155173630a2ff7d94756c5be6130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905338"
---
# <a name="hdr-tone-map-effect"></a>Efecto de mapa de tono HDR

Este efecto ajusta el intervalo dinámico de una imagen para adaptarse mejor a su contenido a la capacidad de la presentación de la salida.

Las propiedades de este efecto se identifican mediante la [**enumeración D2D1_HDRTONEMAP_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)y el CLSID se **CLSID_D2D1HdrToneMap**.

## <a name="effect-properties"></a>Propiedades del efecto

| Enumeración de índice y nombre para mostrar | Tipo y valor predeterminado | Descripción |
|-|-|-|
| InputMaxLuminance, D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE | FLOAT | Nivel de luz máximo (o MaxCLL) de la imagen, en Nits. |
| OutputMaxLuminance, D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE | FLOAT | MaxCLL compatible con el destino de salida, en Nits &mdash; normalmente establecido en el MaxCLL de la pantalla. |
| DisplayMode, D2D1_HDRTONEMAP_PROP_DISPLAY_MODE | [**D2D1_HDRTONEMAP_DISPLAY_MODE**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_display_mode) | Cuando se establece en **_HDR**, la curva de asignación de tono se ajusta para ajustarse mejor al comportamiento de las pantallas HDR comunes. |

## <a name="remarks"></a>Observaciones
El valor de `InputMaxLuminance` se deriva normalmente de los metadatos de la imagen. En los casos en los que los metadatos no están presentes, puede usar la función **D2DAdvancedColorImagesRenderer:: ComputeHdrMetadata** (en el [ejemplo de representación de imágenes de color avanzado de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)) para calcular el nivel máximo de luz (MaxCLL) de una imagen, en Nits.

El valor de `OutputMaxLuminance` se ha diseñado para que se derive de la presentación, mediante [**DXGI_OUTPUT_DESC1:: MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1).

El efecto de mapa de tono HDR tiene curvas de mapa de tono diferentes en función de si la pantalla es una pantalla HDR o una pantalla SDR/WCG.

Este efecto está pensado para combinarse con el [efecto de ajuste de nivel blanco](white-level-adjustment-effect.md) para que pueda representar imágenes HDR en Direct2D con la administración de color y la asignación de tono adecuadas. Está dirigido a cualquier marco que quiera proporcionar una experiencia de visualización de imágenes HDR mejor en su clase que controle todos los formatos de imagen HDR de Windows y se adapta a las capacidades de la pantalla (ya sea HDR o WCG/SDR). Los efectos están diseñados para encadenarse en secuencia, tal y como se describe a continuación.

- Tome la imagen de entrada, cuyo espacio de colores definido por su códec. Los metadatos pueden especificar whitePoint. Los metadatos pueden especificar el nivel de luminancia de entrada.
- Aplique el efecto administración del color. Convertir en espacio scRGB (CCCS).
- Aplique el efecto de mapa de tono HDR. Baje el nivel de luz de la imagen hasta el nivel deseado.
- Aplique el efecto ajuste de nivel blanco. Escale el nivel blanco de la imagen al nivel blanco requerido por la cadena de intercambio.
- Vuelva a aplicar el efecto administración del color. Si se va a representar en 8bpc, convertir a sRGB.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Cliente mínimo compatible | Windows 10, versión 1809 (10,0; Compilación 17763) \[ aplicaciones para UWP de aplicaciones de escritorio \|\] |
| Encabezado | d2d1effects \_ 2. h |
| Biblioteca | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [Enumeración D2D1_HDRTONEMAP_PROP](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)
