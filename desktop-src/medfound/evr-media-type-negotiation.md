---
description: Negociación de tipos de medios EVR
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: Negociación de tipos de medios EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6255a32f876a48d0c6193c0a9b470d20ee178ee0ae6fe4c0504b110a353075b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974494"
---
# <a name="evr-media-type-negotiation"></a>Negociación de tipos de medios EVR

En este tema se describe cómo el representador de vídeo mejorado (EVR) valida los tipos de medios.

-   Para el DirectShow EVR, la negociación de tipos se produce cuando se conectan los pines del filtro.

-   Para el receptor de medios EVR, los tipos de medios se establecen a través de la [**interfaz IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) en los receptores de flujo. Normalmente, el cargador de topología negocia los tipos de medios, aunque la aplicación también puede establecer los tipos de medios directamente.

EvR no informa de ningún tipo de medio preferido. El cliente debe probar los tipos de medios hasta que encuentre un tipo aceptable. El tipo de medio para la secuencia de referencia debe establecerse antes de que los tipos se puedan establecer en cualquiera de las sub secuencias.

Para la secuencia de referencia, el mezclador EVR obtiene una lista de formatos de destino de representación compatibles con directX Video Acceleration (DXVA). El presentador de EVR usa esta lista para seleccionar el formato de la cadena de intercambio de Direct3D. Si no se encuentra ningún formato de destino de representación compatible, evr rechaza el tipo de medio.

Para las substreams, el mezclador EVR consulta si el dispositivo DXVA admite ese formato de substream en combinación con el formato de destino de representación seleccionado para la secuencia de referencia. Como resultado, los formatos de subtransmisión disponibles pueden cambiar en función de la secuencia de referencia.

Este es el proceso con más detalle. Estos detalles no son importantes para la mayoría de las aplicaciones, pero pueden resultar útiles si escribe un mezclador o presentador personalizado.

Para la secuencia de referencia, la negociación se produce de la siguiente manera:

1.  El EVR llama [**a IMFTransform::SetInputType en**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) el mezclador.

2.  El mezclador convierte el tipo de medio en una descripción de DXVA 2.0, mediante la [**estructura \_ DxVA2 VideoDesc.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc)

3.  El mezclador llama [**a IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) para obtener una lista de GUID del procesador de vídeo.

4.  Para cada GUID del procesador de vídeo, el mezclador llama a [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) para obtener los formatos de destino de representación admitidos.

5.  EvR llama [**a MFVideoPresenter::P rocessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) en el presentador con el mensaje MFVP \_ MESSAGE \_ INVALIDATEMEDIATYPE. Este mensaje hace que el presentador seleccione un nuevo formato.

6.  El presentador llama a [**IMFTransform::GetOutputAvailableType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) obtener una lista de los formatos de salida disponibles del mezclador. El mezclador genera esta lista a partir de los formatos obtenidos en el paso 4.

7.  El presentador selecciona un formato y llama a [**IMFTransform::SetOutputType en**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) el mezclador.

En el caso de las subrecciones, el proceso es más sencillo:

1.  El EVR llama [**a IMFTransform::SetInputType en**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) el mezclador.

2.  El mezclador llama a [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) para obtener una lista de los formatos de substream disponibles.

3.  Si el formato propuesto está incluido en esta lista, evr acepta el tipo de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> </dl>

 

 



