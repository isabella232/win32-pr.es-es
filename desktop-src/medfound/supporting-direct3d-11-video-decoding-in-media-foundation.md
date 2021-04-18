---
description: En este tema se describe cómo admitir Microsoft Direct3D 11 en un descodificador de Microsoft Media Foundation.
ms.assetid: 656556AA-0266-4318-9D3C-AED75BD728F6
title: Compatibilidad con la descodificación de vídeo Direct3D 11 en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542f7244922dc7947f22e4d33027fdcac1962fe5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670083"
---
# <a name="supporting-direct3d-11-video-decoding-in-media-foundation"></a>Compatibilidad con la descodificación de vídeo Direct3D 11 en Media Foundation

En este tema se describe cómo admitir Microsoft Direct3D 11 en un descodificador de Microsoft Media Foundation. En concreto, describe la comunicación entre el descodificador y el representador de vídeo. En este tema no se describe cómo implementar las operaciones de descodificación.

-   [Información general](#overview)
-   [Abrir un identificador de dispositivo](#open-a-device-handle)
-   [Buscar una configuración de descodificador](#find-a-decoder-configuration)
-   [Retroceso a descodificación de software](#fallback-to-software-decoding)
-   [Asignación de búferes sin comprimir](#allocating-uncompressed-buffers)
-   [Descodificación](#supporting-direct3d-11-video-decoding-in-media-foundation)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

En el resto de este tema, se usan los términos siguientes:

-   **Descodificador de software**. El descodificador de software es la transformación de Media Foundation (MFT) que recibe ejemplos de vídeo comprimidos y genera tramas de vídeo sin comprimir.
-   **Dispositivo descodificador**. El dispositivo descodificador es el acelerador de vídeo y lo implementa el controlador de gráficos. El dispositivo descodificador realiza operaciones de descodificación aceleradas.
-   **Canalización**. La canalización hospeda el descodificador de software y proporciona búferes hacia y desde el descodificador de software. Dependiendo de la aplicación, la canalización podría ser la [sesión multimedia](media-session.md), el [lector de origen](source-reader.md)o el código de aplicación que llama directamente a la MFT.

Para realizar la descodificación con Direct3D 11, el descodificador de software debe tener un puntero a un dispositivo Direct3D 11. El dispositivo Direct3D 11 se crea externamente en el descodificador de software. En un escenario de [sesión multimedia](media-session.md) , el representador de vídeo crea el dispositivo Direct3D 11. En un escenario de [lector de código fuente](source-reader.md) , normalmente la aplicación crea el dispositivo Direct3D 11.

El Administrador de dispositivos de DXGI se usa para compartir Direct3D 11 entre los componentes. El Administrador de dispositivos de DXGI expone la interfaz [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) . La canalización establece el puntero **IMFDXGIDeviceManager** en el descodificador de software mediante el envío del mensaje de [**\_ \_ \_ \_ Administrador D3D del conjunto de mensajes MFT**](mft-message-set-d3d-manager.md) .

En el diagrama siguiente se muestra la relación entre el descodificador de software, Direct3D 11 y la canalización.

![diagrama que muestra el descodificador de software y el administrador de dispositivos de dxgi.](images/d3d11video01.png)

Estos son los pasos básicos que debe realizar un descodificador de software para admitir Direct3D 11 en Media Foundation:

1.  Abra un identificador para el dispositivo Direct3D 11.
2.  Busque una configuración de descodificador.
3.  Asignar búferes sin comprimir.
4.  Descodificar fotogramas.

Estos pasos se describen con más detalle en el resto de este tema.

## <a name="open-a-device-handle"></a>Abrir un identificador de dispositivo

La MFT del descodificador usa el administrador de dispositivos de DXGI para obtener un identificador para el dispositivo Direct3D 11. Para abrir el identificador del dispositivo, realice los pasos siguientes:

1.  La MFT del descodificador debe exponer el atributo de [ \_ \_ \_ reconocimiento de SA D3D11 de MF](mf-sa-d3d11-aware.md) con el valor **true**.
2.  El cargador de topología consulta este atributo mediante una llamada a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). El valor **true** indica que MFT es compatible con Direct3D 11.
3.  El cargador de topología llama a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el mensaje de administrador de D3D del conjunto de mensajes de [**MFT \_ \_ \_ \_**](mft-message-set-d3d-manager.md) . El parámetro *ulParam* es un puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) al administrador de dispositivos de DXGI. Consulte este puntero para la interfaz [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .
4.  Llame a [**IMFDXGIDeviceManager:: OpenDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle) para obtener un identificador para el dispositivo Direct3D 11.
5.  Para obtener un puntero al dispositivo Direct3D 11, llame a [**IMFDXGIDeviceManager:: GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). Pase el identificador de dispositivo y el IID de valor **\_ ID3D11Device**. El método devuelve un puntero a la interfaz [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) .
6.  Para obtener un puntero al Acelerador de vídeo, llame a [**IMFDXGIDeviceManager:: GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice) de nuevo. Esta vez, pase el identificador de dispositivo y el IID de valor **\_ ID3D11VideoDevice**. El método devuelve un puntero a la interfaz [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) .
7.  Llame a [**ID3D11Device:: GetImmediateContext**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-getimmediatecontext) para obtener un puntero [**ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) .
8.  Llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en [**ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) para obtener un puntero [**ID3D11VideoContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext) .
9.  Se recomienda usar la protección multiproceso en el contexto de dispositivo para evitar problemas de interbloqueo que a veces pueden producirse cuando se llama a [**ID3D11VideoContext:: GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) o [**ID3D11VideoContext:: ReleaseDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer). Para establecer la protección de varios subprocesos, llame primero a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) para obtener un puntero [**ID3D10Multithread**](/windows/win32/api/d3d10/nn-d3d10-id3d10multithread) . Después, llame a [**ID3D10Multithread:: SetMultithreadProtected**](/windows/win32/api/d3d10/nf-d3d10-id3d10multithread-setmultithreadprotected), pasando **true** para *bMTProtect*.

## <a name="find-a-decoder-configuration"></a>Buscar una configuración de descodificador

Para realizar la descodificación, el descodificador de software debe buscar una configuración compatible compatible con el dispositivo descodificador, incluido un formato de destino de representación. Este paso se produce dentro del método [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) , como se indica a continuación.

1.  Valide el tipo de medio de entrada. Si el tipo es rechazado, omita los pasos restantes y devuelva un código de error.
2.  Llame a [**ID3D11VideoDevice:: GetVideoDecoderProfileCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) para obtener el número de perfiles admitidos.
3.  Llame a [**ID3D11VideoDevice:: GetVideoDecoderProfile**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) para enumerar los perfiles y obtener los GUID de perfil.
4.  Busque un GUID de perfil que coincida con el formato de vídeo y las capacidades del descodificador de software. Por ejemplo, un descodificador de MPEG-2 encontraría el perfil de descodificador de **D3D11 \_ \_ \_ MPEG2 \_ MOCOMP**, el **Perfil de \_ descodificador D3D11 \_ \_ MPEG2 \_ IDCT** y el **Perfil de \_ descodificador de D3D11 \_ \_ MPEG2 \_ VLD**.
5.  Si se encuentra un GUID de descodificador adecuado, compruebe el formato de salida llamando al método [**ID3D11VideoDevice:: CheckVideoDecoderFormat**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) . Pase el GUID del descodificador y un valor de **\_ formato de DXGI** que especifique el formato de destino de representación.
6.  A continuación, busque una configuración adecuada para el descodificador.
    1.  Llame a [**ID3D11VideoDevice:: GetVideoDecoderConfigCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) para obtener el número de configuraciones del descodificador. Pase el mismo GUID del dispositivo descodificador, junto con una [**estructura \_ \_ \_ DESC del descodificador de vídeo D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc) que describe el formato de destino de representación propuesto.
    2.  Llame a [**ID3D11VideoDevice:: GetVideoDecoderConfig**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) para enumerar las configuraciones del descodificador.

En el método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , devuelve un formato de vídeo sin comprimir basado en el formato de destino de representación propuesto.

En el método [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , compruebe el tipo de medio con el formato de destino de representación.

## <a name="fallback-to-software-decoding"></a>Retroceso a descodificación de software

Es posible que la MFT no pueda encontrar una configuración. Por ejemplo, es posible que el controlador de gráficos no admita las capacidades adecuadas. En ese caso, la MFT debe revertir a la descodificación de software, como se indica a continuación.

1.  Los métodos [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) y [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) deben devolver el **\_ \_ \_ \_ tipo D3D no compatible con MF E**.
2.  En respuesta, el cargador de topología enviará el mensaje de [**\_ \_ \_ \_ Administrador D3D de conjunto de mensajes MFT**](mft-message-set-d3d-manager.md) con el valor **null** para el parámetro *ulParam* .
3.  MFT libera su puntero a la interfaz [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .
4.  El cargador de topología vuelve a negociar el tipo de medio.

En este momento, la MFT puede usar la descodificación de software.

## <a name="allocating-uncompressed-buffers"></a>Asignación de búferes sin comprimir

El descodificador es responsable de asignar las texturas de Direct3D 11 para usarlas como búferes de vídeo sin comprimir. El atributo de [ \_ \_ \_ \_ \_ recuento de ejemplo de salida mínima de MF SA](mf-sa-minimum-output-sample-count.md) en los atributos del flujo de salida (vea [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)) se usa para determinar cuántas superficies debe asignar el descodificador para que el representador de vídeo las use para el desentrelazado. Un descodificador debe usar este valor para delimitarlo para algunos límites superiores y inferiores razonables, por ejemplo 3-32. Para obtener contenido progresivo, vea [ \_ ejemplo de salida mínima de MF SA \_ \_ \_ \_ recuento \_ progresiva](mf-sa-minimum-output-sample-count-progressive.md).

En el método [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) , establezca el **flujo de salida de MFT proporciona la marca \_ \_ \_ \_ Samples** en la estructura de información del flujo de salida de [**MFT \_ \_ \_**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) . Esta marca notifica a la sesión de medios que la MFT asigna sus propios ejemplos de salida. Para asignar los ejemplos de salida, la MFT realiza los pasos siguientes:

1.  Cree una matriz de textura 2D llamando a [**ID3D11Device:: CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d). En la estructura [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-d3d11_texture2d_desc) , establezca **tamaño** igual al número de superficies que necesita el descodificador. Esto incluye:
    -   Superficies para fotogramas de referencia.
    -   Superficies para el desentrelazado (tres superficies).
    -   Superficies que el descodificador necesita para el almacenamiento en búfer.

    Las marcas de enlace (**BindFlags**) deben incluir la marca de **\_ \_ descodificador de enlace D3D11** y cualquier marca de enlace establecida mediante el atributo [MF \_ SA \_ D3D11 \_ BindFlags](mf-sa-d3d11-bindflags.md) en los atributos del flujo de salida.
2.  Para cada superficie de la matriz de textura, llame a [**ID3D11VideoDevice:: CreateVideoDecoderOutputView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) para crear una vista de salida del descodificador de vídeo. Durante la descodificación, estas vistas de salida se pasarán al método [**ID3D11VideoContext::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) .
3.  Para cada superficie de la matriz de textura, cree un ejemplo multimedia como se indica a continuación:
    1.  Cree un búfer de medios de DXGI mediante una llamada a la función [**MFCreateDXGISurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer) . Pase el puntero [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) y el desplazamiento de cada elemento de la matriz de textura. La función devuelve un puntero [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .
    2.  Cree un ejemplo vacío mediante una llamada a la función [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) . Establezca el parámetro *pUnkSurface* en **null**. La función devuelve un puntero [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .
    3.  Llame a [**IMFSample:: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) para agregar el búfer multimedia al ejemplo.

Debe destruir todas las texturas que cree al mismo tiempo, en lugar de destruir solo algunas y continuar usando el recordatorio.

## <a name="decoding"></a>Descodificación

Para crear el dispositivo descodificador, llame a [**ID3D11VideoDevice:: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder). El método devuelve un puntero a la interfaz [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) . La descodificación debe realizarse dentro del método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . En cada fotograma, llame a [**IMFDXGIDeviceManager:: TestDevice**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-testdevice) para probar la disponibilidad de DXGI. Si el dispositivo ha cambiado, el descodificador de software debe volver a crear el dispositivo descodificador, como se indica a continuación:

1.  Cierre el identificador del dispositivo mediante una llamada a [**IMFDXGIDeviceManager:: CloseDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-closedevicehandle).
2.  Libera todos los recursos asociados con el dispositivo Direct3D 11 anterior, incluidas las interfaces [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder), [**ID3D11VideoContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext), [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d)y [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) .
3.  Abra un nuevo identificador de dispositivo.
4.  Negocie una nueva configuración del descodificador, tal y como se describió anteriormente en [buscar una configuración de descodificador](#find-a-decoder-configuration). Este paso es necesario porque es posible que las funcionalidades del dispositivo hayan cambiado.
5.  Cree un nuevo dispositivo descodificador.

Suponiendo que el identificador del dispositivo es válido, el proceso de descodificación funciona de la siguiente manera:

1.  Obtiene una superficie disponible que no está actualmente en uso. Inicialmente, todas las superficies están disponibles.
2.  Consulte el ejemplo multimedia para la interfaz [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .
3.  Llame a [**IMFTrackedSample:: SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) y proporcione un puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . (El descodificador de software debe implementar esta interfaz). Cuando el representador de vídeo libera el ejemplo, se invocará la devolución de llamada. Utilice esta devolución de llamada para realizar un seguimiento de los ejemplos que están disponibles actualmente y que están en uso.
4.  Llame a [**ID3D11VideoContext::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe). Pase los punteros a la interfaz [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) para el dispositivo descodificador y la interfaz [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) para la vista de salida.
5.  Haga lo siguiente una o varias veces:
    1.  Llame a [**ID3D11VideoContext:: GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) para obtener un búfer.
    2.  Rellene el búfer.
    3.  Llame a [**ID3D11VideoContext:: ReleaseDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer).
    4.  Llame a [**ID3D11VideoContext:: SubmitDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers). Este método indica al dispositivo descodificador que realice las operaciones de descodificación en el marco.
6.  Llame a [**ID3D11VideoContext::D ecoderendframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) para indicar el final de la descodificación del marco actual.

Direct3D 11 usa las mismas estructuras de datos que DXVA 2,0 para las operaciones de descodificación. En el conjunto original de perfiles de DXVA (para H. 261, H. 263 y MPEG-2), estas estructuras de datos se describen en la [especificación de DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

Dentro de cada par de llamadas a [**DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) y [**SubmitDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) , puede llamar a [**GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) varias veces, pero solo una vez para cada tipo de búfer. Si usa el mismo tipo de búfer dos veces sin llamar a **SubmitDecoderBuffer**, sobrescribirá los datos en el búfer.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de vídeo de Direct3D 11](direct3d-11-video-apis.md)
</dt> <dt>

[Aceleración de vídeo de DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
