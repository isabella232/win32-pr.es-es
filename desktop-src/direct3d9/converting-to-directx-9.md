---
description: Las siguientes características se cambiaron en Microsoft Direct3D 9. Si usa estas características, consulte los cambios que se enumeran a continuación para ayudarle a portabilidad de la aplicación a Direct3D 9.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Conversión a Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdf5ec812ede4e9d5d356d36b01bbcfcc7732fdb5946e2a13af90c9d9428fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850535"
---
# <a name="converting-to-direct3d-9"></a>Conversión a Direct3D 9

Las siguientes características se cambiaron en Microsoft Direct3D 9. Si usa estas características, consulte los cambios que se enumeran a continuación para ayudarle a portabilidad de la aplicación a Direct3D 9.

-   [Cambios de BaseVertexIndex](#basevertexindex-changes)
-   [Cambios de CreateImageSurface](#createimagesurface-changes)
-   [D3DENUM \_ NO \_ WHQL \_ LEVEL Changes](/windows)
-   [Crear cambios de recursos](#create-resource-changes)
-   [Cambios en enumAdapterModes](#enumadaptermodes-changes)
-   [Cambios de Get/SetStreamSource \_](#getsetstreamsource-changes)
-   [Cambios de calidad de variosmuestreos](#multisampling-quality-changes)
-   [Cambios de ResourceManagerDiscardBytes](#resourcemanagerdiscardbytes-changes)
-   [Cambios de SetSoftwareVertexProcessing](#setsoftwarevertexprocessing-changes)
-   [Cambios del muestreador de textura](#texture-sampler-changes)
-   [Cambios en la declaración de vértices](#vertex-declaration-changes)
-   [Intervalos \_ y cambios de \_ SwapEffects \_](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a>Cambios de BaseVertexIndex

En DirectX 8.x, IDirect3DDevice8::SetIndices requería un puntero al búfer de índice y baseVertexIndex para la posición inicial en el búfer de vértices. Una aplicación que agrupaba por lotes distintos objetos en el búfer de vértices tenía que cambiar el búfer de índice (o realizar una llamada a IDirect3DDevice8::SetIndices) antes de llamar a IDirect3DDevice8::D rawIndexedPrimitive.

En Direct3D 9, la posición inicial del búfer de vértices, *BaseVertexIndex*, se ha movido a IDirect3DDevice9::D rawIndexedPrimitive y su tipo de datos ha cambiado de DWORD a INT.


```
HRESULT IDirect3DDevice9::DrawIndexedPrimitive( 
    D3DPRIMITIVETYPE PrimType, 
    INT BaseVertexIndex, 
    UINT minIndex, 
    UINT NumVertices, 
    UINT startIndex, 
    UINT primCount); 

HRESULT SetIndices(IDirect3DIndexBuffer9* pIndexData); 
```



## <a name="createimagesurface-changes"></a>Cambios de CreateImageSurface

Se ha cambiado el nombre de IDirect3DDevice8::CreateImageSurface [**a CreateOffscreenPlainSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface) Se ha agregado un parámetro adicional que toma un tipo D3DPOOL. D3DPOOL SCRATCH devolverá una superficie que tiene características idénticas a una superficie creada por \_ IDirect3DDevice8::CreateImageSurface. D3DPOOL \_ DEFAULT es el grupo adecuado para su uso con [**StretchRect**](/windows/desktop/api) y [**ColorFill.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill)

## <a name="d3denum_no_whql_level-changes"></a>D3DENUM \_ NO \_ WHQL \_ LEVEL Changes

Las aplicaciones ahora tienen que solicitar explícitamente Microsoft Windows Hardware Quality Labs (WHQL) porque la respuesta tarda relativamente largo (unos segundos). D3DENUM NO WHQL LEVEL se ha quitado \_ y se ha agregado \_ \_ D3DENUM \_ WHQL \_ LEVEL.

## <a name="create-resource-changes"></a>Crear cambios de recursos

Se ha agregado un identificador a varios métodos y debe establecerse en **NULL.** Los métodos afectados incluyen:

-   [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [**CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a>Cambios en enumAdapterModes

[**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) ahora toma un D3DFORMAT.


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



El formato admite un conjunto expandido de modos de presentación. Para proteger las aplicaciones de la enumeración de formatos que no se inventaron cuando se envió la aplicación, la aplicación debe especificar a Direct3D el formato de los modos de presentación que se deben enumerar. La matriz resultante de modos de presentación solo variará según el ancho, el alto y la frecuencia de actualización.

La aplicación especifica un formato de píxel y la enumeración está restringida a los modos de presentación que coinciden exactamente con el formato. A continuación se muestra una lista de los formatos permitidos:

-   D3DFMT \_ A1R5G5B5
-   D3DFMT \_ A2B10G10R10
-   D3DFMT \_ A8R8G8B8
-   D3DFMT \_ R5G6B5
-   D3DFMT \_ X1R5G5B5
-   D3DFMT \_ X8R8G8B8

La enumeración es equivalente a las versiones alfa y nonalpha del mismo formato. El formato devuelto siempre se rellenará con el mismo formato proporcionado por la aplicación.

Este método trata 565 y 555 como equivalente y devuelve la versión correcta en el formato . La diferencia solo entra en juego cuando la aplicación bloquea el búfer de reserva y hay una marca explícita que la aplicación debe establecer para lograr esto.

## <a name="getsetstreamsource-changes"></a>Cambios de Get/SetStreamSource

Se ha agregado un parámetro a los [**métodos GetStreamSource**](/windows/desktop/api) [**y SetStreamSource.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) El desplazamiento es el número de bytes entre el principio de la secuencia y el principio de los datos del vértice. Se mide en bytes. Esto permite que la canalización admita desplazamientos de flujo. Para averiguar si el dispositivo admite desplazamientos de flujo, consulte D3DDEVCAPS2 \_ STREAMOFFSET.


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a>Cambios de calidad de variosmuestreos

Anteriormente, solo había la enumeración D3DMULTISAMPLE \_ TYPE. Direct3D 9 conserva esta enumeración y agrega la idea de un nivel de calidad para cada elemento de la enumeración. El nivel de calidad indica un equilibrio entre la calidad visual y el rendimiento indicando el número de muestras enmascarables (en el sentido de D3DRS \_ MULTISAMPLEMASK).

Una aplicación debe elegir cuántos ejemplos enmascarables necesita y, a continuación, consultar pQualityLevels. Si es distinto de cero, este valor indica el número de niveles de calidad que la aplicación puede pasar a las distintas funciones de creación a través de MultiSampleQuality. Dado que los controladores exponen todos sus esquemas de varios ejemplos como niveles de calidad en D3DMULTISAMPLE NONMASKABLE, puede enumerar todos los esquemas de multimuestreo disponibles a través de este tipo si la aplicación no necesita enmascarar \_ ejemplos.

Se ha retirado el bit de límites D3DPRASTERCAPS \_ STRETCHBLTMULTISAMPLE. Este bit solía significar que el método multimuestreo no admite máscaras de escritura y no se podía activar y desactivar entre [**BeginScene**](/windows/desktop/api) y [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene). Estos métodos no máscara ahora se exponen a través de D3DMULTISAMPLE \_ NONMASKABLE.


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



Hay un máximo diferente para cada número de muestras enmascarables. Por ejemplo, D3DMULTISAMPLE 4 SAMPLES podría tener tres niveles de calidad, mientras que \_ \_ D3DMULTISAMPLE 2 SAMPLES podría \_ tener solo \_ uno. Hay como máximo ocho niveles de calidad para cada número de muestras enmascarables (el controlador no puede expresar más). La calidad va de cero a ( \* pQualityLevels - 1).

## <a name="resourcemanagerdiscardbytes-changes"></a>Cambios de ResourceManagerDiscardBytes

ResourceManagerDiscardBytes se ha reemplazado por IDirect3DDevice9::EvictManagedResources. Puede expulsar todos los recursos, tanto de Direct3D como de controladores.

Ahora se consulta al administrador de recursos cuando se produce un error en la creación de un recurso (ya sea administrado o no administrado) porque no hay memoria de vídeo suficiente. Se le pedirá automáticamente al administrador que liberara suficientes recursos para que la creación se realizara correctamente. En DirectX 8.0, este no era un proceso automatizado.

## <a name="setsoftwarevertexprocessing-changes"></a>Cambios de SetSoftwareVertexProcessing

Una aplicación puede crear un dispositivo en modo mixto para usar el procesamiento de vértices de hardware y software.

Para cambiar entre los dos modos de procesamiento de vértices en DirectX 8.x, llame a IDirect3DDevice8::SetRenderState. Esto se ha reemplazado por [**SetSoftwareVertexProcessing para**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) facilitar los problemas causados por los bloques de estado. Los bloques de estado no registran este nuevo método.

## <a name="texture-sampler-changes"></a>Cambios del muestreador de textura

Direct3D 9 admite hasta dieciséis superficies de textura en un solo paso mediante el modelo de sombreador de píxeles 2 0; sin embargo, el número de coordenadas de textura permanece limitado \_ a ocho. El estado de la fase de textura está asociado a superficies, conjuntos de coordenadas, procesamiento de vértices y procesamiento de píxeles. Para administrar estas diferencias en tiempo de compilación, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) se ha dividido en dos métodos:

-   IDirect3DDevice9::SetTextureStageState se seguirá usando para el estado de coordenadas de textura, como los modos de encapsulado y la generación de coordenadas de textura.
-   [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) se ha agregado y ahora se usará para el filtrado, el tiling, la fijación, MIPLOD, etc. Esto funcionará para hasta 16 muestreadores.

### <a name="settexturestagestate-changes"></a>Cambios de SetTextureStageState

IDirect3DDevice9::SetTextureStageState ahora establece los siguientes estados:

-   Se ha corregido el estado de procesamiento de vértices de función. Este estado controla la manipulación de las coordenadas de textura D3DTSS \_ TEXTURETRANSFORMFLAGS y D3DTSS \_ TEXCOORDINDEX. Se pueden establecer hasta ocho de cada una (porque siempre se admiten ocho coordenadas de textura). D3DTSS \_ TEXCOORDINDEX es un estado fijo de procesamiento de vértices de función. Si se usa un sombreador de vértices programable, se omite este estado.
-   Se ha corregido el estado del sombreador de píxeles de función (el objeto TextureStageState heredado).

    -   D3DTSS \_ ALPHAARG0
    -   D3DTSS \_ ALPHAARG1
    -   D3DTSS \_ ALPHAARG2
    -   D3DTSS \_ ALPHAOP
    -   BUMPENVLOFFSET de D3DTSS \_
    -   D3DTSS \_ BUMPENVLSCALE
    -   D3DTSS \_ BUMPENVMAT00
    -   D3DTSS \_ BUMPENVMAT01
    -   D3DTSS \_ BUMPENVMAT10
    -   D3DTSS \_ BUMPENVMAT11
    -   D3DTSS \_ COLORARG0
    -   D3DTSS \_ COLORARG1
    -   D3DTSS \_ COLORARG2
    -   COLOROP de D3DTSS \_
    -   D3DTSS \_ RESULTARG

    El número de estados fijos del sombreador de píxeles de función que se pueden establecer es menor o igual que el número representado por MaxTextureBlendStages.

El número de muestreadores de textura disponibles para la aplicación viene determinado por la versión del sombreador de píxeles, como se indica en la tabla siguiente.



| Nombre                    | Número                                                         |
|-------------------------|----------------------------------------------------------------|
| ps \_ 1 \_ 1 to ps \_ 1 \_ 3    | 4 muestreadores de textura                                             |
| ps \_ 1 \_ 4                | 6 muestreadores de textura                                             |
| ps \_ 2 \_ 0                | 16 muestreadores de textura                                            |
| canalización de función fija | Muestras de textura MaxTextureBlendStages/MaxSimultaneousTextures |



 

Los dispositivos que admiten la asignación de desplazamiento en Direct3D 9 admitirán un sampler adicional (D3DDMAPSAMPLER), que muestrea los mapas de desplazamiento en la unidad de teselador.

### <a name="setsamplerstate-changes"></a>Cambios de SetSamplerState

IDirect3DDevice9::SetSamplerState establece el estado del muestreador (incluido el que se usa en la unidad de teselador para muestrear mapas de desplazamiento). Se ha cambiado el nombre de estos con un prefijo D3DSAMP para habilitar la detección de errores en tiempo de compilación al portear \_ desde DirectX 8.x. Los estados incluyen:

-   D3DSAMP \_ ADDRESSU
-   D3DSAMP \_ ADDRESSV
-   D3DSAMP \_ ADDRESSW
-   D3DSAMP \_ BORDERCOLOR
-   D3DSAMP \_ MAGFILTER
-   D3DSAMP \_ MAXANISOTROPY
-   D3DSAMP \_ MAXMIPLEVEL
-   D3DSAMP \_ MINFILTER
-   MIPFILTER de D3DSAMP \_
-   D3DSAMP \_ MIPMAPLODBIAS

## <a name="vertex-declaration-changes"></a>Cambios en la declaración de vértices

Las declaraciones de vértices ahora se desacoplan de la creación del sombreador de vértices. Las declaraciones de vértice ahora usan una interfaz de Modelo de objetos componentes (COM).

Para DirectX 8.x, las declaraciones de vértices están vinculadas a sombreadores de vértices.

-   Para la canalización de función fija, llame a [**SetVertexShader con**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) el código de formato de vértice flexible (FVF) del búfer de vértices.
-   En el caso de los sombreadores de vértices, llame a IDirect3DDevice9::SetVertexShader con un identificador para un sombreador de vértices creado anteriormente. El sombreador incluye una declaración de vértice.

Para Direct3D 9, las declaraciones de vértices se desacoplan de los sombreadores de vértices y se pueden usar con la canalización de función fija o con sombreadores.

-   Para la canalización de funciones fijas, no es necesario llamar a IDirect3DDevice9::SetVertexShader. Sin embargo, si desea cambiar a la canalización de función fija y ha usado previamente un sombreador de vértices, llame a IDirect3DDevice9::SetVertexShader(**NULL**). Una vez hecho esto, deberá llamar a [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) para declarar el código FVF.
-   Al usar sombreadores de vértices, llame a IDirect3DDevice9::SetVertexShader con el objeto de sombreador de vértices. Además, llame a IDirect3DDevice9::SetFVF para configurar una declaración de vértice. Esto usa la información implícita en FVF. Se puede llamar a [**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) en lugar de IDirect3DDevice9::SetFVF porque admite declaraciones de vértice que no se pueden expresar con una FVF.

## <a name="intervals-and-swapeffects-changes"></a>Intervalos y cambios de SwapEffects

Se realizaron varios cambios para proporcionar al usuario más control sobre la frecuencia de actualización del monitor, la tasa de presentación y el dibujo del búfer front-buffer frente al de búfer de reserva. Los pasos son los siguientes:

-   Se ha quitado un efecto de intercambio, D3DSWAPEFFECT COPY VSYNC y una tasa de \_ \_ presentación, D3DPRESENT \_ RATE \_ UNLIMITED.
-   Se ha cambiado el nombre de los PARÁMETROS D3DPRESENT. \_ FullScreen \_ PresentationInterval to PresentationIntervals.
-   Se ha agregado D3DPRESENT INTERVAL IMMEDIATE, lo que significa que la presentación \_ \_ no está sincronizada con la sincronización vertical. Al igual que en DirectX 8.x, D3DPRESENT INTERVAL DEFAULT se define como cero y es equivalente a \_ \_ D3DPRESENT \_ INTERVAL \_ ONE. D3DPRESENT \_ INTERVAL DEFAULT es una comodidad para \_ inicializar parámetros D3DPRESENT \_ en cero.

Para obtener una explicación detallada de los modos y los intervalos admitidos, consulte D3DPRESENT.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gráficos de Direct3D 9](dx9-graphics.md)
</dt> </dl>

 

 
