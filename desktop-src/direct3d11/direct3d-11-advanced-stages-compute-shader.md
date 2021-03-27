---
title: Información general del sombreador de cálculo
description: Un sombreador de cálculo es una fase de sombreador programable que amplía Microsoft Direct3D 11 más allá de la programación de gráficos. La tecnología del sombreador de cálculo también se conoce como tecnología DirectCompute.
ms.assetid: 02c1f98e-fdd6-49b0-b8b2-efbd472ab599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c890e63b468a993e0d08f678d2276d6ce2adad
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "103797217"
---
# <a name="compute-shader-overview"></a>Información general del sombreador de cálculo

Un sombreador de cálculo es una fase de sombreador programable que amplía Microsoft Direct3D 11 más allá de la programación de gráficos. La tecnología del sombreador de cálculo también se conoce como tecnología DirectCompute.

Al igual que otros sombreadores programables (por ejemplo, los sombreadores de vértices y de geometría), un sombreador de cálculo se ha diseñado e implementado con [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) , pero es precisamente donde finaliza la similitud. Un sombreador de cálculo proporciona una informática de uso general de alta velocidad y aprovecha el gran número de procesadores en paralelo de la unidad de procesamiento de gráficos (GPU). El sombreador de cálculo proporciona características de uso compartido de memoria y sincronización de subprocesos para permitir métodos de programación paralelas más eficaces. Llame al método [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch) o [**ID3D11DeviceContext::D ispatchindirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect) para ejecutar comandos en un sombreador de cálculo. Un sombreador de cálculo puede ejecutarse en muchos subprocesos en paralelo.

## <a name="using-compute-shader-on-direct3d-10x-hardware"></a>Usar el sombreador de cálculo en hardware de Direct3D 10. x

Un sombreador de cálculo en Microsoft Direct3D 10 también se conoce como DirectCompute 4. x.

Si usa la API de Direct3D 11 y controladores actualizados, el hardware de Direct3D de [nivel de característica](overviews-direct3d-11-devices-downlevel-intro.md) 10 y 10,1 puede admitir opcionalmente una forma limitada de DirectCompute que usa los \_ perfiles CS 4 \_ 0 y CS \_ 4 \_ 1. [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models) Al usar DirectCompute en este hardware, tenga en cuenta las siguientes limitaciones:

-   El número máximo de subprocesos está limitado a los subprocesos máximos de grupo de subprocesos de D3D11 \_ CS \_ 4 \_ X \_ \_ \_ \_ \_ por \_ grupo (768) por grupo.
-   La dimensión X e y de **numthreads** está limitada a D3D11 \_ CS \_ 4 \_ x \_ grupo de subprocesos \_ \_ \_ x (768) y D3D11 \_ CS \_ 4 \_ x \_ número máximo de subprocesos \_ \_ \_ y (768).
-   La dimensión Z de **numthreads** está limitada a 1.
-   La dimensión Z de Dispatch se limita a D3D11 \_ CS \_ 4 \_ X \_ Dispatch \_ Max \_ Thread \_ Groups \_ en \_ Z \_ Dimension (1).
-   Solo se puede enlazar una vista de acceso sin ordenar al sombreador (el número de registros de D3D11 \_ CS \_ 4 \_ X \_ UAV \_ \_ es 1).
-   Solo [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s y [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s están disponibles como vistas de acceso desordenado.
-   Un subproceso solo puede tener acceso a su propia región en la memoria de groupshared para escritura, aunque puede leer desde cualquier ubicación.
-   [SV \_](/previous-versions/windows/desktop/legacy/ff471569(v=vs.85)) Se debe usar GroupIndex o [SV \_ DispatchThreadID](/windows/desktop/direct3dhlsl/sv-dispatchthreadid) al tener acceso a la memoria **groupshared** para escritura.
-   La memoria de **Groupshared** está limitada a 16 KB por grupo.
-   Un solo subproceso se limita a una región de 256 bytes de memoria **groupshared** para escritura.
-   No hay instrucciones atómicas disponibles.
-   No hay valores de precisión doble disponibles.

## <a name="using-compute-shader-on-direct3d-11x-hardware"></a>Usar el sombreador de cálculo en hardware de Direct3D 11. x

Un sombreador de cálculo en Direct3D 11 también se conoce como DirectCompute 5,0.

Cuando use DirectCompute con perfiles CS \_ 5 \_ 0 [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models), tenga en cuenta los siguientes elementos:

-   El número máximo de subprocesos se limita al grupo de subprocesos máximo de D3D11 \_ CS \_ \_ \_ \_ \_ por \_ grupo (1024) por grupo.
-   La dimensión X e y de **numthreads** se limita al \_ grupo de \_ subprocesos de D3D11 cs \_ \_ Max \_ X (1024) y al \_ grupo de subprocesos de D3D11 CS \_ \_ \_ Max \_ y (1024).
-   La dimensión Z de **numthreads** se limita al \_ grupo de \_ subprocesos de D3D11 CS \_ \_ Max \_ Z (64).
-   La dimensión máxima de Dispatch está limitada a D3D11 \_ CS \_ Dispatch \_ Max \_ Thread \_ groups \_ per \_ Dimension (65535).
-   El número máximo de vistas de acceso desordenado que se pueden enlazar a un sombreador es D3D11 \_ PS \_ CS \_ UAV \_ Register \_ Count (8).
-   Admite [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s, [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s y vistas de acceso desordenado con tipo ([RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d), etc.).
-   Hay instrucciones atómicas disponibles.
-   La compatibilidad de doble precisión podría estar disponible. Para obtener información sobre cómo determinar si la precisión doble está disponible, vea [**la \_ característica D3D11 \_ dobles**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                              | Descripción                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nuevos tipos de recursos](direct3d-11-advanced-stages-cs-resources.md)<br/>      | Se han agregado varios tipos de recursos nuevos en Direct3D 11.<br/>                                                                                                                                                                                                 |
| [Acceso a recursos](direct3d-11-advanced-stages-cs-access.md)<br/>        | Hay varias maneras de tener acceso a [los recursos](overviews-direct3d-11-resources-types.md).<br/>                                                                                                                                                                   |
| [Funciones atómicas](direct3d-11-advanced-stages-cs-atomic-functions.md)<br/> | Para tener acceso a un nuevo tipo de recurso o a la memoria compartida, use una función intrínseca entrelazada. Se garantiza que las funciones entrelazadas funcionen de forma atómica. Es decir, se garantiza que se produzcan en el orden programado. En esta sección se enumeran las funciones atómicas.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Cómo: crear un sombreador de cálculo](direct3d-11-advanced-stages-compute-create.md)
</dt> </dl>

 

