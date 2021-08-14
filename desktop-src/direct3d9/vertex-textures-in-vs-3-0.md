---
description: El modelo del sombreador de vértices 3.0 admite la búsqueda de textura en el sombreador de vértices mediante la instrucción texldl - vs texture load.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Texturas de vértice en vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4cbd4aa1e1830d29656fea2bc7b028191bee158eede119c9a47ae2457d10e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519453"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a>Texturas de vértice en frente \_ a 3 \_ 0 (DirectX HLSL)

El modelo del sombreador de vértices 3.0 admite la búsqueda de textura en el sombreador de vértices mediante la [instrucción texldl - vs](../direct3dhlsl/texldl---vs.md) texture load. El motor de vértices contiene cuatro fases del muestreador de textura, [denominadas D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 y D3DVERTEXTEXTURESAMPLER3. Son distintos del sampler del mapa de desplazamiento y de los muestreadores de textura en el motor de píxeles.

Para muestrear las texturas establecidas en esas cuatro fases, puede usar el motor de vértices y programar las fases con el [**método CheckDeviceFormat.**](/windows/desktop/api) Establezca texturas en esas fases mediante [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), con el índice de fase [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) a D3DVERTEXTEXTURESAMPLER3. Se ha introducido un nuevo registro en el sombreador de vértices, el registro del muestreador (como en ps \_ 2 0), que representa el muestreador de textura \_ de vértice. Este registro debe definirse en el sombreador antes de usarlo.

Una aplicación puede consultar si se admite un formato como textura de vértice llamando a [**CheckDeviceFormat**](/windows/desktop/api) con [D3DUSAGE \_ QUERY \_ VERTEXTEXTURE](d3dusage-query.md).

> [!Note]  
> Se trata de una marca de consulta, por lo que no se acepta en ninguna función Createxxx. Una textura de vértice creada en el grupo predeterminado se puede establecer como una textura de píxel y viceversa. Sin embargo, para usar el procesamiento de vértices de software, la textura de vértice debe crearse en el grupo de vértices (independientemente de si es un dispositivo en modo mixto o un dispositivo de procesamiento de vértices de software).

 

La funcionalidad es idéntica a las texturas de píxel, excepto lo siguiente:

-   No se admite el filtrado de texturas anisotropicas, por lo que D3DSAMP MAXANISOTROPY se omite y \_ D3DTEXF ANISOTROPIC no se puede establecer para la lupa ni para la minificación para estas \_ fases.
-   La tasa de cambio de información no está disponible, por lo que la aplicación tiene que calcular el nivel de detalle y proporcionar esa información como un parámetro para [texldl- frente](../direct3dhlsl/texldl---vs.md)a .

Entre las restricciones se incluyen:

-   Al igual que en los sombreadores de píxeles, si se admiten texturas de varios elementos, se usa D3DSAMP ELEMENTINDEX para averiguar de qué elemento se \_ va a muestrear.
-   El estado D3DSAMP \_ DMAPOFFSET se omite para estas fases.
-   Use [**CheckDeviceFormat**](/windows/desktop/api) con [D3DUSAGE \_ QUERY \_ VERTEXTEXTURE"](d3dusage-query.md) para consultar una textura para ver si se puede usar como textura de vértice.
-   VertexTextureFilterCaps indica qué tipo de filtros se permiten en los muestreadores de textura de vértice. [D3DPTFILTERCAPS \_ MINFANISOTROPIC](d3dptfiltercaps.md) y D3DPTFILTERCAPS \_ MAGFANISOTROPIC no están permitidos.

## <a name="sampling-stage-registers"></a>Registros de fase de muestreo

Un registro de fase de muestreo identifica una unidad de muestreo que se puede usar en instrucciones de carga de textura. Una unidad de muestreo corresponde a la fase de muestreo de textura, encapsulando el estado específico del muestreo proporcionado en [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).

Cada muestreador identifica de forma única una sola superficie de textura que se establece en el muestreador correspondiente mediante [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Sin embargo, la misma superficie de textura se puede establecer en varios muestreadores.

En el momento del dibujo, una textura no se puede establecer simultáneamente como un destino de representación y una textura en una fase.

Dado que \_ vs 3 0 admite cuatro muestreadores, se pueden leer hasta cuatro superficies de textura en \_ un solo paso de sombreador. Un registro de sampler solo puede aparecer como argumento en la instrucción de carga de textura: [texldl - frente a](../direct3dhlsl/texldl---vs.md).

En vs 3 0, si usa un sampler, se debe declarar al principio del programa de \_ \_ sombreador, mediante [dcl \_ samplerType (sm3 - vs asm)](../direct3dhlsl/dcl-samplertype---vs.md) (como en ps \_ 2 \_ 0).

## <a name="software-processing"></a>Procesamiento de software

Esta característica se admite en el procesamiento de vértices de software. Los tipos de filtro específicos admitidos se pueden comprobar llamando [**a GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) y comprobando VertexTextureFilterCaps. Todos los formatos de textura publicados se admiten como texturas de vértice en el procesamiento de vértices de software.

Las aplicaciones pueden comprobar si se admite un formato de textura determinado en el modo de procesamiento de vértices de software llamando a [**CheckDeviceFormat**](/windows/desktop/api) y proporcionando (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md)) como uso. Todos los formatos se admiten para el procesamiento de vértices de software. El grupo de scratch es necesario para el procesamiento de vértices de software.

## <a name="api-changes"></a>Cambios de API


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 
