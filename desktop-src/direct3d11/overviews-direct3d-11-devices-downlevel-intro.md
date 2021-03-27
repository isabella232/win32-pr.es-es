---
title: Niveles de característica de Direct3D
description: En este tema se describen los niveles de características de Direct3D.
ms.assetid: 5ad0525c-249f-452d-950b-df8fa2addde2
keywords:
- Nivel de característica de DX
- Nivel de característica de DirectX
- nivel de característica, DX
- nivel de características, DirectX
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 82667a7a2e02d675185fd65c318aeed10db79844
ms.sourcegitcommit: 85bd7112570865dd2136e0d05bd0a4132e6313ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "104078511"
---
# <a name="direct3d-feature-levels"></a>Niveles de característica de Direct3D

Para controlar la diversidad de tarjetas de vídeo en máquinas nuevas y existentes, Microsoft Direct3D 11 presenta el concepto de niveles de características. En este tema se describen los niveles de características de Direct3D.

Cada tarjeta de vídeo implementa un cierto nivel de funcionalidad de Microsoft DirectX (DX) en función de las unidades de procesamiento de gráficos (GPU) instaladas. En versiones anteriores de Microsoft Direct3D, podía averiguar la versión de Direct3D que la tarjeta de vídeo implementó y, después, programar la aplicación en consecuencia.

Con Direct3D 11, se introduce un nuevo paradigma denominado niveles de características. Un nivel de características es un conjunto bien definido de funcionalidades GPU. Por ejemplo, el \_ nivel de característica 9 1 implementa la funcionalidad que se implementó en Microsoft Direct3D 9, que expone las capacidades de los modelos de sombreador [PS \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-x.md) y [vs \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-vs-2-x.md), mientras que el \_ nivel de características 11 0 implementa la funcionalidad que se implementó en Direct3D 11.

Ahora, cuando cree un dispositivo, puede intentar crear un dispositivo para el nivel de característica que desea solicitar. Si la creación del dispositivo funciona, ese nivel de característica existe, de lo contrario, el hardware no admite ese nivel de características. Puede intentar volver a crear un dispositivo en un nivel de características inferior o puede salir de la aplicación. Para obtener más información sobre la creación de un dispositivo, consulte la función [**D3D11CreateDevice**](/windows/win32/api/D3D11/nf-d3d11-d3d11createdevice) .

Con los niveles de características, puede desarrollar una aplicación para Direct3D 9, Microsoft Direct3D 10 o Direct3D 11 y, a continuación, ejecutarla en el hardware de 9, 10 u 11 (con algunas excepciones; por ejemplo, las nuevas 11 características no se ejecutarán en una tarjeta 9 existente). Este es un par de otras propiedades básicas de los niveles de características:

- Una GPU que permite crear un dispositivo cumple o supera la funcionalidad de dicho nivel de características.
- Un nivel de característica siempre incluye la funcionalidad de niveles de características anteriores o inferiores.
- Un nivel de característica no implica el rendimiento, solo la funcionalidad. El rendimiento depende de la implementación de hardware.
- Elija un nivel de característica al crear un dispositivo Direct3D 11.

Para obtener información sobre las limitaciones de la creación de dispositivos que no son de tipo hardware en determinados niveles de características, vea [limitaciones para crear dispositivos](overviews-direct3d-11-devices-limitations.md)de hipertexto y de referencia.

Para ayudarle a decidir qué nivel de característica diseñar, compare las características de cada nivel de característica.

En la sección de [referencia de 10Level9 se](d3d11-graphics-reference-10level9.md) enumeran las diferencias entre el comportamiento de varios métodos [**ID3D11Device**](/windows/win32/api/D3D11/nn-d3d11-id3d11device) y [**ID3D11DeviceContext**](/windows/win32/api/D3D11/nn-d3d11-id3d11devicecontext) en distintos niveles de características de 10Level9.

## <a name="formats-of-version-numbers"></a>Formatos de números de versión

Existen tres formatos para las versiones de Direct3D, los modelos de sombreador y los niveles de características.

- Las versiones de Direct3D usan un punto; por ejemplo, Direct3D 12,0.
- Los modelos de sombreador usan un punto; por ejemplo, el modelo de sombreador 5,1.
- Los niveles de características usan un carácter de subrayado; por ejemplo, nivel de característica 12 \_ 0.

## <a name="feature-support-for-feature-levels-12_1-through-9_3"></a>Compatibilidad de características para los niveles de características de 12_1 a 9_3

Las siguientes características están disponibles para los niveles de características enumerados. Los encabezados de la fila superior son niveles de características de Direct3D. Los encabezados de la columna izquierda son características. Vea también [las notas al pie de las tablas](#footnotes-for-the-tables).

| Nivel de característica de características \\ | 12 \_ 1<sup>0</sup> | 12 \_ 0<sup>0</sup> | 11 \_ 1<sup>1</sup> | 11 \_ 0 | 10 \_ 1 | 10 \_ 0 | 9 \_ 3<sup>7</sup> |
|-|-|-|-|-|-|-|-|
| Modelo de sombreador (D3D11) | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 4.x | 4.0 | 2,0 (4 \_ 0 \_ nivel \_ 9 \_ 3) \[ vs \_ 2 \_ a/PS \_ 2 \_ x \] <sup>5</sup> |
| Modelo de sombreador (D3D12) | 5,1<sup>2</sup> | 5,1<sup>2</sup> | 5,1<sup>2</sup> | 5,1<sup>2</sup> | N/D | N/D | N/D |
| [Recursos en mosaico](tiled-resources.md) | Tier2<sup>6</sup> | Tier2<sup>6</sup> | Opcional | Opcional | No | No | No |
| [Rasterización conservadora](conservative-rasterization.md) | Tier1<sup>6</sup> | Opcional | Opcional | No | No | No | No |
| [Vistas de orden de rasterizador](rasterizer-order-views.md) | Sí | Opcional | Opcional | No | No | No | No |
| [Filtros mín./máx.](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | Sí | Sí | Opcional | No | No | No | No |
| Asignar búfer predeterminado | Opcional | Opcional | Opcional | Opcional | No | No | No |
| [Valor de la referencia de galería de símbolos especificado por el sombreador](shader-specified-stencil-reference-value.md) | Opcional | Opcional | Opcional | No | No | No | No |
| Cargas de vista de acceso no ordenada con tipo | 18 formatos, más opcionales | 18 formatos, más opcionales | 3 formatos, más opcionales | 3 formatos, más opcionales | No | No | No |
| [Sombreador de geometría](/previous-versions/bb205146(v=vs.85)) | Sí | Sí | Sí | Sí | Sí | Sí | No |
| [Transmisión por secuencias](./d3d10-graphics-programming-guide-output-stream-stage.md) | Sí | Sí | Sí | Sí | Sí | Sí | No |
| [DirectCompute/sombreador de cálculo](direct3d-11-advanced-stages-compute-shader.md) | Sí | Sí | Sí | Sí | Opcional | Opcional | N/D |
| <b>Nivel de característica de características \\</b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| [Sombreadores de casco y de dominio](direct3d-11-advanced-stages-tessellation.md) | Sí | Sí | Sí | Sí | No | No | No |
| [Matrices de recursos de textura](overviews-direct3d-11-resources-textures-intro.md) | Sí | Sí | Sí | Sí | Sí | Sí | No |
| [Matrices de recursos mapa](overviews-direct3d-11-resources-textures-intro.md) | Sí | Sí | Sí | Sí | Sí | No | No |
| [Compresión las texturas BC4/BC5](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | Sí | Sí | Sí | Sí | Sí | Sí | No |
| [Compresión BC6H/BC7](texture-block-compression-in-direct3d-11.md) | Sí | Sí | Sí | Sí | No | No | No |
| [Alfa a cobertura](./d3d10-graphics-programming-guide-blend-state.md) | Sí | Sí | Sí | Sí | Sí | Sí | No |
| [Formatos extendidos (BGRA, etc.)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sí | Sí | Sí | Sí | Opcional | Opcionales | Sí |
| [Formato de color de alta densidad XR de 10 bits](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sí | Sí | Sí | Sí | Opcional | Opcional | N/D |
| [Operaciones lógicas (fusión de salida)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Sí | Sí | Sí | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | No |
| Rasterización independiente del destino | Sí | Sí | Sí | No | No | No | No |
| [Destino de representación múltiple (MRT) con ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Sí | Sí | Sí | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | No |
| Ranuras UAV | 64 | 64 | 64 | 8 | 1 | 1 | N/D |
| <b>Nivel de característica de características \\</b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| UAVs en cada fase | Sí | Sí | Sí | No | No | No | N/D |
| [Recuento de muestras forzadas máximas para la representación solo UAV](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 16 | 16 | 16 | 8 | N/D | N/D | N/D |
| Compensación de búfer de constantes y actualizaciones parciales | Sí | Sí | Sí | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Sí<sup>1</sup> |
| formatos de 16 bits por píxel (BPP) | Sí | Sí | Sí | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> |
| Dimensión de textura máxima | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Dimensión mapa máxima | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Extensión de volumen máxima | 2048 | 2048 | 2048 | 2048 | 2048 | 2048 | 256 |
| Repetición de textura máxima | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 8192 |
| Anisotropía máx. | 16 | 16 | 16 | 16 | 16 | 16 | 16 |
| Recuento máximo de primitivas | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 1048575 |
| Índice de vértice máximo | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 1048575 |
| Máximo de ranuras de entrada | 32 | 32 | 32 | 32 | 32 | 16 | 16 |
| Destinos de representación simultáneos | 8 | 8 | 8 | 8 | 8 | 8 | 4 |
| Consultas de oclusión | Sí | Sí | Sí | Sí | Sí | Sí | Sí |
| <b>Nivel de característica de características \\</b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| Combinación alfa independiente | Sí | Sí | Sí | Sí | Sí | Sí | Sí |
| Reflejar una vez | Sí | Sí | Sí | Sí | Sí | Sí | Sí |
| Elementos de vértice superpuestos | Sí | Sí | Sí | Sí | Sí | Sí | Sí |
| Máscaras de escritura independientes | Sí | Sí | Sí | Sí | Sí | Sí | Sí |
| Instancing | Sí | Sí | Sí | Sí | Sí | Sí | Sí<sup>7</sup> |
| No potencias-de-2 condicionalmente<sup>3</sup> | No | No | No | No | No | No | Sí |
| No potencias-de-2 incondicionalmente<sup>4</sup> | Sí | Sí | Sí | Sí | Sí | Sí | No |

## <a name="feature-support-for-feature-levels-9_2-and-9_1"></a>Compatibilidad de características para los niveles de características 9_2 y 9_1

Las siguientes características están disponibles para los niveles de características enumerados. Los encabezados de la fila superior son niveles de características de Direct3D. Los encabezados de la columna izquierda son características. Vea también [las notas al pie de las tablas](#footnotes-for-the-tables).

| Nivel de característica de características \\ | 9 \_ 2 | 9 \_ 1 |
|-|-|-|
| Modelo de sombreador (D3D11) | 2,0 (4 \_ 0 \_ nivel \_ 9 \_ 1) | 2,0 (4 \_ 0 \_ nivel \_ 9 \_ 1) |
| Modelo de sombreador (D3D12) | N/D | N/D |
| [Recursos en mosaico](tiled-resources.md) | No | No |
| [Rasterización conservadora](conservative-rasterization.md) | No | No |
| [Vistas de orden de rasterizador](rasterizer-order-views.md) | No | No |
| [Filtros mín./máx.](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | No | No |
| Asignar búfer predeterminado | No | No |
| [Valor de la referencia de galería de símbolos especificado por el sombreador](shader-specified-stencil-reference-value.md) | No | No |
| Cargas de vista de acceso no ordenada con tipo | No | No |
| [Sombreador de geometría](/previous-versions/bb205146(v=vs.85)) | No | No |
| [Transmisión por secuencias](./d3d10-graphics-programming-guide-output-stream-stage.md) | No | No |
| [DirectCompute/sombreador de cálculo](direct3d-11-advanced-stages-compute-shader.md) | N/D | N/D |
| [Sombreadores de casco y de dominio](direct3d-11-advanced-stages-tessellation.md) | No | No |
| [Matrices de recursos de textura](overviews-direct3d-11-resources-textures-intro.md) | No | No |
| [Matrices de recursos mapa](overviews-direct3d-11-resources-textures-intro.md) | No | No |
| [Compresión las texturas BC4/BC5](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | No | No |
| <b>Nivel de característica de características \\</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| [Compresión BC6H/BC7](texture-block-compression-in-direct3d-11.md) | No | No |
| [Alfa a cobertura](./d3d10-graphics-programming-guide-blend-state.md) | No | No |
| [Formatos extendidos (BGRA, etc.)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sí | Sí |
| [Formato de color de alta densidad XR de 10 bits](overviews-direct3d-11-devices-downlevel-exceptions.md) | N/D | N/D |
| [Operaciones lógicas (fusión de salida)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | No | No |
| Rasterización independiente del destino | No | No |
| [Destino de representación múltiple (MRT) con ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | No | No |
| Ranuras UAV | N/D | N/D |
| UAVs en cada fase | N/D | N/D |
| [Recuento de muestras forzadas máximas para la representación solo UAV](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | N/D | N/D |
| Compensación de búfer de constantes y actualizaciones parciales | Sí<sup>1</sup> | Sí<sup>1</sup> |
| formatos de 16 bits por píxel (BPP) | Opcional<sup>1</sup> | Opcional<sup>1</sup> |
| Dimensión de textura máxima | 2048 | 2048 |
| Dimensión mapa máxima | 512 | 512 |
| Extensión de volumen máxima | 256 | 256 |
| Repetición de textura máxima | 2048 | 128 |
| <b>Nivel de característica de características \\</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| Anisotropía máx. | 16 | 2 |
| Recuento máximo de primitivas | 1048575 | 65535 |
| Índice de vértice máximo | 1048575 | 65534 |
| Máximo de ranuras de entrada | 16 | 16 |
| Destinos de representación simultáneos | 1 | 1 |
| Consultas de oclusión | Sí | No |
| Combinación alfa independiente | Sí | No |
| Reflejar una vez | Sí | No |
| Elementos de vértice superpuestos | Sí | No |
| Máscaras de escritura independientes | No | No |
| Instancing | No | No |
| No potencias-de-2 condicionalmente<sup>3</sup> | Sí | Sí |
| No potencias-de-2 incondicionalmente<sup>4</sup> | No | No |

## <a name="footnotes-for-the-tables"></a>Notas a pie de tabla

<sup>0</sup> requiere el tiempo de ejecución de Direct3D 11,3 o Direct3D 12.

<sup>1</sup> requiere el tiempo de ejecución de Direct3D 11,1.

<sup>2</sup> el modelo de sombreador 5,0 y versiones posteriores pueden admitir opcionalmente los sombreadores de doble precisión, los sombreadores de doble precisión extendidos, la instrucción del sombreador **SAD4** y los sombreadores de precisión parcial. Para determinar las opciones del modelo de sombreador 5,0 que están disponibles para DirectX 11, llame a [**ID3D11Device:: CheckFeatureSupport**](/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Cierta compatibilidad depende del hardware en el que se ejecute. El modelo de sombreador 5,1 y versiones posteriores solo se admiten a través de la API de DirectX 12, independientemente del nivel de característica que se esté usando. DirectX 11 solo admite hasta el modelo de sombreador 5,0. La API de DirectX 12 solo deja de funcionar hasta el nivel de características 11 \_ 0.

<sup>3</sup> en los niveles de características 9 \_ 1, 9 \_ 2 y 9 \_ 3, el dispositivo de pantalla admite el uso de texturas 2D con dimensiones que no son potencias de dos en dos condiciones. En primer lugar, solo se puede crear un nivel de mapa de MIP para cada textura y, en segundo lugar, no se permiten los modos de muestra de ajuste para las texturas (es decir, los miembros **AddressU**, **AddressV** y **AddressW** de la [**muestra de D3D11 \_ \_**](/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc) no se pueden establecer en [**D3D11 \_ Texture \_ Address \_ Wrap**](/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode)).

<sup>4</sup> en los niveles de características 10 \_ 0, 10 \_ 1 y 11 \_ 0, el dispositivo de pantalla admite incondicionalmente el uso de texturas 2D con dimensiones que no son potencias de dos.

<sup>5</sup> sombreador de vértices 2A con las instrucciones 256, 32 registros temporales, control de flujo estático de profundidad 4, control de flujo dinámico de profundidad 24 y D3DVS20CAPS \_ PREDICATION. Sombreador de píxeles 2x con instrucciones 512, 32 registros temporales, control de flujo estático de profundidad 4, control de flujo dinámico de profundidad 24, D3DPS20CAPS \_ ARBITRARYSWIZZLE, D3DPS20CAPS \_ GRADIENTINSTRUCTIONS, D3DPS20CAPS \_ PREDICATION, D3DPS20CAPS \_ NODEPENDENTREADLIMIT y D3DPS20CAPS \_ NOTEXINSTRUCTIONLIMIT.

<sup>6</sup> niveles superiores opcionales.

<sup>7</sup> para 9_3 de nivel de característica, los únicos métodos de representación admitidos son **Draw**, **DrawIndexed** y **DrawIndexInstanced**. Además para 9_3 de nivel de características, la representación de lista de puntos solo se admite para la representación a través de **Draw**.

Para más información sobre la compatibilidad con formatos en diferentes niveles de características de hardware, consulte:

- [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 12,1](../direct3ddxgi/hardware-support-for-direct3d-12-1-formats.md)
- [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 12,0](../direct3ddxgi/hardware-support-for-direct3d-12-0-formats.md)
- [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 11,1](../direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware.md)
- [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 11,0](../direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware.md)
- [Compatibilidad de hardware con formatos 10Level9 de Direct3D](/previous-versions/ff471324(v=vs.85))
- [Compatibilidad de hardware con formatos de Direct3D 10,1](/previous-versions/cc627091(v=vs.85))
- [Compatibilidad de hardware con formatos de Direct3D 10](/previous-versions/cc627090(v=vs.85))

## <a name="related-topics"></a>Temas relacionados

* [Direct3D 11 en hardware de nivel inferior](overviews-direct3d-11-devices-downlevel.md)
* [Niveles de características de hardware (Direct3D 12)](../direct3d12/hardware-feature-levels.md)
