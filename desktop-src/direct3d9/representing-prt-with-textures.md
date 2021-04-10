---
description: El ejemplo PRTDemo y el simulador PRTCmdLine incluidos en el SDK de DirectX representan vectores de transferencia en los vértices de una malla.
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: Representar PRT con texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4647cfc85451ede9507e007ed556a203a3cd890a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274784"
---
# <a name="representing-prt-with-textures-direct3d-9"></a>Representar PRT con texturas (Direct3D 9)

El ejemplo PRTDemo y el simulador PRTCmdLine incluidos en el SDK de DirectX representan vectores de transferencia en los vértices de una malla. Para representar la señal de PRT con precisión, esto puede requerir teselaciones que podrían no ser prácticas para los juegos actuales. Representar vectores de transferencia en mapas de textura es un enfoque alternativo que tiene el mismo costo de datos independiente de la complejidad de la malla. Hay varias maneras de generar mapas de textura vectoriales de transferencia mediante la biblioteca de D3DX PRT.

## <a name="precomputing-transfer-vectors"></a>Computación de vectores de transferencia

Un enfoque sería modificar los ejemplos PRTDemo y PRTCmdLine para calcular un vector de transferencia en cada textura en una parametrización de una superficie. Para hacerlo:

1.  Modifique la llamada a [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) para extraer las coordenadas de textura de la malla (ExtractUVs debe ser **true**)
2.  Reemplace las llamadas a [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) por [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) con el mismo tamaño de textura.

Todos los métodos de ID3DXPRTEngine funcionan con simulaciones por textura, excepto: ComputeBounceAdaptive, ComputeSSAdaptive, Compute y ComputeDirectLightingSHAdaptive. Aunque la simulación de espacio de textura generará el resultado correcto, a menudo puede ser bastante lento, ya que lo más probable es que el cálculo de los vectores de transferencia a una alta densidad.

Otro enfoque consiste en calcular una simulación de PRT adaptable por vértice (con coordenadas de textura que se usarán para los datos por textura) y, a continuación, llamar a [**ID3DXPRTEngine:: ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (mediante un búfer de salida creado con [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) en la resolución adecuada). Esto funciona con toda la funcionalidad de D3DX PRT en el SDK y a menudo puede ser mucho más eficaz que calcular directamente un búfer de transferencia por textura.

## <a name="runtime-calculations"></a>Cálculos en tiempo de ejecución

Si se usa un solo clúster, los resultados se pueden filtrar y mapas MIP como cualquier otra textura y el sombreador de píxeles es idéntico al código del sombreador de vértices que se distribuye con PRTDemo.

Si la compresión genera varios clústeres, no se pueden filtrar o adquierer los datos porque los índices de agrupación en clústeres no son continuos. Estas son algunas alternativas para administrar datos en clúster múltiple:

-   Realice todo el filtrado en el sombreador de píxeles. Desafortunadamente, esto generalmente no es práctico por motivos de rendimiento.
-   Si las texturas tienen texturas de baja resolución no asignadas a MIP (es decir, mapas ligeros), lo más probable es que solo calcule la iluminación directamente en el espacio de textura, donde no se producirá ningún filtrado y represente el objeto con una textura sombreada. Es esencialmente un mapa dinámico de luz que se crea completamente en la GPU.
-   Si se usa un Atlas de textura (consulte [uso de UVAtlas (Direct3D 9)](using-uvatlas.md)), puede agrupar manualmente la escena con todos los vectores de transferencia de un componente conectado en el espacio de textura en el mismo clúster. De este modo, puede filtrar la textura porque todos los textura a los que se tiene acceso estarán en el mismo clúster mediante la construcción. El identificador de clúster para una esfera determinada podría propagarse desde el sombreador de vértices.

Los sombreadores de píxeles tienen muchos menos registros constantes que no se pueden indizar, por lo que el sombreador de píxeles es algo diferente que el sombreador de vértices. Almacenar el trabajo por clúster en una textura dinámica de baja resolución y usar cargas de textura sería la manera más eficaz de representar cuando se usan varios clústeres.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferencia Radiance precalculada](precomputed-radiance-transfer.md)
</dt> <dt>

[Ejemplo de demostración de PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)
</dt> <dt>

[Simulador PRT (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)
</dt> </dl>

 

 



