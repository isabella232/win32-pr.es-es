---
description: Se cambiaron las siguientes características en Microsoft Direct3D 9. Si usa estas características, consulte los cambios que se enumeran a continuación para ayudarle a migrar la aplicación a Direct3D 9.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Convertir a Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becdb878ad462bfc0157fb15b3c9c1ef2ba158dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714861"
---
# <a name="converting-to-direct3d-9"></a>Convertir a Direct3D 9

Se cambiaron las siguientes características en Microsoft Direct3D 9. Si usa estas características, consulte los cambios que se enumeran a continuación para ayudarle a migrar la aplicación a Direct3D 9.

-   [BaseVertexIndex cambios](#basevertexindex-changes)
-   [CreateImageSurface cambios](#createimagesurface-changes)
-   [D3DENUM \_ sin \_ cambios en el nivel de WHQL \_](/windows)
-   [Crear cambios de recursos](#create-resource-changes)
-   [EnumAdapterModes cambios](#enumadaptermodes-changes)
-   [Cambios de Get/SetStreamSource \_](#getsetstreamsource-changes)
-   [Cambios de calidad de muestreo múltiple](#multisampling-quality-changes)
-   [ResourceManagerDiscardBytes cambios](#resourcemanagerdiscardbytes-changes)
-   [SetSoftwareVertexProcessing cambios](#setsoftwarevertexprocessing-changes)
-   [Cambios de la muestra de textura](#texture-sampler-changes)
-   [Cambios en la declaración de vértices](#vertex-declaration-changes)
-   [Intervalos \_ y \_ cambios de SwapEffects \_](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a>BaseVertexIndex cambios

En DirectX 8. x, IDirect3DDevice8:: SetIndices requería un puntero al búfer de índice y un BaseVertexIndex para la posición inicial en el búfer de vértices. Una aplicación que procesa por lotes objetos diferentes en el búfer de vértices tenía que cambiar el búfer de índice (o realizar una llamada a IDirect3DDevice8:: SetIndices) antes de llamar a IDirect3DDevice8::D rawIndexedPrimitive.

En Direct3D 9, la posición inicial en el búfer de vértices, *BaseVertexIndex*, se ha pasado a IDirect3DDevice9::D rawindexedprimitive y su tipo de datos ha cambiado de DWORD a int.


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



## <a name="createimagesurface-changes"></a>CreateImageSurface cambios

IDirect3DDevice8:: CreateImageSurface ha cambiado el nombre de [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface). Se ha agregado un parámetro adicional que toma un tipo D3DPOOL. D3DPOOL \_ Scratch devolverá una superficie que tiene características idénticas a una superficie creada por IDirect3DDevice8:: CreateImageSurface. D3DPOOL \_ default es el grupo adecuado para su uso con [**StretchRect**](/windows/desktop/api) y [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).

## <a name="d3denum_no_whql_level-changes"></a>D3DENUM \_ sin \_ cambios en el nivel de WHQL \_

Ahora, las aplicaciones tienen que solicitar explícitamente los laboratorios de calidad de hardware de Microsoft Windows (WHQL), ya que la respuesta tarda un tiempo relativamente largo (unos segundos). D3DENUM \_ no se ha \_ \_ quitado el nivel de WHQL y se ha agregado el nivel de WHQL de D3DENUM \_ \_ .

## <a name="create-resource-changes"></a>Crear cambios de recursos

Se ha agregado un identificador a varios métodos y debe establecerse en **null**. Los métodos afectados incluyen:

-   [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [**CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a>EnumAdapterModes cambios

[**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) Now toma D3DFORMAT.


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



El formato admite un conjunto expandido de modos de presentación. Para proteger las aplicaciones de los formatos que no se inventaron cuando se envió la aplicación, la aplicación debe indicar a Direct3D el formato de los modos de presentación que se deben enumerar. La matriz de modos de presentación resultante solo variará en función del ancho, el alto y la frecuencia de actualización.

La aplicación especifica un formato de píxel y la enumeración está restringida a los modos de presentación que coinciden exactamente con el formato. A continuación se muestra una lista de los formatos permitidos:

-   D3DFMT \_ A1R5G5B5
-   D3DFMT \_ A2B10G10R10
-   D3DFMT \_ A8R8G8B8
-   D3DFMT \_ R5G6B5
-   D3DFMT \_ X1R5G5B5
-   D3DFMT \_ X8R8G8B8

La enumeración es equivalente para las versiones alfa y no Alpha del mismo formato. El formato devuelto siempre se rellenará con el mismo formato proporcionado por la aplicación.

Este método trata 565 y 555 como equivalente y devuelve la versión correcta en el formato. La diferencia solo se produce cuando la aplicación bloquea el búfer de reserva y hay una marca explícita que la aplicación debe establecer para lograrlo.

## <a name="getsetstreamsource-changes"></a>Cambios de Get/SetStreamSource

Se ha agregado un parámetro a los métodos [**GetStreamSource**](/windows/desktop/api) y [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) . El desplazamiento es el número de bytes entre el principio de la secuencia y el principio de los datos de vértice. Se mide en bytes. Esto permite que la canalización admita desplazamientos de flujo. Para averiguar si el dispositivo admite desplazamientos de flujo, consulte D3DDEVCAPS2 \_ STREAMOFFSET.


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a>Cambios de calidad de muestreo múltiple

Anteriormente, solo había una \_ enumeración de tipo D3DMULTISAMPLE. Direct3D 9 conserva esta enumeración y agrega la idea de un nivel de calidad para cada elemento de la enumeración. El nivel de calidad indica un equilibrio entre la calidad visual y el rendimiento indicando el número de muestras Enmascarables (en el sentido de D3DRS \_ MULTISAMPLEMASK).

Una aplicación debe elegir el número de ejemplos Enmascarables que requiera y, a continuación, consultar pQualityLevels. Si es distinto de cero, este valor indica el número de niveles de calidad que la aplicación puede pasar a las distintas funciones de creación a través de MultiSampleQuality. Dado que los controladores exponen todos los esquemas de ejemplo múltiple como niveles de calidad en D3DMULTISAMPLE \_ no enmascarable, puede enumerar todos los esquemas de muestreo múltiple disponibles a través de este tipo si la aplicación no necesita enmascarar los ejemplos.

Se ha \_ retirado el bit de Cap de STRETCHBLTMULTISAMPLE de D3DPRASTERCAPS. Este bit se usa para indicar que el método de muestreo múltiple no admitía máscaras de escritura y no se podía activar y desactivar entre [**BeginScene**](/windows/desktop/api) y [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene). Estos métodos no Enmascarables ahora se exponen a través de D3DMULTISAMPLE no \_ enmascarable.


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



Existe un máximo diferente para cada número de muestras Enmascarables. Por ejemplo, \_ los ejemplos de D3DMULTISAMPLE 4 \_ podrían tener tres niveles de calidad, mientras que los de D3DMULTISAMPLE \_ 2 \_ pueden tener solo uno. Hay ocho niveles de calidad como máximo para cada número de muestras Enmascarables (el controlador no puede expresar más). La calidad oscila entre cero y ( \* pQualityLevels-1).

## <a name="resourcemanagerdiscardbytes-changes"></a>ResourceManagerDiscardBytes cambios

ResourceManagerDiscardBytes se ha reemplazado por IDirect3DDevice9:: EvictManagedResources. Puede expulsar todos los recursos, tanto Direct3D como los recursos de controlador.

Ahora se consulta al administrador de recursos cuando un recurso (ya sea administrado o no administrado) produce un error en la creación porque no hay suficiente memoria de vídeo. Se pedirá automáticamente al administrador que libere suficientes recursos para que la creación se realice correctamente. En DirectX 8,0, no se trata de un proceso automatizado.

## <a name="setsoftwarevertexprocessing-changes"></a>SetSoftwareVertexProcessing cambios

Una aplicación puede crear un dispositivo en modo mixto para usar el procesamiento de vértices de software y hardware.

Para cambiar entre los dos modos de procesamiento de vértices en DirectX 8. x, llame a IDirect3DDevice8:: SetRenderState. Esto se ha sustituido por [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) para facilitar los problemas causados por los bloques de estado. Este nuevo método no está registrado por los bloques de estado.

## <a name="texture-sampler-changes"></a>Cambios de la muestra de textura

Direct3D 9 admite hasta dieciséis superficies de textura en un solo paso mediante el modelo de sombreador de píxeles 2 \_ 0; sin embargo, el número de coordenadas de textura permanece limitado a ocho. El estado de la fase de textura está asociado a las superficies, los conjuntos de coordenadas, el procesamiento de vértices y el procesamiento de píxeles. Para administrar estas diferencias en tiempo de compilación, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) se ha dividido en dos métodos:

-   IDirect3DDevice9:: SetTextureStageState se seguirá usando para el estado de coordenadas de textura, como los modos de ajuste y la generación de coordenadas de textura.
-   [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) se ha agregado y ahora se usará para filtrar, colocar en mosaicos, adfijar, MIPLOD, etc. Esto funcionará para hasta dieciséis muestreadores.

### <a name="settexturestagestate-changes"></a>SetTextureStageState cambios

IDirect3DDevice9:: SetTextureStageState ahora establece los siguientes Estados:

-   Estado de procesamiento de vértice de función fija. Este estado controla la manipulación de las coordenadas de textura D3DTSS \_ TEXTURETRANSFORMFLAGS y D3DTSS \_ TEXCOORDINDEX. Se pueden establecer hasta ocho de cada uno (dado que se admiten ocho coordenadas de textura siempre). D3DTSS \_ TEXCOORDINDEX es un estado de procesamiento de vértice de función fijo. Si se usa un sombreador de vértices programable, se omite este estado.
-   Estado del sombreador de píxeles de función fija (el TextureStageState heredado).

    -   D3DTSS \_ ALPHAARG0
    -   D3DTSS \_ ALPHAARG1
    -   D3DTSS \_ ALPHAARG2
    -   D3DTSS \_ ALPHAOP
    -   D3DTSS \_ BUMPENVLOFFSET
    -   D3DTSS \_ BUMPENVLSCALE
    -   D3DTSS \_ BUMPENVMAT00
    -   D3DTSS \_ BUMPENVMAT01
    -   D3DTSS \_ BUMPENVMAT10
    -   D3DTSS \_ BUMPENVMAT11
    -   D3DTSS \_ COLORARG0
    -   D3DTSS \_ COLORARG1
    -   D3DTSS \_ COLORARG2
    -   D3DTSS \_ COLOROP
    -   D3DTSS \_ RESULTARG

    El número de Estados de sombreador de píxeles de función fija que se pueden establecer es menor o igual que el número representado por MaxTextureBlendStages.

El número de muestras de textura disponibles para la aplicación viene determinado por la versión del sombreador de píxeles, como se indica en la tabla siguiente.



| Nombre                    | Number                                                         |
|-------------------------|----------------------------------------------------------------|
| PS \_ 1 \_ 1 a PS \_ 1 \_ 3    | 4 muestras de texturas                                             |
| PS \_ 1 \_ 4                | 6 muestras de texturas                                             |
| PS \_ 2 \_ 0                | 16 muestras de texturas                                            |
| canalización de funciones fijas | Muestras de textura de MaxTextureBlendStages/MaxSimultaneousTextures |



 

Los dispositivos que admiten la asignación de desplazamiento en Direct3D 9 serán compatibles con una muestra adicional (D3DDMAPSAMPLER), que muestrea los mapas de desplazamiento en la unidad del teselador.

### <a name="setsamplerstate-changes"></a>SetSamplerState cambios

IDirect3DDevice9:: SetSamplerState establece el estado de la muestra (incluido el usado en la unidad del teselador en los mapas de desplazamiento de ejemplo). Se les ha cambiado el nombre con un \_ prefijo D3DSAMP para habilitar la detección de errores en tiempo de compilación al migrar desde DirectX 8. x. Los Estados incluyen:

-   D3DSAMP \_ ADDRESSU
-   D3DSAMP \_ ADDRESSV
-   D3DSAMP \_ ADDRESSW
-   D3DSAMP \_ BORDERCOLOR
-   D3DSAMP \_ MAGFILTER
-   D3DSAMP \_ MAXANISOTROPY
-   D3DSAMP \_ MAXMIPLEVEL
-   D3DSAMP \_ MINFILTER
-   D3DSAMP \_ MIPFILTER
-   D3DSAMP \_ MIPMAPLODBIAS

## <a name="vertex-declaration-changes"></a>Cambios en la declaración de vértices

Las declaraciones de vértices ahora se desacoplan de la creación del sombreador de vértices. Las declaraciones de vértices ahora usan una interfaz del modelo de objetos componentes (COM).

Para DirectX 8. x, las declaraciones de vértices están asociadas a los sombreadores de vértices.

-   Para la canalización de función fija, llame a [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) con el código de formato de vértice flexible (FVF) del búfer de vértices.
-   Para los sombreadores de vértices, llame a IDirect3DDevice9:: SetVertexShader con un identificador a un sombreador de vértices creado anteriormente. El sombreador incluye una declaración de vértice.

En Direct3D 9, las declaraciones de vértices se desacoplan de los sombreadores de vértices y se pueden usar con la canalización de función fija o con los sombreadores.

-   Para la canalización de función fija, no es necesario llamar a IDirect3DDevice9:: SetVertexShader. Sin embargo, si desea cambiar a la canalización de función fija y ha usado previamente un sombreador de vértices, llame a IDirect3DDevice9:: SetVertexShader (**null**). Una vez hecho esto, deberá llamar a [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) para declarar el código FVF.
-   Al usar sombreadores de vértices, llame a IDirect3DDevice9:: SetVertexShader con el objeto de sombreador de vértices. Además, llame a IDirect3DDevice9:: SetFVF para configurar una declaración de vértice. Usa la información implícita en el FVF. Se puede llamar a [**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) en lugar de IDirect3DDevice9:: SetFVF porque admite declaraciones de vértices que no se pueden expresar con un FVF.

## <a name="intervals-and-swapeffects-changes"></a>Intervalos y cambios de SwapEffects

Se realizaron varios cambios para ofrecer al usuario más control sobre la frecuencia de actualización del monitor, la velocidad de presentación y el dibujo del búfer frontal frente al de búfer. Los pasos son los siguientes:

-   Se ha quitado un efecto de intercambio, D3DSWAPEFFECT \_ Copy \_ VSYNC y una velocidad de presentación, D3DPRESENT \_ rate \_ Unlimited.
-   Se ha cambiado el nombre de \_ los parámetros D3DPRESENT. FullScreen \_ PresentationInterval a PresentationIntervals.
-   Se ha agregado el intervalo de D3DPRESENT \_ \_ inmediato, lo que significa que la presentación no está sincronizada con la sincronización vertical. Como en DirectX 8. x, D3DPRESENT \_ Interval \_ default se define como cero y es equivalente a D3DPRESENT \_ Interval \_ One. D3DPRESENT \_ Interval \_ default es una comodidad para inicializar \_ los parámetros de D3DPRESENT en cero.

Para obtener una explicación detallada de los modos y los intervalos que se admiten, vea D3DPRESENT.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gráficos de Direct3D 9](dx9-graphics.md)
</dt> </dl>

 

 
