---
title: Fase del sombreador de píxeles
description: La fase de sombreador de píxeles (PS) permite técnicas de sombreado enriquecciones, como la iluminación por píxel y el procesamiento posterior.
ms.assetid: 09831B10-4FD1-41E7-8D81-5AA63DC90020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd58bbc55bbc2fb7d590036bceb061f2a304c0be16ff058d04f226021dfe3cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988165"
---
# <a name="pixel-shader-stage"></a>Fase del sombreador de píxeles

La fase de sombreador de píxeles (PS) permite técnicas de sombreado enriquecciones, como la iluminación por píxel y el procesamiento posterior. Un sombreador de píxeles es un programa que combina variables constantes, datos de textura, valores interpolados por vértice y otros datos para generar salidas por píxel. La fase de rasterizador invoca un sombreador de píxeles una vez para cada píxel cubierto por un primitivo; sin embargo, es posible especificar un sombreador **NULL** para evitar la ejecución de un sombreador.

## <a name="the-pixel-shader"></a>Sombreador de píxeles

Cuando se multimuestrea una textura, se invoca un sombreador de píxeles una vez por píxel cubierto, mientras que se produce una prueba de profundidad o galería de símbolos para cada multimuestreo cubierto. Los ejemplos que pasan la prueba de profundidad o galería de símbolos se actualizan con el color de salida del sombreador de píxeles.

Las funciones intrínsecas del sombreador de píxeles generan o usan derivados de cantidades con respecto al espacio de pantalla x e y. El uso más común de los derivados es calcular cálculos de nivel de detalle para el muestreo de textura y, en el caso del filtrado anisotropico, seleccionar muestras a lo largo del eje de anisotropía. Normalmente, una implementación de hardware ejecuta un sombreador de píxeles en varios píxeles (por ejemplo, una cuadrícula de 2x2) simultáneamente, de modo que los derivados de las cantidades calculadas en el sombreador de píxeles se puedan aproximar razonablemente como diferencias de los valores en el mismo punto de ejecución en píxeles adyacentes.

### <a name="inputs"></a>Entradas

Cuando la canalización se configura sin un sombreador de geometría, un sombreador de píxeles se limita a 16 entradas de 32 bits y 4 componentes. De lo contrario, un sombreador de píxeles puede tardar hasta 32 entradas de 32, 32 bits y 4 componentes.

Los datos de entrada del sombreador de píxeles incluyen atributos de vértice (que se pueden interpolar con o sin corrección de perspectiva) o se pueden tratar como constantes por primitiva. Las entradas del sombreador de píxeles se interpolan a partir de los atributos de vértice de la primitiva que se va a rasterizar, en función del modo de interpolación declarado. Si se recorta una primitiva antes de la rasterización, también se respeta el modo de interpolación durante el proceso de recorte.

Los atributos de vértice se interpolan (o evalúan) en las ubicaciones centrales del sombreador de píxeles. Los modos de interpolación de atributos de sombreador de píxeles se declaran en una declaración de registro de entrada, por elemento en un [argumento](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters) o una [estructura de entrada](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-struct). Los atributos se pueden interpolar linealmente o con muestreo [centroide.](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) La evaluación de centroide solo es pertinente durante la multimuestreo para cubrir los casos en los que un píxel está cubierto por un primitivo, pero es posible que un centro de píxeles no lo sea. La evaluación de centroide se produce lo más cerca posible del centro de píxeles (no cubierto).

Las entradas también se pueden declarar con una semántica de valor del [sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), que marca un parámetro consumido por otras fases de canalización. Por ejemplo, una posición de píxel debe marcarse con la semántica de \_ la posición SV. La fase IA puede generar un escalar para un sombreador de píxeles (mediante SV PrimitiveID); la fase de rasterizador también puede generar un escalar para un sombreador de \_ píxeles (mediante SV \_ IsFrontFace).

### <a name="outputs"></a>Salidas

Un sombreador de píxeles puede generar hasta 8, 32 bits, colores de 4 componentes o ningún color si se descarta el píxel. Los componentes del registro de salida del sombreador de píxeles deben declararse antes de que se puedan usar; Cada registro se permite una máscara de salida y escritura distinta.

Use el estado depth-write-enable (habilitación de escritura en profundidad) (en la fase de fusión de salida) para controlar si los datos de profundidad se escriben en un búfer de profundidad (o use la instrucción de descarte para descartar los datos de ese píxel). Un sombreador de píxeles también puede generar un valor opcional de profundidad de 32 bits, un componente, punto flotante y profundidad para las pruebas de profundidad (mediante la semántica \_ de profundidad SV). El valor de profundidad se genera en el registro oDepth y reemplaza el valor de profundidad interpolado para las pruebas de profundidad (suponiendo que las pruebas de profundidad están habilitadas). No hay ninguna manera de cambiar dinámicamente entre usar la profundidad de función fija o el sombreador oDepth.

Un sombreador de píxeles no puede generar un valor de galería de símbolos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 