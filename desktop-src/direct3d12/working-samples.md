---
title: Ejemplos de trabajo
description: Hay ejemplos de trabajo disponibles para su descarga, en los que se muestra el uso de varias características de Direct3D 12.
ms.assetid: 4C4475D4-534F-484F-8D60-9ACEA09AC109
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1b61ec374e21c9173797121ee90ec72e789de8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567965"
---
# <a name="working-samples"></a>Ejemplos de trabajo

Hay ejemplos de trabajo disponibles para su descarga, en los que se muestra el uso de varias características de Direct3D 12.

## <a name="working-samples"></a>Ejemplos de trabajo

Los ejemplos de trabajo (en forma de Visual Studio proyectos de 2015) se pueden descargar de [GitHub/Microsoft/DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples).

> [!Note]  
> La lista exacta de muestras disponibles en esta ubicación variará a medida que se agregan y actualizan los ejemplos.

 



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
<td>El conjunto de ejemplo HelloWorld contiene los siguientes proyectos sencillos que le ayudarán a empezar a trabajar con Direct3D 12.<dl> Crea una ventana como preparación para representar contenido de Direct3D 12.<br />
Representa un triángulo simple mediante Direct3D 12.<br />
Muestra el uso de una agrupación para la representación mediante Direct3D 12.<br />
Muestra cómo usar búferes constantes para pasar datos a la GPU usada para la representación en Direct3D 12.<br />
Muestra cómo aplicar una textura a un triángulo mediante Direct3D 12.<br />
</dl></td>
<td>Y</td>
<td>Y</td>
<td><a href="creating-a-basic-direct3d-12-component.md">Crear un componente básico de Direct3D 12</a></td>
</tr>
<tr class="even">
<td>D3D12Bundles</td>
<td>Muestra los procedimientos recomendados de almacenamiento en búfer y sincronización de fotogramas, así como la representación de una malla simple mediante agrupaciones.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="odd">
<td>D3D12Multithreading</td>
<td>Un ejemplo de cómo compilar una aplicación compatible con multiproceso.</td>
<td>Y</td>
<td>N</td>

</tr>
<tr class="even">
<td>D3D12nBodyGravity</td>
<td>Muestra cómo se pueden usar varios motores para realizar el trabajo de proceso asincrónico junto con el trabajo 3D en la misma GPU.</td>
<td>Y</td>
<td>Y</td>
<td><a href="multi-engine-n-body-gravity-simulation.md">Simulación de la gravedad de n-cuerpos de varios motores</a></td>
</tr>
<tr class="odd">
<td>D3D12PredicationQueries</td>
<td>Muestra la selección de oclusión mediante montones de consultas y predicados.</td>
<td>Y</td>
<td>Y</td>
<td><a href="predication-queries.md">Consultas de predicación</a></td>
</tr>
<tr class="even">
<td>D3D12DynamicIndexing</td>
<td>Muestra las funcionalidades de indexación dinámica de DirectX 12 y HLSL.</td>
<td>Y</td>
<td>Y</td>
<td><a href="dynamic-indexing-using-hlsl-5-1.md">Indexado dinámico mediante HLSL 5.1</a></td>
</tr>
<tr class="odd">
<td>D3D1211on12</td>
<td>Muestra el uso básico de la capa 11on12. En este ejemplo se representa texto mediante D2D mediante la API de Direct3D 11 en un dispositivo Direct3D 12 11on12.</td>
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
<td>Muestra cómo controlar las transiciones de pantalla completa a las ventanas y el cambio de tamaño de ventana en DirectX 12.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="odd">
<td>D3D12HeterogeneousMultiadapter</td>
<td>Muestra cómo compartir cargas de trabajo entre varias GPU heterogéneos mediante montones compartidos.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="even">
<td>D3D12ReservedResources</td>
<td>Muestra el uso de recursos reservados (en mosaico). En este ejemplo, un cuadrándido se textura con un recurso reservado que contiene una cadena de mip completa.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="odd">
<td>D3D12Residency</td>
<td>Esto está pensado como una solución de bajo costo de integración para administrar los montones de Direct3D 12 y los recursos confirmados, mediante técnicas de administración de memoria de Direct3D 11.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="even">
<td>D3D12SmallResources</td>
<td>Muestra el uso de recursos pequeños colocados, lo que muestra el posible ahorro de memoria obtenido mediante los recursos colocados (con una alineación 4K) sobre los recursos confirmados y reservados (con una alineación de 64 000).</td>
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

 

 




