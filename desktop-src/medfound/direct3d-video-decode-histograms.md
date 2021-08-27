---
description: Este artículo contiene instrucciones para generar histogramas al decodificar vídeo mediante las API de vídeo de Direct3D 11 o 12.
ms.assetid: ''
title: Histogramas de descodificación de vídeo de Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 94371fd68c981a98c4ba629822f928e148c230565b5103dfaa2350543bbe9a57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061635"
---
# <a name="direct3d-video-decode-histograms"></a>Histogramas de descodificación de vídeo de Direct3D

Este artículo contiene instrucciones para generar histogramas al decodificar vídeo mediante las API de vídeo de Direct3D 11 o 12.

## <a name="checking-the-video-device-for-histogram-capabilities"></a>Comprobación de las funcionalidades del histograma en el dispositivo de vídeo

Antes de intentar generar histogramas, debe comprobar si el dispositivo de vídeo actual admite la característica histograma de descodificación de vídeo.

### <a name="direct3d-12"></a>Direct3D 12

Llame [a ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) para comprobar los detalles de soporte técnico de las operaciones de decodificación de vídeo de Direct3D 12. Pase el **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** de la enumeración [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) para especificar que está solicitando compatibilidad con histogramas de descodificación de vídeo.

### <a name="direct3d-11"></a>Direct3D 11

Llame a [ID3D11VideoDevice2::CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) y pase el valor **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** del [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) para determinar si se admiten histogramas para el dispositivo actual.

## <a name="enabling-histogram-during-decode"></a>Habilitación del histograma durante la descodificación

El autor de la llamada habilita la recopilación de datos del histograma proporcionando los búferes en los que se almacenan los datos del histograma.  Un búfer de salida de histograma nulo para un componente determinado indica que la colección de histogramas está deshabilitada.

### <a name="direct3d-12"></a>Direct3D 12

Para proporcionar búferes de salida para recibir datos del histograma mediante Direct3D 12, debe crear la lista de comandos de descodificación mediante el método [ID3D12VideoDecodeCommandList1::D ecodeFrame1.](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) Este método toma una [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) estructura como argumento. **D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** tiene un campo de [tipo D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), que permite especificar un [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) en el que se salidan los datos del histograma.

### <a name="direct3d-11"></a>Direct3D 11

La [interfaz ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) proporciona el método [DecoderBeginFrame1,](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) que permite proporcionar una o varias interfaces [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) en las que se van a generar los datos del histograma. El [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) especificar los componentes para los que desea que se generen los datos del histograma.


## <a name="buffer-format"></a>Formato de búfer

La salida del histograma de descodificación se escribe en un búfer como un contador entero por componente.  El formato de búfer es un valor de 32 bits por cubo.  Un dispositivo puede usar una profundidad de bits de contador entero inferior a 32 bits, pero debe ser de 16, 24 o 32 bits.  Si es así, el valor del contador se almacena en los bits inferiores y los bits superiores no utilizados son cero.  Cuando el recuento de una ubicación superaría el valor máximo, el dispositivo establece el valor máximo en su lugar. Los dispositivos informan del número de contenedores admitidos, que debe ser un valor que sea una potencia de 2.  El número mínimo de contenedores necesarios para los dispositivos que admiten esta característica es 64. 

Debe proporcionar un búfer con un desplazamiento alineado de 256 bytes y un tamaño que sea el número admitido de cubos multiplicado por el tamaño de cubo (4 bytes) para cada componente solicitado.  La selección de ubicación de la ubicación viene determinada por:

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


Cuando un formato define los bits útiles de un componente como menor que el número de bits de almacenamiento (por ejemplo, P010 usa los 10 bits principales de 16 bits de almacenamiento de componentes), solo se consideran los bits útiles (P010 se trata como un valor de 10 bits). 

El dispositivo de vídeo informa de qué componentes se admiten.  Si el autor de la llamada no desea un histograma para un componente determinado, especifica nullptr.  Si el controlador no admite un histograma para un componente determinado, el búfer del histograma de ese componente debe ser nullptr.

Cuando se admiten varios componentes, la aplicación puede solicitar cualquier combinación de componentes por descodificación de fotograma.  Por ejemplo, si el hardware notifica compatibilidad con los componentes Y, U y V, la aplicación puede solicitar el histograma Y solo para el fotograma uno, el histograma U solo para el fotograma dos y el histograma V solo para el fotograma 3.  También pueden solicitar cualquier combinación de dos componentes o los tres componentes.

Las aplicaciones suministran un desplazamiento y un identificador de búfer independientes para cada componente solicitado.  Este puntero puede apuntar al mismo recurso que otro componente o a un recurso independiente.  El desplazamiento permite colocar varios componentes en el mismo búfer, pero la región de salida especificada por el desplazamiento y el tamaño del histograma no deben superponerse a la salida de otro componente de histograma.  El histograma también se puede escribir en el mismo búfer que otro contenido no relacionado, como cuando se usa en una estrategia de subatribución de recursos.


El tiempo de ejecución D3D valida que los llamadores solo habiliten histograma para los componentes admitidos, que el desplazamiento del búfer esté alineado y que el tamaño del búfer sea suficiente para el número notificado de ubicaciones.


## <a name="protected-content"></a>Contenido protegido

Los búferes de histograma deben tener la misma protección de superficie que la superficie de salida de descodificación. Si la superficie de salida de descodificación no es un recurso protegido, el búfer del histograma no debe ser un recurso protegido. Si la superficie de salida de descodificación es un recurso protegido, el histograma debe ser un recurso protegido.








## <a name="related-topics"></a>Temas relacionados

<dl> <dt>API de vídeo 
[de Direct3D 12](direct3d-12-video-apis.md) 
 [Media Foundation de programación](media-foundation-programming-guide.md)
</dt> </dl>

 

 




