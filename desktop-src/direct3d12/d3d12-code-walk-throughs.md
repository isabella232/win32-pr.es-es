---
title: Tutoriales de código D3D12
description: En esta sección se proporciona código para escenarios de ejemplo. Muchos de los recorridos proporcionan detalles sobre qué codificación es necesario agregar a un ejemplo básico, para evitar repetir el código de componente básico para cada escenario.
ms.assetid: 1F37FD3A-385C-4DD5-B04C-980F078D90D0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdea9b519e2a0adac9dc346d6bee455af0018da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359827"
---
# <a name="d3d12-code-walk-throughs"></a>Tutoriales de código D3D12

En esta sección se proporciona código para escenarios de ejemplo. Muchos de los recorridos proporcionan detalles sobre qué codificación es necesario agregar a un ejemplo básico, para evitar repetir el código de componente básico para cada escenario.

Para obtener el componente más básico, consulte la sección Creación de un componente básico de [Direct3D 12.](creating-a-basic-direct3d-12-component.md) En los siguientes pasos se describen escenarios más avanzados.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [D2D con D3D11on12](d2d-using-d3d11on12.md)<br/>                                       | El **ejemplo D3D1211on12** muestra cómo representar contenido D2D sobre contenido D3D12 mediante el uso compartido de recursos entre un dispositivo basado en 11 y un dispositivo basado en 12. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Simulación de la gravedad de n-cuerpos de varios motores](multi-engine-n-body-gravity-simulation.md)<br/> | El **ejemplo D3D12nBodyGravity** muestra cómo realizar el trabajo de proceso de forma asincrónica. El ejemplo pone en marcha varios subprocesos cada uno con una cola de comandos de proceso y programa el trabajo de proceso en la GPU que realiza una simulación de gravedad de n cuerpos. Cada subproceso funciona en dos búferes llenos de datos de posición y velocidad. Con cada iteración, el sombreador de proceso lee los datos de posición y velocidad actuales de un búfer y escribe la siguiente iteración en el otro búfer. Cuando se completa la iteración, el sombreador de proceso intercambia qué búfer es el SRV para leer los datos de posición/velocidad y cuál es el UAV para escribir actualizaciones de posición/velocidad cambiando el estado de los recursos en cada búfer.<br/> |
| [Consultas de predicación](predication-queries.md)<br/>                                       | El **ejemplo D3D12PredicationQueries** muestra la selección de oclusión mediante montones de consultas y predicados de DirectX 12. En el tutorial se describe el código adicional necesario para ampliar el ejemplo **HelloConstBuffer** para controlar las consultas de predicado. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Indexado dinámico mediante HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)<br/>               | El ejemplo **D3D12DynamicIndexing** muestra algunas de las nuevas características HLSL disponibles en El modelo de sombreador 5.1, especialmente la indexación dinámica y las matrices sin enlazar, para representar la misma malla varias veces, cada vez que se representa con un material seleccionado dinámicamente. Con la indexación dinámica, los sombreadores ahora pueden indexar en una matriz sin conocer el valor del índice en tiempo de compilación. Cuando se combina con matrices sin enlazar, esto agrega otro nivel de direccionamiento indirecto y flexibilidad para los autores de sombreadores y las canalizaciones de arte.<br/>                                                                                                                                                                                  |
| [Dibujo indirecto y selección de GPU](indirect-drawing-and-gpu-culling-.md)<br/>            | El ejemplo D3D12ExecuteIndirect muestra cómo usar comandos indirectos para dibujar contenido. También muestra cómo se pueden manipular estos comandos en la GPU en un sombreador de proceso antes de que se emita. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

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

 

 





