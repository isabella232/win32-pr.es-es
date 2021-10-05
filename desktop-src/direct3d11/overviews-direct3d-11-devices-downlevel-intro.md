---
title: Niveles de característica de Direct3D
description: En este tema se deba a los niveles de características de Direct3D.
ms.assetid: 5ad0525c-249f-452d-950b-df8fa2addde2
keywords:
- Nivel de característica DX
- Nivel de característica de DirectX
- nivel de característica, DX
- nivel de característica, DirectX
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 311257c8ba0881d6937a33083f4077cf31bdc77e
ms.sourcegitcommit: b1f058e2360e54c07cb988a3204ec33f47889122
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2021
ms.locfileid: "129454601"
---
# <a name="direct3d-feature-levels"></a>Niveles de característica de Direct3D

Para controlar la diversidad de tarjetas de vídeo en máquinas nuevas y existentes, Microsoft Direct3D 11 presenta el concepto de niveles de características. En este tema se deba a los niveles de características de Direct3D.

Cada tarjeta de vídeo implementa un cierto nivel de funcionalidad de Microsoft DirectX (DX) en función de las unidades de procesamiento gráfico (GPU) instaladas. En versiones anteriores de Microsoft Direct3D, podía averiguar la versión de Direct3D que implementó la tarjeta de vídeo y, a continuación, programar la aplicación en consecuencia.

Con Direct3D 11, se introduce un nuevo paradigma denominado niveles de características. Un nivel de características es un conjunto bien definido de funcionalidades GPU. Por ejemplo, el nivel de característica 9 1 implementa la funcionalidad que se implementó en Microsoft Direct3D 9, que expone las funcionalidades de los modelos de sombreador \_ [ps \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-x.md) y [vs \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-vs-2-x.md), mientras que el nivel de característica 11 0 implementa la funcionalidad que se implementó en \_ Direct3D 11.

Ahora, cuando cree un dispositivo, puede intentar crear un dispositivo para el nivel de característica que desea solicitar. Si la creación del dispositivo funciona, ese nivel de característica existe, si no es así, el hardware no admite ese nivel de característica. Puede intentar volver a crear un dispositivo en un nivel de característica inferior o puede optar por salir de la aplicación. Para obtener más información sobre cómo crear un dispositivo, consulte la [**función D3D11CreateDevice.**](/windows/win32/api/D3D11/nf-d3d11-d3d11createdevice)

Con los niveles de características, puede desarrollar una aplicación para Direct3D 9, Microsoft Direct3D 10 o Direct3D 11 y, a continuación, ejecutarla en hardware 9, 10 o 11 (con algunas excepciones; por ejemplo, las 11 nuevas características no se ejecutarán en una tarjeta 9 existente). Este es un par de otras propiedades básicas de los niveles de características:

- Una GPU que permite crear un dispositivo cumple o supera la funcionalidad de ese nivel de característica.
- Un nivel de característica siempre incluye la funcionalidad de los niveles de características anteriores o inferiores.
- Un nivel de característica no implica rendimiento, solo funcionalidad. El rendimiento depende de la implementación de hardware.
- Elija un nivel de característica al crear un dispositivo Direct3D 11.

Para obtener información sobre las limitaciones de creación de dispositivos de tipo que no son de hardware en determinados niveles de características, vea Limitaciones de creación de [WARP y Dispositivos de referencia.](overviews-direct3d-11-devices-limitations.md)

Para ayudarle a decidir con qué nivel de característica diseñar, compare las características de cada nivel de característica.

En la sección 10Level9 Reference (Referencia de [10Level9)](d3d11-graphics-reference-10level9.md) se enumeran las diferencias entre el comportamiento de los distintos métodos [**ID3D11Device**](/windows/win32/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/win32/api/D3D11/nn-d3d11-id3d11devicecontext) en los distintos niveles de características 10Level9.

## <a name="formats-of-version-numbers"></a>Formatos de números de versión

Hay tres formatos para las versiones de Direct3D, los modelos de sombreador y los niveles de características.

- Las versiones de Direct3D usan un punto; por ejemplo, Direct3D 12.0.
- Los modelos de sombreador usan un punto; por ejemplo, el modelo de sombreador 5.1.
- Los niveles de características usan un carácter de subrayado; por ejemplo, nivel de característica 12 \_ 0.

## <a name="feature-support-for-feature-levels-12_2-through-9_3"></a>Compatibilidad con características para los niveles de características del 12_2 al 9_3

Las siguientes características están disponibles para los niveles de características enumerados. Los encabezados de la fila superior son niveles de características de Direct3D. Los encabezados de la columna izquierda son características. Consulte también [Notas al pie para las tablas](#footnotes-for-the-tables).

| Nivel \\ de característica | 12 \_ 2<sup>8</sup> | 12 \_ 1<sup>0</sup> | 12 \_ 0<sup>0</sup> | 11 \_ 1<sup>1</sup> | 11 \_ 0 | 10 \_ 1 | 10 \_ 0 | 9 \_ 3<sup>7</sup> |
|-|-|-|-|-|-|-|-|-|
| Modelo de sombreador (D3D11) | N/D | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 4.x | 4.0 | 2.0 (4 \_ 0 \_ nivel \_ 9 \_ 3) \[ frente a \_ 2 \_ a/ps \_ 2 x \_ \] <sup>5</sup> |
| Modelo de sombreador (D3D12) | 6.5 | 5.1<sup>2</sup> | 5.1<sup>2</sup> | 5.1<sup>2</sup> | 5.1<sup>2</sup> | N/D | N/D | N/D |
| [Recursos en mosaico](tiled-resources.md) | Nivel 3 | Nivel<sup>2 6</sup> | Nivel<sup>2 6</sup> | Opcional | Opcional | No | No | No |
| [Rasterización conservadora](conservative-rasterization.md) | Nivel 3 | Nivel<sup>1 6</sup> | Opcional | Opcional | No | No | No | No |
| [Vistas de orden de rasterizador](rasterizer-order-views.md) | Sí | Sí | Opcional | Opcional | No | No | No | No |
| [Filtros mínimos y máximos](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | Sí | Sí | Sí | Opcional | No | No | No | No |
| Asignar búfer predeterminado | N/D | Opcional | Opcional | Opcional | Opcional | No | No | No |
| [Valor de la referencia de galería de símbolos especificado por el sombreador](shader-specified-stencil-reference-value.md) | Opcional | Opcional | Opcional | Opcional | No | No | No | No |
| Cargas de vista de acceso sin ordenar con tipo | 18 formatos, más opcionales | 18 formatos, más opcionales | 18 formatos, más opcionales | 3 formatos, más opcionales | 3 formatos, más opcionales | No | No | No |
| [Sombreador de geometría](/previous-versions/bb205146(v=vs.85)) | Sí | Sí | Sí | Sí | Sí | Sí | Sí | No |
| [Stream Out](./d3d10-graphics-programming-guide-output-stream-stage.md) | Sí | Sí | Sí | Sí | Sí | Sí | Sí | No |
| [DirectCompute/Sombreador de proceso](direct3d-11-advanced-stages-compute-shader.md) | Sí | Sí | Sí | Sí | Sí | Opcional | Opcional | N/D |
| <b>Nivel \\ de característica de características</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| [Sombreadores de casco y dominio](direct3d-11-advanced-stages-tessellation.md) | Sí | Sí | Sí | Sí | Sí | No | No | No |
| [Matrices de recursos de textura](overviews-direct3d-11-resources-textures-intro.md) | Sí | Sí | Sí | Sí | Sí | Sí | Sí | No |
| [Matrices de recursos de asignación de cubos](overviews-direct3d-11-resources-textures-intro.md) | Sí | Sí | Sí | Sí | Sí | Sí | No | No |
| [Compresión BC4/BC5](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | Sí | Sí | Sí | Sí | Sí | Sí | Sí | No |
| [Compresión BC6H/BC7](texture-block-compression-in-direct3d-11.md) | Sí | Sí | Sí | Sí | Sí | No | No | No |
| [Alfa a cobertura](./d3d10-graphics-programming-guide-blend-state.md) | Sí | Sí | Sí | Sí | Sí | Sí | Sí | No |
| [Formatos extendidos (BGRA, y así sucesivamente)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sí | Sí | Sí | Sí | Sí | Opcional | Opcionales | Sí |
| [Formato de color de alta densidad XR de 10 bits](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sí | Sí | Sí | Sí | Sí | Opcional | Opcional | N/D |
| [Operaciones lógicas (fusión de salida)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Sí | Sí | Sí | Sí | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | No |
| Rasterización independiente del destino | Sí | Sí | Sí | Sí | No | No | No | No |
| [Destino de representación múltiple (MRT) con ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Sí | Sí | Sí | Sí | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | No |
| Ranuras UAV | En niveles<sup>9</sup> | 64 | 64 | 64 | 8 | 1 | 1 | N/D |
| <b>Nivel \\ de característica de características</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| UAV en cada fase | Sí | Sí | Sí | Sí | No | No | No | N/D |
| [Número máximo de muestras forzadas para la representación solo de UAV](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 16 | 16 | 16 | 16 | 8 | N/D | N/D | N/D |
| Desplazamiento de búfer constante y actualizaciones parciales | Sí | Sí | Sí | Sí | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Sí<sup>1</sup> |
| Formatos de 16 bits por píxel (bpp) | Sí | Sí | Sí | Sí | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> |
| Dimensión de textura máxima | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Dimensión de asignación de cubo máxima | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Extensión máxima del volumen | 2048 | 2048 | 2048 | 2048 | 2048 | 2048 | 2048 | 256 |
| Repetición máxima de textura | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 8192 |
| Anisotropía máxima | 16 | 16 | 16 | 16 | 16 | 16 | 16 | 16 |
| Recuento primitivo máximo | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 1048575 |
| Índice máximo de vértices | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 1048575 |
| Número máximo de ranuras de entrada | 32 | 32 | 32 | 32 | 32 | 32 | 16 | 16 |
| Destinos de representación simultáneos | 8 | 8 | 8 | 8 | 8 | 8 | 8 | 4 |
| Consultas de oclusión | Sí | Sí | Sí | Sí | Sí | Sí | Sí | Sí |
| <b>Nivel \\ de característica</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| Combinación alfa independiente | Sí | Sí | Sí | Sí | Sí | Sí | Sí | Sí |
| Reflejo una vez | Sí | Sí | Sí | Sí | Sí | Sí | Sí | Sí |
| Elementos de vértice superpuestos | Sí | Sí | Sí | Sí | Sí | Sí | Sí | Sí |
| Máscaras de escritura independientes | Sí | Sí | Sí | Sí | Sí | Sí | Sí | Sí |
| Instancing | Sí | Sí | Sí | Sí | Sí | Sí | Sí | Sí<sup>7</sup> |
| Nonpowers-of-2 condicionalmente<sup>3</sup> | No | No | No | No | No | No | No | Sí |
| Nonpowers-of-2 unconditionally<sup>4</sup> | Sí | Sí | Sí | Sí | Sí | Sí | Sí | No |

## <a name="feature-support-for-feature-levels-9_2-and-9_1"></a>Compatibilidad con características para los niveles de características 9_2 y 9_1

Las siguientes características están disponibles para los niveles de características enumerados. Los encabezados de la fila superior son niveles de características de Direct3D. Los encabezados de la columna izquierda son características. Consulte también [Notas al pie para las tablas](#footnotes-for-the-tables).

| Nivel \\ de característica | 9 \_ 2 | 9 \_ 1 |
|-|-|-|
| Modelo de sombreador (D3D11) | 2.0 (4 \_ 0 \_ nivel \_ 9 \_ 1) | 2.0 (4 \_ 0 \_ nivel \_ 9 \_ 1) |
| Modelo de sombreador (D3D12) | N/D | N/D |
| [Recursos en mosaico](tiled-resources.md) | No | No |
| [Rasterización conservadora](conservative-rasterization.md) | No | No |
| [Vistas de orden de rasterizador](rasterizer-order-views.md) | No | No |
| [Filtros mínimos y máximos](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | No | No |
| Asignar búfer predeterminado | No | No |
| [Valor de la referencia de galería de símbolos especificado por el sombreador](shader-specified-stencil-reference-value.md) | No | No |
| Cargas de la vista de acceso sin ordenar con tipo | No | No |
| [Sombreador de geometría](/previous-versions/bb205146(v=vs.85)) | No | No |
| [Stream Out](./d3d10-graphics-programming-guide-output-stream-stage.md) | No | No |
| [DirectCompute/Sombreador de proceso](direct3d-11-advanced-stages-compute-shader.md) | N/D | N/D |
| [Sombreadores de casco y dominio](direct3d-11-advanced-stages-tessellation.md) | No | No |
| [Matrices de recursos de textura](overviews-direct3d-11-resources-textures-intro.md) | No | No |
| [Matrices de recursos de Cubemap](overviews-direct3d-11-resources-textures-intro.md) | No | No |
| [Compresión BC4/BC5](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | No | No |
| <b>Nivel \\ de característica</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| [Compresión BC6H/BC7](texture-block-compression-in-direct3d-11.md) | No | No |
| [Alfa a cobertura](./d3d10-graphics-programming-guide-blend-state.md) | No | No |
| [Formatos extendidos (BGRA, y así sucesivamente)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sí | Sí |
| [Formato de color de alta densidad XR de 10 bits](overviews-direct3d-11-devices-downlevel-exceptions.md) | N/D | N/D |
| [Operaciones lógicas (fusión de salida)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | No | No |
| Rasterización independiente del destino | No | No |
| [Varios destinos de representación (MRT) con ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | No | No |
| Ranuras UAV | N/D | N/D |
| UAV en cada fase | N/D | N/D |
| [Número máximo de muestras forzadas para la representación solo de UAV](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | N/D | N/D |
| Desplazamiento de búfer constante y actualizaciones parciales | Sí<sup>1</sup> | Sí<sup>1</sup> |
| Formatos de 16 bits por píxel (bpp) | Opcional<sup>1</sup> | Opcional<sup>1</sup> |
| Dimensión de textura máxima | 2048 | 2048 |
| Max Cubemap Dimension | 512 | 512 |
| Extensión máxima del volumen | 256 | 256 |
| Repetición máxima de textura | 2048 | 128 |
| <b>Nivel \\ de característica</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| Anisotropía máxima | 16 | 2 |
| Número máximo de primitivas | 1048575 | 65535 |
| Índice máximo de vértices | 1048575 | 65534 |
| Número máximo de ranuras de entrada | 16 | 16 |
| Destinos de representación simultáneos | 1 | 1 |
| Consultas de oclusión | Sí | No |
| Combinación alfa independiente | Sí | No |
| Reflejo una vez | Sí | No |
| Elementos de vértice superpuestos | Sí | No |
| Máscaras de escritura independientes | No | No |
| Instancing | No | No |
| Nonpowers-of-2 condicionalmente<sup>3</sup> | Sí | Sí |
| Nonpowers-of-2 unconditionally<sup>4</sup> | No | No |

## <a name="footnotes-for-the-tables"></a>Notas al pie de las tablas

<sup>0 Requiere</sup> el entorno de ejecución de Direct3D 11.3 o Direct3D 12.

<sup>1 Requiere</sup> el entorno de ejecución de Direct3D 11.1.

<sup>2</sup> El modelo de sombreador 5.0 y superior puede admitir opcionalmente sombreadores de precisión doble, sombreadores extendidos de precisión doble, la instrucción de **sombreador SAD4** y sombreadores de precisión parcial. Para determinar las opciones del modelo de sombreador 5.0 que están disponibles para DirectX 11, llame a [**ID3D11Device::CheckFeatureSupport.**](/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) Cierta compatibilidad depende del hardware en el que se ejecute. El modelo de sombreador 5.1 y versiones posteriores solo se admiten a través de la API de DirectX 12, independientemente del nivel de característica que se esté utilizando. DirectX 11 solo admite hasta el modelo de sombreador 5.0. La API de DirectX 12 solo baja al nivel de característica 11 \_ 0.

<sup>3</sup> En los niveles de características \_ 9 1, 9 2 y 9 3, el dispositivo de pantalla admite el uso de \_ texturas 2D con dimensiones que no son potencias de dos en dos \_ condiciones. En primer lugar, solo se puede crear un nivel de mapa MIP para cada textura y, en segundo lugar, no se permite ningún modo de muestreador de encapsulado para texturas (es decir, los miembros **AddressU,** **AddressV** y **AddressW** de [**D3D11 \_ SAMPLER \_ DESC**](/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc) no se pueden establecer en [**D3D11 \_ TEXTURE ADDRESS \_ \_ WRAP**](/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode)).

<sup>4</sup> En los niveles de características 10 \_ 0, 10 1 y 11 0, el dispositivo de visualización admite incondicionalmente el uso de \_ texturas 2D con dimensiones que no son potencias de \_ dos.

<sup>5</sup> Sombreador de vértices 2a con 256 instrucciones, 32 registros temporales, control de flujo estático de profundidad 4, control de flujo dinámico de profundidad 24 y PREDICACIÓN D3DVS20CAPS. \_ Sombreador de píxeles 2x con instrucciones 512, 32 registros temporales, control de flujo estático de profundidad 4, control de flujo dinámico de profundidad 24, \_ \_ D3DPS20CAPS ARBITRARYSWHIBLE, D3DPS20CAPS GRADIENTINSTRUCTIONS, D3DPS20CAPS \_ PREDICATION, D3DPS20CAPS \_ NODEPENDENTREADLIMIT y D3DPS20CAPS \_ NOTESTRUCTIONLIMIT.

<sup>6 niveles</sup> superiores opcionales.

<sup>7</sup> Para el nivel de característica 9_3, los únicos métodos de representación admitidos son **Draw**, **DrawIndexed** y **DrawIndexInstanced.** Además, para el nivel de característica 9_3, la representación de lista de puntos solo se admite para la representación a través **de Draw**.

<sup>8 Requiere</sup> el entorno de ejecución de Direct3D 12.

<sup>9</sup> En la API de Direct3D 12 hay límites en el número de descriptores de un montón CBV/SRV/UAV. Consulte [Niveles de hardware para](../direct3d12/hardware-support.md) más información. Por separado, hay un límite en el número de UAV en todas las tablas de descriptores en todas las fases, que se basa en el [nivel de enlace de recursos](https://microsoft.github.io/DirectX-Specs/d3d/ResourceBinding.html#levels-of-hardware-support).

Para más información sobre la compatibilidad con formatos en distintos niveles de características de hardware, consulte:

- [Compatibilidad con formato DXGI para hardware de nivel 12.1 de características de Direct3D](../direct3ddxgi/hardware-support-for-direct3d-12-1-formats.md)
- [Compatibilidad con formato DXGI para hardware de nivel 12.0 de características de Direct3D](../direct3ddxgi/hardware-support-for-direct3d-12-0-formats.md)
- [Compatibilidad con el formato DXGI para hardware de nivel 11.1 de características de Direct3D](../direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware.md)
- [Compatibilidad con formato DXGI para hardware de nivel 11.0 de características de Direct3D](../direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware.md)
- [Compatibilidad de hardware con formatos Direct3D 10Level9](/previous-versions/ff471324(v=vs.85))
- [Compatibilidad de hardware con formatos de Direct3D 10.1](/previous-versions/cc627091(v=vs.85))
- [Compatibilidad de hardware con formatos Direct3D 10](/previous-versions/cc627090(v=vs.85))

## <a name="related-topics"></a>Temas relacionados

* [Direct3D 11 en hardware de nivel inferior](overviews-direct3d-11-devices-downlevel.md)
* [Niveles de características de hardware (Direct3D 12)](../direct3d12/hardware-feature-levels.md)