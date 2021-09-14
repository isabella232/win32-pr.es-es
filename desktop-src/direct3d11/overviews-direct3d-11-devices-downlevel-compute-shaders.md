---
title: Sombreadores de proceso en hardware de nivel inferior
description: En este tema se describe cómo usar sombreadores de proceso en una aplicación de Direct3D 11 en hardware de Direct3D 10.
ms.assetid: b864269f-c1f7-4253-888d-04d1ed3e6587
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e77214e917d4d74b0e1eebcc3de245d136157976
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160462"
---
# <a name="compute-shaders-on-downlevel-hardware"></a>Sombreadores de proceso en hardware de nivel inferior

Direct3D 11 proporciona la [](direct3d-11-advanced-stages-compute-shader.md) capacidad de usar sombreadores de proceso que funcionan en la mayoría del hardware de Direct3D 10.x, con algunas limitaciones de funcionamiento. La tecnología de sombreador de proceso también se conoce como tecnología DirectCompute. En este tema se describe [](direct3d-11-advanced-stages-compute-shader.md) cómo usar sombreadores de proceso en una aplicación de Direct3D 11 en hardware de Direct3D 10.

La compatibilidad con sombreadores de proceso en hardware de nivel inferior solo es para dispositivos compatibles con Direct3D 10.x. Los sombreadores de proceso no se pueden usar en hardware direct3D 9.x.

Para comprobar si el hardware de Direct3D 10.x admite sombreadores de proceso, llame a [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). En la llamada **CheckFeatureSupport,** pase el valor D3D11 FEATURE D3D10 X HARDWARE OPTIONS al parámetro Feature, pase un puntero a la estructura \_ FEATURE DATA \_ \_ \_ \_ [**\_ \_ \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options) al parámetro *pFeatureSupportData*  y pase el tamaño de la estructura **D3D11 FEATURE DATA \_ \_ \_ D3D10 X HARDWARE \_ \_ \_ OPTIONS** al parámetro *FeatureSupportDataSize.* **CheckFeatureSupport** devuelve **TRUE** en **ComputeShaders \_ Plus \_ RawAndStructuredBuffers \_ Via Shader \_ \_ 4 \_ x** member of **D3D11 \_ FEATURE DATA \_ \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS** si el hardware de Direct3D 10.x admite sombreadores de proceso.

En la sección 10Level9 Reference (Referencia de [10Level9)](d3d11-graphics-reference-10level9.md) se enumeran las diferencias entre el comportamiento de los distintos métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) en los distintos niveles de características 10Level9.

-   [Vistas de acceso no ordenado (UAV)](#unordered-access-views-uavs)
-   [Vistas de recursos de sombreador (SRV)](#shader-resource-views-srvs)
-   [Grupos de subprocesos](#thread-groups)
    -   [Dimensiones de grupo de subprocesos](#thread-group-dimensions)
    -   [Índices de subprocesos bidimensionales](#two-dimensional-thread-indices)
    -   [Memoria compartida del grupo de subprocesos (TGSM)](#thread-group-shared-memory-tgsm)
-   [D3DCompile con D3DCOMPILE \_ SKIP \_ OPTIMIZATION](/windows)
-   [Temas relacionados](#related-topics)

## <a name="unordered-access-views-uavs"></a>Vistas de acceso no ordenado (UAV)

Las vistas de acceso sin ordenar raw ([RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)) y Structured ([RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)) se admiten en hardware de nivel inferior, con las siguientes limitaciones:

-   Solo se puede enlazar un único UAV a una canalización a la vez a través de [**ID3D11DeviceContext::CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews).
-   El desplazamiento base de un UAV sin procesar debe alinearse en un límite de 256 bytes (en lugar de la alineación de 16 bytes necesaria para el hardware de Direct3D 11).

Los UAV con tipo no se admiten en hardware de nivel inferior. Esto incluye [los UAV Texture1D,](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d) [Texture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)y [Texture3D.](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

Los sombreadores de píxeles del hardware de nivel inferior no admiten el acceso desordenado.

## <a name="shader-resource-views-srvs"></a>Vistas de recursos de sombreador (SRV)

Los búferes sin procesar y estructurados como vistas de recursos de sombreador se admiten en hardware de nivel inferior para el acceso de solo lectura, ya que se encuentran en hardware de Direct3D 11. Estos tipos de recursos se admiten para sombreadores de vértices, sombreadores de geometría, sombreadores de píxeles, así como sombreadores de proceso.

## <a name="thread-groups"></a>Grupos de subprocesos

Un sombreador de proceso puede ejecutarse en muchos subprocesos en paralelo, dentro de un grupo de subprocesos.

Los grupos de subprocesos se admiten en hardware de nivel inferior, con las siguientes limitaciones:

### <a name="thread-group-dimensions"></a>Dimensiones de grupo de subprocesos

Los grupos de subprocesos definidos para el hardware de nivel inferior se limitan a las dimensiones X e Y de 768. Es menor que los valores máximos de 1024 para el hardware de Direct3D 11. La dimensión Z máxima de 64 no se modifica.

El número total de subprocesos del grupo (X × Y × Z) se limita a 768. Esto es menor que el límite de 1024 para el hardware de Direct3D 11.

Si se superan estos números, se producirá un error en la compilación del sombreador.

### <a name="two-dimensional-thread-indices"></a>Two-Dimensional índices de subprocesos

Un subproceso determinado dentro de un grupo de subprocesos se indexa mediante un vector 3D dado por (x,y,z).

En el caso de los sombreadores de proceso que funcionan en hardware de nivel inferior, los grupos de subprocesos solo admiten dos dimensiones. Esto significa que el valor Z del vector 3D siempre debe ser 1.

Esta limitación se aplica específicamente a lo siguiente:

-   [**ID3D11DeviceContext::D ispatch:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch)el argumento *ThreadGroupCountZ* debe ser 1.
-   [**ID3D11DeviceContext::D ispatchIndirect:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect)esta función no se admite en hardware de nivel inferior.
-   [numthreads:](/windows/desktop/direct3dhlsl/sm5-attributes-numthreads)el valor Z debe ser 1.

### <a name="thread-group-shared-memory-tgsm"></a>Memoria compartida del grupo de subprocesos (TGSM)

La memoria compartida del grupo de subprocesos está limitada a 16 Kb en hardware de nivel inferior. Es menor que los 32 Kb que está disponible para el hardware de Direct3D 11.

Un subproceso de sombreador de proceso solo puede escribir en su propia región de TGSM. Esta región de solo escritura tiene un tamaño máximo de 256 bytes o menos, con la disminución máxima a medida que aumenta el número de subprocesos declarados para el grupo.

En la tabla siguiente se define el tamaño máximo por subproceso de una región de TGSM para el número de subprocesos del grupo:



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



 

Un subproceso de sombreador de proceso puede leer el TGSM desde cualquier ubicación.

## <a name="d3dcompile-with-d3dcompile_skip_optimization"></a>D3DCompile con D3DCOMPILE \_ SKIP \_ OPTIMIZATION

[**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) devuelve **E \_ NOTIMPL** cuando se pasa cs 4 0 como destino del sombreador junto con la opción de compilación \_ \_ [**D3DCOMPILE \_ SKIP \_ OPTIMIZATION.**](/windows/desktop/direct3dhlsl/d3dcompile-constants) El destino de sombreador cs \_ \_ 5 0 funciona con **D3DCOMPILE \_ SKIP \_ OPTIMIZATION**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Direct3D 11 en hardware de nivel inferior](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 