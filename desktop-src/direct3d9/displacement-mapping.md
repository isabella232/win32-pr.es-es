---
description: Los mapas de desplazamiento son similares a los mapas de textura, pero el motor de vértices tiene acceso a ellos.
ms.assetid: d6f16ff2-5a66-48a3-82c4-523faaafa6ae
title: Asignación de desplazamiento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b687583b0109223d8c2dac807425e235ddf280e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495311"
---
# <a name="displacement-mapping-direct3d-9"></a>Asignación de desplazamiento (Direct3D 9)

Los mapas de desplazamiento son similares a los mapas de textura, pero el motor de vértices tiene acceso a ellos.

## <a name="block-diagram"></a>Diagrama de bloque

Hay una fase de muestra adicional en la parte temprana de la canalización de vértices, como se muestra en el diagrama siguiente, que puede muestrear un mapa de desplazamiento para proporcionar datos de desplazamiento de vértices.

![diagrama de la fase de muestra en la canalización de vértices](images/tessellatordx9.png)

El estado de muestra del mapa de desplazamiento se puede establecer mediante [**SetSamplerState**](/windows/desktop/api) con el número de fase 256, que es un nuevo número de fase. La textura del mapa de desplazamiento se establece mediante [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).

La asignación se puede premuestrear o no, lo que significa que se puede ordenar de forma que permita la búsqueda de los valores de desplazamiento sin filtrado.

-   Los mapas de desplazamiento son análogos a los mapas de textura, pero el motor de vértices tiene acceso a ellos.
-   Hay una fase de muestra adicional en la parte temprana de la canalización de vértices que puede muestrear un mapa de desplazamiento. A esta fase se accede mediante la API de SetSamplerState habitual, pero el número de fase es D3DDMAPSAMPLER = 256.
-   El estado de muestra del mapa de desplazamiento se puede establecer mediante SetSamplerState (D3DDMAPSAMPLER,...) API.
-   La textura del mapa de desplazamiento se establece mediante la API SetTexture (D3DDMAPSAMPLER, Texture).
-   La asignación se puede mostrar previamente o no. Esto significa que se puede ordenar de una manera determinada que habilita la búsqueda de los valores de desplazamiento sin filtrado.
-   Los cambios en la estructura de declaración permiten la especificación de la coordenada de textura utilizada para buscar el mapa de textura. Por ejemplo, Stream0, offset, FLOAT2, LOOKUP y el \_ valor de desplazamiento. Esto indica a del teselador que use el vector Float 2D en stream0 en un determinado desplazamiento como una coordenada de textura para buscar el mapa de desplazamiento y asociarle la \_ semántica del uso del valor de desplazamiento. La declaración del sombreador de vértices contendría una línea similar a {DCL \_ texture0, V0} que indica que la semántica de texture0 se asociará con el registro de entrada de v0. El valor de desplazamiento buscado se copia en el registro de entrada v0.
-   Hay un tipo especial de asignación de desplazamiento, cuando el mapa de textura se muestrea previamente. El índice secuencial de los vértices generados se utiliza como una coordenada de textura a un mapa de textura. Por ejemplo, 0, 0, (D3DDECLTYPE) 0, D3DDECLMETHOD \_ LOOKUPPRESAMPLED, Usage, UsageIndex.
-   La salida de la búsqueda es 4 flotantes.
-   La asignación de desplazamiento solo se admite con N-patches.
-   Los controladores deben omitir D3DDMAPSAMPLER en SetTextureStageState si no controlan los mapas de desplazamiento.
-   \_No se admite el modo de filtro anisotrópico de D3DTEXF.
-   Cuando D3DSAMP \_ MIPFILTER de la muestra de mapa de desplazamiento no es D3DTEXF \_ ninguno, el nivel de detalle se calcula como se indica a continuación (tenga en cuenta que el estado de teselación adaptable se usa incluso si el \_ ENABLEADAPTIVETESSELLATION D3DRS es **false**): Tmax = estado de representación D3DRS \_ MAXTESSELLATIONLEVEL
-   Nivel de teselación de proceso de un vértice VI: (XI, Yi, Zi) de la misma manera que se describe en la sección "teselación adaptativa". Nivel de detalle L = LOG2 (Tmax)-LOG2 (te).
-   Las operaciones de filtrado y muestreo de textura siguen las mismas reglas que se aplican a la canalización de píxeles (el nivel de detalle (LOD), etc.).
-   No todos los formatos se pueden usar como mapas de desplazamiento, sino solo aquellos que admiten \_ DMAP D3DUSAGE. La aplicación puede consultarlo con el [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)de CheckDeviceFormat.
-   D3DUSAGE \_ DMAP se debe especificar en [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) para notificar al controlador que esta textura se va a usar como un mapa de desplazamiento.
-   D3DUSAGE \_ DMAP solo se puede usar con texturas. No se puede usar con asignaciones o volúmenes de cubos.
-   Las texturas y los destinos de representación creados con D3DUSAGE \_ DMAP se pueden establecer en fases normales de muestra y como destinos de representación.
-   Los Estados de representación para establecer el modo de ajuste para las coordenadas de textura se omiten en la asignación de desplazamiento. En general, no hay modos de ajuste para el motor de del teselador.
-   Una muestra de mapa de desplazamiento tiene un comportamiento idéntico al de los ejemplos de textura de píxeles. Si se busca una textura con menos de cuatro canales (como R32f), los valores buscados van a los canales adecuados del registro de destino (el registro de entrada del sombreador de vértices etiquetado con la \_ semántica del ejemplo), mientras que los demás canales tienen como valor predeterminado (1, 1, 1). Cuando se busca, D3DFMT \_ L8 se emite en los canales R, G, B y el valor predeterminado es 1. El rasterizador de referencia tiene los detalles de implementación completos.

## <a name="pre-sampled-displacement-mapping"></a>Asignación de desplazamiento previamente muestreada

-   Se introduce un nuevo estado de muestra: D3DSAMP \_ DMAPOFFSET (DWORD)-offset (en vértices) en un mapa de desplazamiento premuestreado.
-   Se presentó el nuevo método de declaración: D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   La teselación adaptable debe estar deshabilitada.
-   Se omite la configuración del filtro de textura. Se realiza el muestreo de puntos. Se supone que el filtro de textura MIP es D3DTEXF \_ ninguno. Se supone que todos los demás modos de filtro de textura son D3DTEXF \_ Point.
-   Las coordenadas de textura se calculan como: U = (índice% TextureWidthInPixeles)/(float) (TextureWidthInPixeles) V = (index/TextureWidthInPixeles)/(float) (TextureHeightInPixeles), donde index es un índice secuencial de los vértices generados más TSS D3DSAMP DMAPOFFSET \[ \_ \] . El índice secuencial se establece en cero al principio de cada primitiva y se aumenta después de que se genere un vértice.

Estos son los cambios de la API que admiten la asignación de desplazamiento.

-   Un formato de canal único agregado, D3DFMT \_ L16.
-   Una nueva marca de uso, D3DUSAGE \_ DMAP.
-   Una fase de textura especial, que se usa para establecer una textura de mapa de desplazamiento, D3DDMAPSAMPLER.
-   Se han agregado nuevas Cap de hardware, D3DDEVCAPS2 \_ DMAPNPATCH y D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH. Vea [D3DDEVCAPS2](d3ddevcaps2.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 
