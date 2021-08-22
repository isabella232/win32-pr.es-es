---
title: Stream-Output fase
description: El propósito de la fase stream-output es generar continuamente (o transmitir) datos de vértices desde la fase del sombreador de geometría (o la fase del sombreador de vértices si la fase del sombreador de geometría está inactiva) a uno o varios búferes en memoria (consulte Tareas iniciales con la fase Stream-Output).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- fase de salida de flujo (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f630208b60b107b211f8bb6f6ee0f1efac3ed736c96756dbe1e95e24032b02f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538579"
---
# <a name="stream-output-stage"></a>Stream-Output fase

El propósito de la fase stream-output es generar continuamente (o transmitir) datos de vértices desde la fase del sombreador de geometría (o la fase del sombreador de vértices si la fase del sombreador de geometría está inactiva) a uno o varios búferes en memoria (vea [Tareas iniciales con](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)la fase Stream-Output ).

La fase de salida de flujo (SO) se encuentra en la canalización justo después de la fase del sombreador de geometría y justo antes de la fase de rasterización, como se muestra en el diagrama siguiente.

![diagrama de la ubicación de la fase stream-output en la canalización](images/d3d10-pipeline-stages-so.png)

Los datos transmitidos a la memoria se pueden volver a leer en la canalización en un paso de representación posterior o se pueden copiar en un recurso de almacenamiento provisional (para que la CPU pueda leerlo). La cantidad de datos transmitidos por secuencias puede variar; LA API [**ID3D11DeviceContext::D rawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) está diseñada para controlar los datos sin necesidad de consultar (la GPU) sobre la cantidad de datos escritos.

Cuando se enlaza un triángulo o una franja de línea a la fase de ensamblador de entrada, cada franja se convierte en una lista antes de que se transmitan. Los vértices siempre se escriben como primitivos completos (por ejemplo, tres vértices a la vez para triángulos); las primitivas incompletas nunca se transmiten por secuencias. Los tipos primitivos con adyacencia descartan los datos de adyacencia antes de transmitir los datos.

Hay dos maneras de alimentar los datos de salida de flujo en la canalización:

-   Los datos de salida de flujo se pueden devolver a la fase de ensamblador de entrada.
-   Los sombreadores programables pueden leer los datos de salida de flujo mediante funciones de carga (como [Cargar).](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)

Para usar un búfer como recurso de salida de flujo, cree el búfer con la [**marca BIND STREAM OUTPUT \_ \_ \_ de D3D11.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) La fase de salida de flujo admite hasta 4 búferes simultáneamente.

-   Si está transmitiendo datos en varios búferes, cada búfer solo puede capturar un único elemento (hasta 4 componentes) de datos por vértice, con un paso de datos implícito igual al ancho del elemento en cada búfer (compatible con la forma en que los búferes de un solo elemento se pueden enlazar para la entrada en las fases del sombreador). Además, si los búferes tienen tamaños diferentes, la escritura se detiene en cuanto cualquiera de los búferes está lleno.
-   Si está transmitiendo datos a un solo búfer, el búfer puede capturar hasta 64 componentes escalares de datos por vértice (256 bytes o menos) o el paso del vértice puede ser de hasta 2048 bytes.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                               | Descripción                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Tareas iniciales con la fase Stream-Output de trabajo](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | En esta sección se describe cómo usar un sombreador de geometría con la fase de salida del flujo.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

