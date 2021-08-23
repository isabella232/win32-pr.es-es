---
description: Los mapas de desplazamiento son similares a los mapas de textura, pero el motor de vértices accede a ellos.
ms.assetid: d6f16ff2-5a66-48a3-82c4-523faaafa6ae
title: Asignación de desplazamiento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87b559c2c4758b773c48c0b556b6d61af54549f1b30e5c2693a24c4c27856c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523774"
---
# <a name="displacement-mapping-direct3d-9"></a>Asignación de desplazamiento (Direct3D 9)

Los mapas de desplazamiento son similares a los mapas de textura, pero el motor de vértices accede a ellos.

## <a name="block-diagram"></a>Diagrama de bloques

Hay una fase de muestreo adicional en la parte temprana de la canalización de vértices, como se muestra en el diagrama siguiente, que puede muestrear un mapa de desplazamiento para proporcionar datos de desplazamiento de vértices.

![diagrama de la fase del muestreador en la canalización de vértices](images/tessellatordx9.png)

[**SetSamplerState**](/windows/desktop/api) puede establecer el estado del sampler del mapa de desplazamiento mediante el número de fase 256, que es un nuevo número de fase. [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)establece la textura del mapa de desplazamiento.

El mapa se puede presamplear o no, lo que significa que se puede ordenar de una manera que permita la búsqueda de los valores de desplazamiento sin filtrar.

-   Los mapas de desplazamiento son análogos a los mapas de textura, pero el motor de vértices accede a ellos.
-   Hay una fase de muestreo adicional en la primera parte de la canalización de vértices que puede muestrear un mapa de desplazamiento. La API SetSamplerState habitual accede a esta fase, pero el número de fase es D3DDMAPSAMPLER = 256.
-   SetSamplerState(D3DDMAPSAMPLER, ...) puede establecer el estado del sampler de mapa de desplazamiento. Api.
-   La textura del mapa de desplazamiento se establece mediante la API SetTexture(D3DDMAPSAMPLER, texture).
-   El mapa se puede muestrear previamente o no. Esto significa que se puede ordenar de una manera determinada que permite la búsqueda de los valores de desplazamiento sin filtrar.
-   Los cambios en la estructura de declaración permiten especificar la coordenada de textura usada para buscar el mapa de textura. Por ejemplo, Stream0, Offset, FLOAT2, LOOKUP, Valor de \_ desplazamiento. Esto indica al teselador que use el vector float 2D en stream0 en un desplazamiento determinado como coordenada de textura para buscar el mapa de desplazamiento y asociarle la semántica de uso de valores de \_ desplazamiento. La declaración del sombreador de vértices contendrá una línea similar a {dcl texture0, v0} que indica que la semántica texture0 se asociará al registro de \_ entrada v0. El valor de desplazamiento que se busca se copia en el registro de entrada v0.
-   Hay un tipo especial de asignación de desplazamiento cuando el mapa de textura se muestrea previamente. El índice secuencial de vértices generados se usa como coordenada de textura para un mapa de textura. Por ejemplo, 0,0,(D3DDECLTYPE)0,D3DDECLMETHOD \_ LOOKUPPRESAMPLED, Usage, UsageIndex.
-   La salida de la búsqueda es de 4 flotantes.
-   La asignación de desplazamiento solo se admite con N revisiones.
-   Los controladores deben omitir D3DDMAPSAMPLER en SetTextureStageState si no controlan mapas de desplazamiento.
-   No se admite el modo de filtro D3DTEXF \_ ANISOTROPIC.
-   Cuando D3DSAMP MIPFILTER en el sampler de mapa de desplazamiento no es D3DTEXF NONE, el nivel de detalle se calcula de la manera siguiente (tenga en cuenta que el estado de teselación adaptable se usa incluso si \_ \_ D3DRS \_ ENABLEADAPTIVETESSELLATION es **FALSE**): Tmax = estado de representación D3DRS \_ MAXTESSELLATIONLEVEL
-   Nivel de teselación de proceso Te para un vértice Vi: (Xi, Yi, Zi) de la misma manera que se describe en la sección "Teselación adaptable". Nivel de detalle L = log2(Tmax) - log2 (Te).
-   Las operaciones de filtrado y muestreo de textura siguen las mismas reglas que la canalización de píxeles (nivel de detalle (LOD), etc.).
-   No todos los formatos se pueden usar como mapas de desplazamiento, sino solo los que admiten \_ DMAP D3DUSAGE. La aplicación puede consultarlo con CheckDeviceFormat [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).
-   D3DUSAGE DMAP debe especificarse en CreateTexture para notificar al controlador que esta textura se va a usar como \_ mapa de desplazamiento. [](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   D3DUSAGE \_ DMAP solo se puede usar con texturas. No se puede usar con asignaciones de cubos o volúmenes.
-   Las texturas y los destinos de representación creados con DMAP D3DUSAGE se pueden establecer en fases de muestreador \_ normales y como destinos de representación.
-   Los estados de representación para establecer el modo de ajuste de las coordenadas de textura se omiten en la asignación de desplazamiento. En general, no hay modos de ajuste para el motor de teselador.
-   Un muestreador de mapa de desplazamiento tiene un comportamiento idéntico al de los muestreadores de textura de píxeles. Si se busca una textura con menos de cuatro canales (como R32f), los valores buscados van a los canales adecuados del registro de destino (el registro de entrada del sombreador de vértices etiquetado con la semántica de ejemplo), mientras que los demás canales tienen como valor predeterminado \_ (1, 1, 1). Cuando se busca, D3DFMT L8 se difunde en los canales R, G, B y A tiene como valor predeterminado \_ 1. El rasterizador de referencia tiene todos los detalles de implementación.

## <a name="pre-sampled-displacement-mapping"></a>Asignación de desplazamiento muestreada previamente

-   Se introduce un nuevo estado del muestreador: D3DSAMP DMAPOFFSET (DWORD): desplazamiento (en vértices) en un mapa de desplazamiento previamente \_ muestreado.
-   Se ha introducido un nuevo método de declaración: D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   La teselación adaptable debe deshabilitarse.
-   Se omite la configuración del filtro de textura. Se realiza el muestreo de puntos. Se supone que el filtro de textura mip es D3DTEXF \_ NONE. Se supone que todos los demás modos de filtro de textura son D3DTEXF \_ POINT.
-   Las coordenadas de textura se calculan como: U = (Index % TextureWidthInPixeles) / (float)(TextureWidthInPixeles) V = (Index/TextureWidthInPixeles) / (float)(TextureHeightInPixeles) donde Index es un índice secuencial de vértices generados más TSS \[ D3DSAMP \_ DMAPOFFSET \] . El índice secuencial se establece en cero al principio de cada primitivo y se aumenta después de generar un vértice.

Estos son los cambios de API que admiten la asignación de desplazamiento.

-   Se ha agregado un formato de canal único, D3DFMT \_ L16.
-   Una nueva marca de uso, D3DUSAGE \_ DMAP.
-   Una fase de textura especial, que se usa para establecer una textura de mapa de desplazamiento, D3DDMAPSAMPLER.
-   Se han agregado nuevos límites de hardware, D3DDEVCAPS2 \_ DMAPNPATCH y D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH. Vea [D3DDEVCAPS2.](d3ddevcaps2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 
