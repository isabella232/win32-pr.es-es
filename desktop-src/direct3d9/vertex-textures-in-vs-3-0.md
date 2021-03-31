---
description: El modelo de sombreador de vértices 3,0 admite la búsqueda de texturas en el sombreador de vértices mediante la instrucción texldl-vs Texture Load.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Texturas de vértices en vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e8e7bbf7e1ae9764fe5b30647f318dfaeb3ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806518"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a>Texturas de vértices en vs \_ 3 \_ 0 (DirectX HLSL)

El modelo de sombreador de vértices 3,0 admite la búsqueda de texturas en el sombreador de vértices mediante la instrucción [texldl-vs](../direct3dhlsl/texldl---vs.md) Texture Load. El motor de vértices contiene cuatro fases de muestra de textura, denominadas [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 y D3DVERTEXTEXTURESAMPLER3. Se diferencian de las muestras de textura y muestra del mapa de desplazamiento en el motor de píxeles.

Para muestras de texturas establecidas en esas cuatro fases, puede usar el motor de vértices y programar las fases con el método [**CheckDeviceFormat**](/windows/desktop/api) . Establezca texturas en esas fases mediante [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), con el índice de fase [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) a través de D3DVERTEXTEXTURESAMPLER3. Se ha introducido un nuevo registro en el sombreador de vértices, el registro de muestra (como en PS \_ 2 \_ 0), que representa la muestra de textura de vértices. Este registro debe definirse en el sombreador antes de usarlo.

Una aplicación puede consultar si se admite un formato como textura de vértice llamando a [**CheckDeviceFormat**](/windows/desktop/api) con [ \_ \_ VERTEXTEXTURE de consulta D3DUSAGE](d3dusage-query.md).

> [!Note]  
> Se trata de una marca de consulta para que no se acepte en ninguna función de Createxxx. Una textura de vértice creada en el grupo predeterminado se puede establecer como una textura de píxeles y viceversa. Sin embargo, para usar el procesamiento de vértices de software, se debe crear la textura de vértices en el grupo de medios (independientemente de si se trata de un dispositivo de modo mixto o de un dispositivo de procesamiento de vértices de software).

 

La funcionalidad es idéntica a las texturas de píxeles, excepto para lo siguiente:

-   No se admite el filtrado de texturas anisotrópico, por lo que D3DSAMP \_ MAXANISOTROPY se pasa por alto y \_ no se puede establecer D3DTEXF anisotrópico para ampliar o minimizar en estas fases.
-   La velocidad de la información de los cambios no está disponible; por lo tanto, la aplicación tiene que calcular el nivel de detalle y proporcionar esa información como un parámetro a [texldl-vs](../direct3dhlsl/texldl---vs.md).

Entre las restricciones se incluyen:

-   Como en los sombreadores de píxeles, si se admiten las texturas de múltiples elementos, \_ se usa D3DSAMP ELEMENTINDEX para averiguar de qué elemento se va a muestrear.
-   El estado D3DSAMP \_ DMAPOFFSET se omite en estas fases.
-   Use [**CheckDeviceFormat**](/windows/desktop/api) con [D3DUSAGE \_ query \_ VERTEXTEXTURE "](d3dusage-query.md) para consultar una textura y ver si se puede usar como textura de vértice.
-   VertexTextureFilterCaps indica qué tipo de filtros se permiten en los muestreadores de textura de vértices. [D3DPTFILTERCAPS \_ MINFANISOTROPIC](d3dptfiltercaps.md) y D3DPTFILTERCAPS \_ MAGFANISOTROPIC no se permiten.

## <a name="sampling-stage-registers"></a>Registros de fase de muestreo

Un registro de fase de muestreo identifica una unidad de muestreo que se puede utilizar en las instrucciones de carga de textura. Una unidad de muestreo corresponde a la fase de muestreo de textura, encapsulando el estado específico del muestreo proporcionado en [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).

Cada muestra identifica de forma única una superficie de textura única que se establece en la muestra correspondiente mediante [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Sin embargo, la misma superficie de textura se puede establecer en varios muestreadores.

En el momento de dibujar, no se puede establecer una textura simultáneamente como un destino de representación y una textura en una fase.

Dado \_ que vs 3 \_ 0 admite cuatro muestreadores, se pueden leer hasta cuatro superficies de textura desde en una sola fase del sombreador. Un registro de muestra solo puede aparecer como un argumento en la instrucción de carga de textura: [texldl-vs](../direct3dhlsl/texldl---vs.md).

En vs \_ 3 \_ 0, si utiliza una muestra, debe declararse al principio del programa del sombreador mediante la [DCL \_ samplerType (SM3-vs ASM)](../direct3dhlsl/dcl-samplertype---vs.md) (como en PS \_ 2 \_ 0).

## <a name="software-processing"></a>Procesamiento de software

Esta característica se admitirá en el procesamiento de vértices de software. Los tipos de filtro específicos admitidos se pueden comprobar llamando a [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) y comprobando VertexTextureFilterCaps. Todos los formatos de textura publicados se admitirán como texturas de vértice en el procesamiento de vértices de software.

Las aplicaciones pueden comprobar si se admite un formato de textura determinado en el modo de procesamiento de vértices de software llamando a [**CheckDeviceFormat**](/windows/desktop/api) y proporcionando (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md)) como uso. Todos los formatos se admiten para el procesamiento de vértices de software. El grupo temporal es necesario para el procesamiento de vértices de software.

## <a name="api-changes"></a>Cambios de la API


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

 

 
