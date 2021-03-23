---
title: Ejemplos de trabajo
description: Los ejemplos de trabajo están disponibles para su descarga, mostrando el uso de una serie de características de Direct3D 12.
ms.assetid: 4C4475D4-534F-484F-8D60-9ACEA09AC109
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1b61ec374e21c9173797121ee90ec72e789de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103432"
---
# <a name="working-samples"></a>Ejemplos de trabajo

Los ejemplos de trabajo están disponibles para su descarga, mostrando el uso de una serie de características de Direct3D 12.

## <a name="working-samples"></a>Ejemplos de trabajo

Los ejemplos de trabajo (en forma de proyectos de Visual Studio 2015) se pueden descargar desde [GitHub/Microsoft/DirectX-Graphics-samples](https://github.com/Microsoft/DirectX-Graphics-Samples).

> [!Note]  
> La lista exacta de ejemplos disponibles en esta ubicación variará a medida que se agreguen y actualicen los ejemplos.

 



<table>
<thead>
<tr class="header">
<th>Título de ejemplo</th>
<th>Descripción</th>
<th>Escritorio</th>
<th>UWP</th>
<th>Ejemplo paso a paso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>HelloWorld<dl> HelloWindow<br />
HelloTriangle<br />
HelloBundles<br />
HelloConstBuffers<br />
HelloTexture<br />
</dl></td>
<td>El conjunto de ejemplo HelloWorld contiene los siguientes proyectos sencillos que le ayudarán a empezar a usar Direct3D 12.<dl> Crea una ventana para preparar la representación del contenido de Direct3D 12.<br />
Representa un triángulo simple mediante Direct3D 12.<br />
Muestra el uso de un paquete para su representación con Direct3D 12.<br />
Muestra cómo usar búferes de constantes para pasar datos a la GPU que se usa para la representación en Direct3D 12.<br />
Muestra cómo aplicar una textura a un triángulo mediante Direct3D 12.<br />
</dl></td>
<td>Y</td>
<td>Y</td>
<td><a href="creating-a-basic-direct3d-12-component.md">Crear un componente básico de Direct3D 12</a></td>
</tr>
<tr class="even">
<td>D3D12Bundles</td>
<td>Muestra procedimientos recomendados de búfer de fotogramas y sincronización, así como la representación de una malla simple mediante paquetes.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="odd">
<td>D3D12Multithreading</td>
<td>Un ejemplo de cómo crear una aplicación compatible con multiproceso.</td>
<td>Y</td>
<td>N</td>

</tr>
<tr class="even">
<td>D3D12nBodyGravity</td>
<td>Muestra cómo se puede usar varios motores para realizar trabajos de proceso asincrónicos junto con el trabajo 3D en la misma GPU.</td>
<td>Y</td>
<td>Y</td>
<td><a href="multi-engine-n-body-gravity-simulation.md">Simulación de la gravedad n-Body de varios motores</a></td>
</tr>
<tr class="odd">
<td>D3D12PredicationQueries</td>
<td>Muestra la selección de la oclusión mediante montones de consulta y predication.</td>
<td>Y</td>
<td>Y</td>
<td><a href="predication-queries.md">Consultas de Predication</a></td>
</tr>
<tr class="even">
<td>D3D12DynamicIndexing</td>
<td>Muestra las capacidades de indexación dinámica de DirectX 12 y HLSL.</td>
<td>Y</td>
<td>Y</td>
<td><a href="dynamic-indexing-using-hlsl-5-1.md">Indexado dinámico mediante HLSL 5.1</a></td>
</tr>
<tr class="odd">
<td>D3D1211on12</td>
<td>Muestra el uso básico de la capa 11on12. Este ejemplo representa el texto con D2D mediante la API de Direct3D 11 en un dispositivo 11on12 de Direct3D 12.</td>
<td>Y</td>
<td>Y</td>
<td><a href="d2d-using-d3d11on12.md">D2D con D3D11on12</a></td>
</tr>
<tr class="even">
<td>D3D12ExecuteIndirect</td>
<td>Muestra la selección del motor de proceso junto con la característica de ejecución indirecta para representar solo los objetos que pasan la prueba de selección.</td>
<td>Y</td>
<td>Y</td>
<td><a href="indirect-drawing-and-gpu-culling-.md">Dibujo indirecto y selección de GPU</a></td>
</tr>
<tr class="odd">
<td>D3D12PipelineStateCache</td>
<td>Muestra el almacenamiento en caché del objeto de estado de canalización (PSO).</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="even">
<td>D3D12Fullscreen</td>
<td>Muestra cómo controlar las transiciones en ventanas y el cambio de tamaño de las ventanas en DirectX 12.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="odd">
<td>D3D12HeterogeneousMultiadapter</td>
<td>Muestra cómo compartir cargas de trabajo entre varias GPU heterogéneas mediante montones compartidos.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="even">
<td>D3D12ReservedResources</td>
<td>Muestra el uso de recursos reservados (en mosaico). En este ejemplo, un cuádruple está texturizado con un recurso reservado que contiene una cadena de MIP completa.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="odd">
<td>D3D12Residency</td>
<td>Esto está pensado como una solución de bajo costo de integración para administrar los montones de Direct3D 12 y los recursos confirmados mediante técnicas de administración de memoria de Direct3D 11.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="even">
<td>D3D12SmallResources</td>
<td>Muestra el uso de pequeños recursos colocados, que muestran el posible ahorro de memoria obtenido mediante recursos colocados (con una alineación de 4K) sobre recursos comprometidos y reservados (con una alineación de 64K).</td>
<td>Y</td>
<td>Y</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Tutoriales de código D3D12](d3d12-code-walk-throughs.md)
</dt> </dl>

 

 




