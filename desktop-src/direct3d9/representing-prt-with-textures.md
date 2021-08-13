---
description: El ejemplo PRTDemo y el simulador PRTCmdLine incluidos en el SDK de DirectX representan vectores de transferencia en los vértices de una malla.
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: Representar PRT con texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e827e24258d75a91aa75c9eb51ed6563d476ab16f75fedc31a7071bca28a4a78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797930"
---
# <a name="representing-prt-with-textures-direct3d-9"></a>Representar PRT con texturas (Direct3D 9)

El ejemplo PRTDemo y el simulador PRTCmdLine incluidos en el SDK de DirectX representan vectores de transferencia en los vértices de una malla. Para representar la señal PRT con precisión, esto puede requerir teselaciones que pueden ser poco prácticas para los juegos actuales. La representación de vectores de transferencia en mapas de textura es un enfoque alternativo que tiene el mismo costo de datos independientemente de la complejidad de la malla. Hay varias maneras de generar mapas de textura de vector de transferencia mediante la biblioteca PRT D3DX.

## <a name="precomputing-transfer-vectors"></a>Calcular previamente vectores de transferencia

Un enfoque sería modificar los ejemplos PRTDemo y PRTCmdLine para calcular un vector de transferencia en cada elemento de textura en una parametrización de una superficie. Para ello, siga estos pasos:

1.  Modifique la llamada a [**D3DXCreatePRTEngine para**](d3dxcreateprtengine.md) extraer las coordenadas de textura de la malla (ExtractUVs debe ser **TRUE)**
2.  Reemplace [**las llamadas D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) por [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) con el mismo tamaño de textura.

Todos los métodos ID3DXPRTEngine funcionan con simulaciones por texel, excepto: ComputeBounceAdaptive, ComputeSSAdaptive, ComputeSS y ComputeDirectLightingSHAdaptive. Aunque la simulación de espacio de textura generará el resultado correcto, a menudo puede ser bastante lento, ya que lo más probable es que esté computando vectores de transferencia a una alta densidad.

Otro enfoque consiste en calcular una simulación de PRT adaptable por vértice (con coordenadas de textura que se usarán para los datos por elemento de textura) y, a continuación, llamar a [**ID3DXPRTEngine::ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (mediante un búfer de salida creado mediante [**D3DXCreatePRTBufferTex en**](d3dxcreateprtbuffertex.md) la resolución adecuada). Esto funciona con todas las funcionalidades de PRT D3DX del SDK y a menudo puede ser mucho más eficaz que calcular directamente un búfer de transferencia por textura.

## <a name="runtime-calculations"></a>Cálculos en tiempo de ejecución

Si se usa un único clúster, los resultados se pueden filtrar y asignar a mip como cualquier otra textura y el sombreador de píxeles es idéntico al código del sombreador de vértices que se incluye con PRTDemo.

Si la compresión genera varios clústeres, no puede filtrar ni asignar mipmap los datos porque los índices de agrupación en clústeres no son continuos. Estas son algunas alternativas para controlar datos de varios clústeres:

-   Realice todo el filtrado usted mismo en el sombreador de píxeles. Desafortunadamente, esto suele ser poco práctico por motivos de rendimiento.
-   Si las texturas son texturas no asignadas a mip de baja resolución (es decir, mapas claros), lo más probable es que sea más eficaz calcular la iluminación directamente en el espacio de textura , donde no se producirá ningún filtrado, y representar el objeto con una textura sombreada. Se trata básicamente de un mapa de luz dinámico que se crea completamente en la GPU.
-   Si se usa un atlas de textura (consulte Uso de [UVAtlas (Direct3D 9)](using-uvatlas.md)), puede agrupar manualmente la escena haciendo que todos los vectores de transferencia de un componente conectado en el espacio de textura estén en el mismo clúster. De este modo, puede filtrar la textura porque todos los elementos de textura a los que se tiene acceso estarían en el mismo clúster por construcción. El identificador de clúster de una cara determinada se podría propagar desde el sombreador de vértices.

Los sombreadores de píxeles tienen muchos menos registros constantes que no se pueden indexar, por lo que el sombreador de píxeles es algo diferente al sombreador de vértices. Almacenar el trabajo por clúster en una textura dinámica de baja resolución y usar cargas de textura sería la manera más eficaz de representar cuando se usan varios clústeres.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferencia de radiancia precalcalada](precomputed-radiance-transfer.md)
</dt> <dt>

[Ejemplo de demostración de PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)
</dt> <dt>

[Simulador de PRT (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)
</dt> </dl>

 

 



