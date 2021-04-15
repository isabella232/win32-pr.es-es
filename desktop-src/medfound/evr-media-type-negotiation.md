---
description: EVR negociación de tipo de medio
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: EVR negociación de tipo de medio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1f87a24db866c9e80b211b0385c12dcd6b594
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361890"
---
# <a name="evr-media-type-negotiation"></a>EVR negociación de tipo de medio

En este tema se describe cómo el representador de vídeo mejorado (EVR) valida los tipos de medios.

-   En el caso del filtro EVR de DirectShow, la negociación de tipos se produce cuando se conectan los PIN del filtro.

-   En el caso del receptor de medios EVR, los tipos de medios se establecen a través de la interfaz [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) en los receptores de flujo. Normalmente, el cargador de topología negocia los tipos de medios, aunque la aplicación también puede establecer los tipos de medios directamente.

EVR no informa de ningún tipo de medio preferido. El cliente debe probar los tipos de medios hasta que encuentre un tipo aceptable. El tipo de medio para la secuencia de referencia debe establecerse antes de que se puedan establecer los tipos en cualquiera de las subsecuencias.

En el flujo de referencia, el mezclador de EVR obtiene una lista de formatos de destino de representación de DirectX video Acceleration (DXVA) compatibles. El presentador de EVR usa esta lista para seleccionar el formato de la cadena de intercambio de Direct3D. Si no se puede encontrar ningún formato de destino de representación compatible, el EVR rechaza el tipo de medio.

En el caso de las subsecuencias, el mezclador EVR consulta si el dispositivo DXVA admite ese formato de subsecuencia en combinación con el formato de destino de representación que se seleccionó para la secuencia de referencia. Como resultado, los formatos de subflujo disponibles pueden cambiar en función del flujo de referencia.

Este es el proceso con más detalle. Estos detalles no son importantes para la mayoría de las aplicaciones, pero pueden resultar útiles si está escribiendo un presentador o mezclador personalizado.

En el flujo de referencia, la negociación se produce de la manera siguiente:

1.  EVR llama a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) en el mezclador.

2.  El mezclador convierte el tipo de medio en una descripción de DXVA 2,0 mediante la [**estructura \_ videodesc de DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) .

3.  El mezclador llama a [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) para obtener una lista de los GUID del procesador de vídeo.

4.  Para cada GUID del procesador de vídeo, el mezclador llama a [**IDirectXVideoProcessorService:: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) para obtener los formatos de destino de representación admitidos.

5.  EVR llama a [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) en el presentador con el mensaje MFVP \_ Message \_ INVALIDATEMEDIATYPE. Este mensaje hace que el presentador Seleccione un nuevo formato.

6.  El presentador llama a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obtener una lista de los formatos de salida disponibles del mezclador. El mezclador genera esta lista a partir de los formatos obtenidos en el paso 4.

7.  El presentador selecciona un formato y llama a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) en el mezclador.

En el caso de las subsecuencias, el proceso es más sencillo:

1.  EVR llama a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) en el mezclador.

2.  El mezclador llama a [**IDirectXVideoProcessorService:: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) para obtener una lista de los formatos de subflujo disponibles.

3.  Si el formato propuesto está contenido en esta lista, EVR acepta el tipo de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> </dl>

 

 



