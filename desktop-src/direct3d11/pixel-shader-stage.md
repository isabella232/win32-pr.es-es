---
title: Fase del sombreador de píxeles
description: La fase del sombreador de píxeles (PS) permite técnicas de sombreado enriquecidas, como la iluminación por píxel y el procesamiento posterior.
ms.assetid: 09831B10-4FD1-41E7-8D81-5AA63DC90020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57142e9c32919a6959a7fac14bf544cca1dacd79
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149495"
---
# <a name="pixel-shader-stage"></a>Fase del sombreador de píxeles

La fase del sombreador de píxeles (PS) permite técnicas de sombreado enriquecidas, como la iluminación por píxel y el procesamiento posterior. Un sombreador de píxeles es un programa que combina variables constantes, datos de textura, valores interpolados por vértice y otros datos para generar salidas por píxel. La fase de rasterizador invoca un sombreador de píxeles una vez para cada píxel incluido en una primitiva; sin embargo, es posible especificar un sombreador **nulo** para evitar la ejecución de un sombreador.

## <a name="the-pixel-shader"></a>Sombreador de píxeles

Cuando se realiza un muestreo múltiple de una textura, se invoca un sombreador de píxeles una vez por cada uno de ellos, mientras que una prueba de profundidad/estarcido se produce para cada Multimuestra. Los ejemplos que superan la prueba de profundidad/estarcido se actualizan con el color de salida del sombreador de píxeles.

Las funciones intrínsecas del sombreador de píxeles producen o utilizan derivados de cantidades con respecto al espacio de pantalla x e y. El uso más común de los derivados es calcular los cálculos de nivel de detalle para el muestreo de textura y, en el caso del filtrado anisotrópico, seleccionar muestras a lo largo del eje de anisotropía. Normalmente, una implementación de hardware ejecuta un sombreador de píxeles en varios píxeles (por ejemplo, una cuadrícula de 2x2) simultáneamente, de modo que los derivados de cantidades calculadas en el sombreador de píxeles se pueden aproximar razonablemente como deltas de los valores en el mismo punto de ejecución en píxeles adyacentes.

### <a name="inputs"></a>Entradas

Cuando la canalización se configura sin un sombreador de geometría, un sombreador de píxeles se limita a 16, 32 bits, 4-entradas de componentes. De lo contrario, un sombreador de píxeles puede tardar hasta 32, 32 bits, 4-entradas de componente.

Los datos de entrada del sombreador de píxeles incluyen atributos de vértices (que se pueden interpolar con o sin corrección de perspectiva) o se pueden tratar como constantes por primitiva. Las entradas del sombreador de píxeles se interpolan a partir de los atributos de vértice de la primitiva que se está rasterizando, según el modo de interpolación declarado. Si una primitiva se recorta antes de la rasterización, también se respeta el modo de interpolación durante el proceso de recorte.

Los atributos de vértice se interpolan (o evalúan) en las ubicaciones del centro de sombreador de píxeles. Los modos de interpolación de atributo del sombreador de píxeles se declaran en una declaración de registro de entrada, por elemento, en un [argumento](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters) o en una [estructura de entrada](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-struct). Los atributos se pueden interpolar linealmente o con el [muestreo centroide](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx). La evaluación de centroide solo es relevante durante el muestreo múltiple para cubrir los casos en los que un píxel está cubierto por un primitivo, pero un centro de píxeles puede no ser; la evaluación de centroide se produce lo más cerca posible del centro de píxeles (no incluido).

Las entradas también se pueden declarar con una [semántica de valor del sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), que marca un parámetro consumido por otras fases de canalización. Por ejemplo, una posición en píxeles se debe marcar con la \_ semántica de la posición VP. La fase IA puede producir un escalar para un sombreador de píxeles (mediante \_ la VP PrimitiveID); la fase de rasterizador también puede generar un escalar para un sombreador de píxeles (con la VP \_ IsFrontFace).

### <a name="outputs"></a>Salidas

Un sombreador de píxeles puede generar un resultado de hasta 8, 32 bits, colores de cuatro componentes o ningún color si se descarta el píxel. Los componentes del registro de salida del sombreador de píxeles se deben declarar antes de poder usarlos. cada registro tiene permitida una máscara de salida-escritura distinta.

Use el estado de Depth-Write-Enable (en la fase de combinación de salida) para controlar si los datos de profundidad se escriben en un búfer de profundidad (o use la instrucción discard para descartar los datos de ese píxel). Un sombreador de píxeles también puede generar un valor de profundidad de punto flotante y de un componente de 32 bits opcional para las pruebas de profundidad (con la semántica de profundidad de la VP \_ ). El valor de profundidad se genera en el registro oDepth y reemplaza el valor de profundidad interpolada para las pruebas de profundidad (suponiendo que la prueba de profundidad está habilitada). No hay ninguna manera de cambiar de forma dinámica entre el uso de la profundidad de funciones fijas o del sombreador oDepth.

Un sombreador de píxeles no puede generar un valor de estarcido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 