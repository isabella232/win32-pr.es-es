---
title: Información general sobre el sombreador de proceso
description: Un sombreador de proceso es una fase de sombreador programable que expande Microsoft Direct3D 11 más allá de la programación de gráficos. La tecnología de sombreador de proceso también se conoce como tecnología DirectCompute.
ms.assetid: 02c1f98e-fdd6-49b0-b8b2-efbd472ab599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6167915a670b6dfb4fffae957ee0121e8e52f639463b0d1132be9dac3552fe9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566345"
---
# <a name="compute-shader-overview"></a>Información general sobre el sombreador de proceso

Un sombreador de proceso es una fase de sombreador programable que expande Microsoft Direct3D 11 más allá de la programación de gráficos. La tecnología de sombreador de proceso también se conoce como tecnología DirectCompute.

Al igual que otros sombreadores programables (sombreadores de vértices y geometría, por ejemplo), un sombreador de proceso se ha diseñado e implementado con [HLSL,](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) pero es justo donde termina la similitud. Un sombreador de proceso proporciona informática de uso general de alta velocidad y aprovecha el gran número de procesadores paralelos de la unidad de procesamiento gráfico (GPU). El sombreador de proceso proporciona características de uso compartido de memoria y sincronización de subprocesos para permitir métodos de programación en paralelo más eficaces. Llame al [**método ID3D11DeviceContext::D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch) o [**ID3D11DeviceContext::D ispatchIndirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect) para ejecutar comandos en un sombreador de proceso. Un sombreador de proceso se puede ejecutar en muchos subprocesos en paralelo.

## <a name="using-compute-shader-on-direct3d-10x-hardware"></a>Uso del sombreador de proceso en hardware direct3D 10.x

Un sombreador de proceso en Microsoft Direct3D 10 también se conoce como DirectCompute 4.x.

Si usa la API de Direct3D 11 y controladores [actualizados,](overviews-direct3d-11-devices-downlevel-intro.md) el hardware direct3D de nivel de características 10 y 10.1 puede admitir opcionalmente una forma limitada de DirectCompute que usa los perfiles cs \_ 4 0 y \_ cs \_ \_ 4 1. [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models) Cuando use DirectCompute en este hardware, tenga en cuenta las siguientes limitaciones:

-   El número máximo de subprocesos está limitado a D3D11 \_ CS \_ 4 \_ X THREAD GROUP MAX THREADS PER GROUP \_ \_ \_ \_ \_ \_ (768) por grupo.
-   La dimensión X e Y de **numthreads** está limitada a D3D11 \_ CS \_ 4 \_ X THREAD GROUP MAX X \_ \_ \_ \_ (768) y D3D11 \_ CS \_ 4 X THREAD GROUP \_ MAX Y \_ \_ \_ \_ (768).
-   La dimensión Z **de numthreads** está limitada a 1.
-   La dimensión Z de dispatch está limitada a D3D11 \_ CS \_ 4 \_ X DISPATCH MAX THREAD GROUPS IN Z DIMENSION \_ \_ \_ \_ \_ \_ \_ (1).
-   Solo se puede enlazar una vista de acceso desordenado al sombreador (D3D11 \_ CS \_ 4 \_ X \_ UAV \_ REGISTER COUNT es \_ 1).
-   Solo [los objetos RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)y [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)están disponibles como vistas de acceso desordenado.
-   Un subproceso solo puede acceder a su propia región en memoria compartida de grupo para escribir, aunque puede leer desde cualquier ubicación.
-   [SV \_ GroupIndex](/previous-versions/windows/desktop/legacy/ff471569(v=vs.85)) o [SV \_ GroupThreadID](/windows/desktop/direct3dhlsl/sv-groupthreadid) deben usarse al acceder a **la memoria compartida de** grupo para escribir.
-   **La memoria compartida de** grupo está limitada a 16 KB por grupo.
-   Un único subproceso se limita a una región de 256 bytes de **memoria compartida de** grupo para escritura.
-   No hay ninguna instrucción atómica disponible.
-   No hay valores de precisión doble disponibles.

## <a name="using-compute-shader-on-direct3d-11x-hardware"></a>Uso del sombreador de proceso en hardware direct3D 11.x

Un sombreador de proceso en Direct3D 11 también se conoce como DirectCompute 5.0.

Cuando use DirectCompute con perfiles cs \_ \_ 5 0, tenga en [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models)cuenta los siguientes elementos:

-   El número máximo de subprocesos está limitado a D3D11 \_ CS \_ THREAD GROUP MAX THREADS PER GROUP \_ \_ \_ \_ \_ (1024) por grupo.
-   La dimensión X e Y de **numthreads** está limitada a D3D11 \_ CS \_ THREAD GROUP MAX X \_ \_ \_ (1024) y D3D11 \_ CS THREAD GROUP MAX \_ Y \_ \_ \_ (1024).
-   La dimensión Z **de numthreads está** limitada a D3D11 \_ CS THREAD GROUP MAX \_ Z \_ \_ \_ (64).
-   La dimensión máxima de distribución está limitada a D3D11 \_ CS \_ DISPATCH MAX THREAD GROUPS PER DIMENSION \_ \_ \_ \_ \_ (65535).
-   El número máximo de vistas de acceso desordenado que se pueden enlazar a un sombreador es D3D11 \_ PS \_ CS \_ UAV \_ REGISTER COUNT \_ (8).
-   Admite [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s, [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s y vistas de acceso sin ordenar con tipo[(RWTexture1D,](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d) [RWTexture2D,](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d) [RWTexture3D,](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)y así sucesivamente).
-   Hay instrucciones atómicas disponibles.
-   La compatibilidad con la precisión doble puede estar disponible. Para obtener información sobre cómo determinar si la precisión doble está disponible, vea [**D3D11 \_ FEATURE \_ DOUBLES**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                              | Descripción                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nuevos tipos de recursos](direct3d-11-advanced-stages-cs-resources.md)<br/>      | Se han agregado varios tipos de recursos nuevos en Direct3D 11.<br/>                                                                                                                                                                                                 |
| [Acceso a recursos](direct3d-11-advanced-stages-cs-access.md)<br/>        | Hay varias maneras de acceder a [los recursos](overviews-direct3d-11-resources-types.md).<br/>                                                                                                                                                                   |
| [Funciones atómicas](direct3d-11-advanced-stages-cs-atomic-functions.md)<br/> | Para acceder a un nuevo tipo de recurso o memoria compartida, use una función intrínseca entrelazado. Se garantiza que las funciones entrelazados funcionen de forma atómica. Es decir, se garantiza que se produzcan en el orden programado. En esta sección se enumeran las funciones atómicas.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Cómo: Crear un sombreador de proceso](direct3d-11-advanced-stages-compute-create.md)
</dt> </dl>

 

