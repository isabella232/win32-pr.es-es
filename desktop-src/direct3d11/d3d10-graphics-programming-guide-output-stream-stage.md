---
title: Stream-Output fase
description: El propósito de la fase de salida de flujo es la salida continua (o secuencia) de datos de vértices de la fase del sombreador de geometría (o la fase del sombreador de vértices si la fase del sombreador de geometría está inactiva) en uno o varios búferes de la memoria (vea Introducción con la fase Stream-Output).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- fase de salida de flujo (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0879cde2ba2f1bb3ed9cc6121aaf378cd4af312
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488573"
---
# <a name="stream-output-stage"></a>Stream-Output fase

El propósito de la fase de salida de flujo es la salida continua (o secuencia) de datos de vértices de la fase del sombreador de geometría (o la fase del sombreador de vértices si la fase del sombreador de geometría está inactiva) en uno o varios búferes de la memoria (vea [Introducción con la fase Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).

La fase de salida de flujo (para) se encuentra en la canalización justo después de la fase de sombreador de geometría y justo antes de la fase de rasterización, como se muestra en el diagrama siguiente.

![diagrama de la ubicación de la fase de salida de flujo en la canalización](images/d3d10-pipeline-stages-so.png)

Los datos que se transmiten a la memoria se pueden volver a leer en la canalización en una fase de representación subsiguiente, o bien se pueden copiar en un recurso de almacenamiento provisional (de modo que la CPU pueda leerlos). La cantidad de datos transmitidos puede variar; la API [**ID3D11DeviceContext::D rawauto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) está diseñada para controlar los datos sin necesidad de consultar (la GPU) la cantidad de datos escritos.

Cuando un triángulo o una franja de líneas está enlazada a la fase del ensamblador de entrada, cada franja se convierte en una lista antes de que se transmitan. Los vértices siempre se escriben como tipos primitivos completos (por ejemplo, 3 vértices a la vez para triángulos). los primitivos incompletos nunca se transmiten por secuencias. Los tipos primitivos con adyacencias descartan los datos de adyacencia antes de la transmisión de datos.

Hay dos maneras de alimentar los datos de salida de flujo en la canalización:

-   Los datos de salida de flujo se pueden volver a alimentar en la fase de ensamblador de entrada.
-   Los datos de salida de flujo se pueden leer mediante sombreadores programables mediante funciones de carga (como la [carga](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).

Para usar un búfer como un recurso de salida de flujo, cree el búfer con la marca de [**\_ salida de \_ flujo \_ de enlace D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) . La fase Stream-Output admite hasta 4 búferes simultáneamente.

-   Si está transmitiendo datos en varios búferes, cada búfer solo puede capturar un único elemento (hasta 4 componentes) de datos por vértice, con un intervalo de datos implícito igual al ancho del elemento en cada búfer (compatible con la forma en que se pueden enlazar los búferes de un solo elemento para la entrada en fases del sombreador). Además, si los búferes tienen tamaños diferentes, la escritura se detiene en cuanto uno de los búferes esté lleno.
-   Si está transmitiendo datos en un solo búfer, el búfer puede capturar hasta 64 componentes escalares de datos por vértice (256 bytes o menos) o el intervalo de vértices puede tener hasta 2048 bytes.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                               | Descripción                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Introducción con la fase de Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | En esta sección se describe cómo usar un sombreador de geometría con la fase de salida de la secuencia.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

