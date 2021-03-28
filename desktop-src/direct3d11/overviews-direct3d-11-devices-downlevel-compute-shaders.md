---
title: Sombreadores de cálculo en hardware de nivel inferior
description: En este tema se describe cómo usar los sombreadores de cálculo en una aplicación de Direct3D 11 en hardware de Direct3D 10.
ms.assetid: b864269f-c1f7-4253-888d-04d1ed3e6587
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e77214e917d4d74b0e1eebcc3de245d136157976
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078578"
---
# <a name="compute-shaders-on-downlevel-hardware"></a>Sombreadores de cálculo en hardware de nivel inferior

Direct3D 11 proporciona la capacidad de usar [sombreadores de cálculo](direct3d-11-advanced-stages-compute-shader.md) que funcionan en la mayoría del hardware de Direct3D 10. x, con algunas limitaciones en el funcionamiento. La tecnología del sombreador de cálculo también se conoce como tecnología DirectCompute. En este tema se describe cómo usar los [sombreadores de cálculo](direct3d-11-advanced-stages-compute-shader.md) en una aplicación de Direct3D 11 en hardware de Direct3D 10.

La compatibilidad con los sombreadores de cálculo en el hardware de nivel inferior solo es para los dispositivos compatibles con Direct3D 10. x. Los sombreadores de cálculo no se pueden usar en hardware de Direct3D 9. x.

Para comprobar si el hardware de Direct3D 10. x es compatible con los sombreadores de cálculo, llame a [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). En la llamada a **CheckFeatureSupport** , pase el \_ valor de las opciones de hardware de la característica de D3D11 \_ D3D10 \_ x \_ \_ al parámetro de *característica* , pase un puntero a la estructura de   opciones de hardware de D3D11 de datos de la característica [**\_ \_ \_ D3D10 \_ \_ \_ x**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options) al parámetro pFeatureSupportData, y pase el tamaño de la estructura de **\_ \_ \_ \_ \_ \_ Opciones de hardware D3D11 x de datos de características** D3D10 al parámetro FeatureSupportDataSize. **CheckFeatureSupport** devuelve **true** en el **ComputeShaders \_ más \_ RawAndStructuredBuffers \_ a través del miembro de \_ sombreador \_ 4 \_ x** de **D3D11 de datos de \_ características \_ \_ D3D10 \_ x \_ \_ Opciones de hardware** si el hardware de Direct3D 10. x admite sombreadores de cálculo.

En la sección de [referencia de 10Level9 se](d3d11-graphics-reference-10level9.md) enumeran las diferencias entre el comportamiento de varios métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) y [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) en distintos niveles de características de 10Level9.

-   [Vistas de acceso desordenado (UAVs)](#unordered-access-views-uavs)
-   [Vistas de recursos del sombreador (SRVs)](#shader-resource-views-srvs)
-   [Grupos de subprocesos](#thread-groups)
    -   [Dimensiones de grupo de subprocesos](#thread-group-dimensions)
    -   [Índices de subproceso bidimensionales](#two-dimensional-thread-indices)
    -   [Memoria compartida del grupo de subprocesos (TGSM)](#thread-group-shared-memory-tgsm)
-   [D3DCompile con D3DCOMPILE \_ omitir \_ optimización](/windows)
-   [Temas relacionados](#related-topics)

## <a name="unordered-access-views-uavs"></a>Vistas de acceso desordenado (UAVs)

Las vistas de acceso desordenado ([RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)) y estructurado ([RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)) no se admiten en el hardware de nivel inferior, con las siguientes limitaciones:

-   Solo se puede enlazar un UAV único a una canalización a la vez a través de [**ID3D11DeviceContext:: CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews).
-   El desplazamiento base de un UAV sin formato debe estar alineado en un límite de 256 bytes (en lugar de la alineación de 16 bytes necesaria para el hardware de Direct3D 11).

Los UAVs con tipo no se admiten en el hardware de nivel inferior. Esto incluye [Texture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [Texture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)y [Texture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d) UAVs.

Los sombreadores de píxeles en el hardware de nivel inferior no admiten el acceso no ordenado.

## <a name="shader-resource-views-srvs"></a>Vistas de recursos del sombreador (SRVs)

Los búferes sin formato y estructurado como vistas de recursos del sombreador se admiten en el hardware de nivel inferior para el acceso de solo lectura, como en el hardware de Direct3D 11. Estos tipos de recursos son compatibles con los sombreadores de vértices, sombreadores de geometría, sombreadores de píxeles y sombreadores de cálculo.

## <a name="thread-groups"></a>Grupos de subprocesos

Un sombreador de cálculo puede ejecutarse en muchos subprocesos en paralelo, dentro de un grupo de subprocesos.

Los grupos de subprocesos se admiten en el hardware de nivel inferior, con las siguientes limitaciones:

### <a name="thread-group-dimensions"></a>Dimensiones de grupo de subprocesos

Los grupos de subprocesos definidos para el hardware de nivel inferior se limitan a las dimensiones X e y de 768. Es menor que los valores máximos de 1024 para el hardware de Direct3D 11. La dimensión Z máxima de 64 no cambia.

El número total de subprocesos del grupo (X × Y × Z) está limitado a 768. Es menor que el límite de 1024 para el hardware de Direct3D 11.

Si se superan estos números, se producirá un error en la compilación del sombreador.

### <a name="two-dimensional-thread-indices"></a>Two-Dimensional índices de subprocesos

Un subproceso determinado dentro de un grupo de subprocesos se indiza mediante un vector 3D proporcionado por (x, y, z).

En el caso de los sombreadores de cálculo que operan en hardware de nivel inferior, los grupos de subprocesos solo admiten dos dimensiones. Esto significa que el valor Z del vector 3D siempre debe ser 1.

Esta limitación se aplica específicamente a lo siguiente:

-   [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch): el argumento *ThreadGroupCountZ* debe ser 1.
-   [**ID3D11DeviceContext::D ispatchindirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect): esta función no se admite en el hardware de nivel inferior.
-   [numthreads](/windows/desktop/direct3dhlsl/sm5-attributes-numthreads): el valor Z debe ser 1.

### <a name="thread-group-shared-memory-tgsm"></a>Memoria compartida del grupo de subprocesos (TGSM)

La memoria compartida del grupo de subprocesos está limitada a 16Kb en el hardware de nivel inferior. Es menor que los 32 KB disponibles para el hardware de Direct3D 11.

Un subproceso del sombreador de cálculo solo puede escribir en su propia región de TGSM. Esta región de solo escritura tiene un tamaño máximo de 256 bytes o menos, con el máximo en disminución a medida que aumenta el número de subprocesos declarados para el grupo.

En la tabla siguiente se define el tamaño máximo por subproceso de una región TGSM para el número de subprocesos del Grupo:



| Número de subprocesos del grupo | Tamaño máximo de TGSM por subproceso |
|----------------------------|------------------------------|
| 0-64                       | 256                          |
| 65-68                      | 240                          |
| 69-72                      | 224                          |
| 73-76                      | 208                          |
| 77-84                      | 192                          |
| 85-92                      | 176                          |
| 93-100                     | 160                          |
| 101-112                    | 144                          |
| 113-128                    | 128                          |
| 129-144                    | 112                          |
| 145-168                    | 96                           |
| 169-204                    | 80                           |
| 205-256                    | 64                           |
| 257-340                    | 48                           |
| 341-512                    | 32                           |
| 513-768                    | 16                           |



 

Un subproceso del sombreador de cálculo puede leer TGSM desde cualquier ubicación.

## <a name="d3dcompile-with-d3dcompile_skip_optimization"></a>D3DCompile con D3DCOMPILE \_ omitir \_ optimización

[**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) devuelve **E \_ NOTIMPL** cuando se pasa CS \_ 4 \_ 0 como el destino del sombreador junto con la opción de compilación [**\_ omitir \_ optimización de D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile-constants) . El \_ destino del sombreador de CS 5 \_ 0 funciona con la **optimización de D3DCOMPILE \_ SKIP \_**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Direct3D 11 en hardware de nivel inferior](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 