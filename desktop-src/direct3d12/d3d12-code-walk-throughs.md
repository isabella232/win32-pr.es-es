---
title: Walk-Throughs de código D3D12
description: En esta sección se proporciona código para escenarios de ejemplo. Muchos de los tutoriales proporcionan detalles sobre qué codificación se debe agregar a un ejemplo básico, para evitar repetir el código de componente básico para cada escenario.
ms.assetid: 1F37FD3A-385C-4DD5-B04C-980F078D90D0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdea9b519e2a0adac9dc346d6bee455af0018da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104192"
---
# <a name="d3d12-code-walk-throughs"></a>Walk-Throughs de código D3D12

En esta sección se proporciona código para escenarios de ejemplo. Muchos de los tutoriales proporcionan detalles sobre qué codificación se debe agregar a un ejemplo básico, para evitar repetir el código de componente básico para cada escenario.

Para el componente más básico, consulte la sección [creación de un componente básico de Direct3D 12](creating-a-basic-direct3d-12-component.md) . En los siguientes tutoriales se describen escenarios más avanzados.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [D2D con D3D11on12](d2d-using-d3d11on12.md)<br/>                                       | En el ejemplo **D3D1211on12** se muestra cómo representar el contenido de D2D sobre el contenido de D3D12 compartiendo recursos entre un dispositivo basado en 11 y un dispositivo basado en 12. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Simulación de la gravedad n-Body de varios motores](multi-engine-n-body-gravity-simulation.md)<br/> | En el ejemplo **D3D12nBodyGravity** se muestra cómo realizar el trabajo de proceso de forma asincrónica. El ejemplo pone en marcha un número de subprocesos con una cola de comandos de proceso y programa el trabajo de proceso en la GPU que realiza una simulación de gravedad n-Body. Cada subproceso opera en dos búferes llenos de datos de la posición y la velocidad. Con cada iteración, el sombreador de cálculo lee la posición actual y los datos de velocidad de un búfer y escribe la siguiente iteración en el otro búfer. Una vez completada la iteración, el sombreador de cálculo intercambia qué búfer es el SRV para leer los datos de posición/velocidad y cuál es el UAV para escribir las actualizaciones de posición/velocidad cambiando el estado del recurso en cada búfer.<br/> |
| [Consultas de Predication](predication-queries.md)<br/>                                       | En el ejemplo **D3D12PredicationQueries** se muestra la selección de la oclusión mediante montones de consulta de DirectX 12 y predication. En el tutorial se describe el código adicional necesario para extender el ejemplo **HelloConstBuffer** para controlar las consultas de predication. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Indexado dinámico mediante HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)<br/>               | En el ejemplo **D3D12DynamicIndexing** se muestran algunas de las nuevas características de HLSL disponibles en el modelo de sombreador 5,1, especialmente la indexación dinámica y las matrices sin enlazar, para representar la misma malla varias veces, cada una de ellas con un material seleccionado dinámicamente. Con la indexación dinámica, los sombreadores ahora pueden indexar en una matriz sin conocer el valor del índice en tiempo de compilación. Cuando se combina con matrices sin enlazar, agrega otro nivel de direccionamiento indirecto y flexibilidad para los autores del sombreador y las canalizaciones de arte.<br/>                                                                                                                                                                                  |
| [Dibujo indirecto y selección de GPU](indirect-drawing-and-gpu-culling-.md)<br/>            | En el ejemplo D3D12ExecuteIndirect se muestra cómo usar comandos indirectos para dibujar contenido. También muestra cómo se pueden manipular estos comandos en la GPU en un sombreador de cálculo antes de que se emitan. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Tutoriales de vídeo de aprendizaje avanzado de DirectX](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
</dt> <dt>

[Código de ejemplo en la referencia de D3D12](notes-on-example-code.md)
</dt> <dt>

[Ejemplos de trabajo](working-samples.md)
</dt> </dl>

 

 





