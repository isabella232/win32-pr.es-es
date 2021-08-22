---
description: En este tema se describe cómo admitir Microsoft Direct3D 11 en un Microsoft Media Foundation descodificador.
ms.assetid: 656556AA-0266-4318-9D3C-AED75BD728F6
title: Compatibilidad con la decodificación de vídeo de Direct3D 11 en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95a1d1bc1dd9987fe59fe807e56aa9af1ea4ad597b72c077906483d623e11e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972893"
---
# <a name="supporting-direct3d-11-video-decoding-in-media-foundation"></a>Compatibilidad con la decodificación de vídeo de Direct3D 11 en Media Foundation

En este tema se describe cómo admitir Microsoft Direct3D 11 en un Microsoft Media Foundation descodificador. En concreto, describe la comunicación entre el descodificador y el representador de vídeo. En este tema no se describe cómo implementar las operaciones de decoding.

-   [Información general](#overview)
-   [Abrir un identificador de dispositivo](#open-a-device-handle)
-   [Buscar una configuración de descodificador](#find-a-decoder-configuration)
-   [Reserva a la decodificación de software](#fallback-to-software-decoding)
-   [Asignación de búferes sin comprimir](#allocating-uncompressed-buffers)
-   [Descodificación](#supporting-direct3d-11-video-decoding-in-media-foundation)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

En el resto de este tema, se usan los siguientes términos:

-   **Descodificador de software**. El descodificador de software es Media Foundation transformación de archivos (MFT) que recibe ejemplos de vídeo comprimidos y genera fotogramas de vídeo sin comprimir.
-   **Descodificador del dispositivo**. El dispositivo descodificador es el acelerador de vídeo y lo implementa el controlador de gráficos. El dispositivo descodificador realiza operaciones de descodificación acelerada.
-   **Canalización**. La canalización hospeda el descodificador de software y entrega búferes hacia y desde el descodificador de software. Dependiendo de la aplicación, la canalización [](source-reader.md)podría ser la sesión [multimedia,](media-session.md)el lector de origen o el código de aplicación que llama directamente a MFT.

Para realizar la descodificación mediante Direct3D 11, el descodificador de software debe tener un puntero a un dispositivo Direct3D 11. El dispositivo Direct3D 11 se crea externamente en el descodificador de software. En un [escenario de sesión multimedia,](media-session.md) el representador de vídeo crea el dispositivo Direct3D 11. En un [escenario de lector de](source-reader.md) origen, normalmente la aplicación crea el dispositivo Direct3D 11.

El Administrador de dispositivos DXGI se usa para compartir Direct3D 11 entre componentes. El Administrador de dispositivos DXGI expone la [**interfaz IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) La canalización establece el puntero **IMFDXGIDeviceManager** en el descodificador de software mediante el envío del mensaje [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER.**](mft-message-set-d3d-manager.md)

En el diagrama siguiente se muestra la relación entre el descodificador de software, Direct3D 11 y la canalización.

![diagrama que muestra el descodificador de software y el administrador de dispositivos dxgi.](images/d3d11video01.png)

Estos son los pasos básicos que debe realizar un descodificador de software para admitir Direct3D 11 en Media Foundation:

1.  Abra un identificador en el dispositivo Direct3D 11.
2.  Busque una configuración de descodificador.
3.  Asigne búferes sin comprimir.
4.  Descodificar fotogramas.

Estos pasos se describen con más detalle en el resto de este tema.

## <a name="open-a-device-handle"></a>Abrir un identificador de dispositivo

El descodificador MFT usa el administrador de dispositivos DXGI para obtener un identificador para el dispositivo Direct3D 11. Para abrir el identificador del dispositivo, realice los pasos siguientes:

1.  El descodificador MFT debe exponer el atributo [MF \_ SA \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md) con el valor **TRUE**.
2.  El cargador de topologías consulta este atributo mediante una llamada [**a IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). El valor **TRUE** indica que MFT admite Direct3D 11.
3.  El cargador de topologías llama [**a IMFTransform::P rocessMessage con**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) el mensaje [**MFT MESSAGE SET \_ \_ \_ D3D \_ MANAGER.**](mft-message-set-d3d-manager.md) El *parámetro ulParam* es un [**puntero IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) al administrador de dispositivos DXGI. Consulte este puntero para la [**interfaz IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)
4.  Llame [**a IMFDXGIDeviceManager::OpenDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle) para obtener un identificador para el dispositivo Direct3D 11.
5.  Para obtener un puntero al dispositivo Direct3D 11, llame a [**IMFDXGIDeviceManager::GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). Pase el identificador del dispositivo y el valor **IID \_ ID3D11Device**. El método devuelve un puntero a la [**interfaz ID3D11Device.**](/windows/win32/api/d3d11/nn-d3d11-id3d11device)
6.  Para obtener un puntero al acelerador de vídeo, llame de nuevo [**a IMFDXGIDeviceManager::GetVideoService.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice) Esta vez, pase el identificador del dispositivo y el valor **IID \_ ID3D11VideoDevice**. El método devuelve un puntero a la [**interfaz ID3D11VideoDevice.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice)
7.  Llame [**a ID3D11Device::GetImmediateContext**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-getimmediatecontext) para obtener un [**puntero ID3D11DeviceContext.**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext)
8.  Llame [**a QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en [**ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) para obtener un [**puntero ID3D11VideoContext.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext)
9.  Se recomienda usar la protección multiproceso en el contexto del dispositivo para evitar problemas de interbloqueo que a veces pueden producirse al llamar a [**ID3D11VideoContext::GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) o [**ID3D11VideoContext::ReleaseDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer). Para establecer la protección multiproceso, primero llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) para obtener un [**puntero ID3D10Multithread.**](/windows/win32/api/d3d10/nn-d3d10-id3d10multithread) A [**continuación, llame a ID3D10Multithread::SetMultithreadProtected**](/windows/win32/api/d3d10/nf-d3d10-id3d10multithread-setmultithreadprotected), pasando **true** para *bMTProtect*.

## <a name="find-a-decoder-configuration"></a>Buscar una configuración de descodificador

Para realizar la descodificación, el descodificador de software debe encontrar una configuración compatible que sea compatible con el dispositivo descodificador, incluido un formato de destino de representación. Este paso se produce dentro del [**método IMFTransform::SetInputType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) como se muestra a continuación.

1.  Valide el tipo de medio de entrada. Si se rechaza el tipo, omita los pasos restantes y devuelva un código de error.
2.  Llame [**a ID3D11VideoDevice::GetVideoDecoderProfileCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) para obtener el número de perfiles admitidos.
3.  Llame [**a ID3D11VideoDevice::GetVideoDecoderProfile**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) para enumerar los perfiles y obtener los GUID de perfil.
4.  Busque un GUID de perfil que coincida con el formato de vídeo y las funcionalidades del descodificador de software. Por ejemplo, un descodificador MPEG-2 buscaría **D3D11 \_ DECODER \_ PROFILE \_ MPEG2 \_ MOCOMP,****D3D11 \_ DECODER PROFILE \_ \_ MPEG2 \_ IDCT** y **D3D11 \_ DECODER PROFILE \_ \_ MPEG2 \_ VLD**.
5.  Si se encuentra un GUID de descodificador adecuado, compruebe el formato de salida llamando al método [**ID3D11VideoDevice::CheckVideoDecoderFormat.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) Pase el GUID del descodificador y un **valor \_ DXGI FORMAT** que especifique el formato render-target.
6.  A continuación, busque una configuración adecuada para el descodificador.
    1.  Llame [**a ID3D11VideoDevice::GetVideoDecoderConfigCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) para obtener el número de configuraciones de descodificador. Pase el mismo GUID del dispositivo descodificador, junto con una estructura [**\_ \_ \_ DESC de DESCODIFICADOR DE VÍDEO D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc) que describe el formato de destino de representación propuesto.
    2.  Llame [**a ID3D11VideoDevice::GetVideoDecoderConfig**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) para enumerar las configuraciones del descodificador.

En el [**método IMFTransform::GetOutputAvailableType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) devuelva un formato de vídeo sin comprimir basado en el formato de destino de representación propuesto.

En el [**método IMFTransform::SetOutputType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) compruebe el tipo de medio con el formato de destino de representación.

## <a name="fallback-to-software-decoding"></a>Reserva a la decodificación de software

Es posible que MFT no pueda encontrar una configuración. Por ejemplo, es posible que el controlador de gráficos no admita las funcionalidades correctas. En ese caso, MFT debe volver a lacodación de software, como se muestra a continuación.

1.  Los [**métodos SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) y [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) deben devolver **MF E \_ \_ UNSUPPORTED \_ D3D \_ TYPE**.
2.  En respuesta, el cargador de topologías enviará el mensaje [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) con el valor **NULL** para el *parámetro ulParam.*
3.  El MFT libera su puntero a la [**interfaz IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)
4.  El cargador de topologías vuelve a negociar el tipo de medio.

En este momento, MFT puede usar la decodificación de software.

## <a name="allocating-uncompressed-buffers"></a>Asignación de búferes sin comprimir

El descodificador es responsable de asignar texturas de Direct3D 11 para usarlas como búferes de vídeo sin comprimir. El atributo [MF SA MINIMUM OUTPUT SAMPLE \_ \_ \_ \_ \_ COUNT](mf-sa-minimum-output-sample-count.md) en los atributos del flujo de salida (vea [**MFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)) se usa para determinar cuántas superficies debe asignar el descodificador para que el representador de vídeo use para desinterlazar . Un descodificador debe usar este valor que lo limite para algunos límites superiores e inferiores razonables, por ejemplo, 3-32. Para obtener contenido progresiva, vea [MF SA MINIMUM OUTPUT SAMPLE COUNT \_ \_ \_ \_ \_ \_ PROGRESSIVE](mf-sa-minimum-output-sample-count-progressive.md).

En el [**método IMFTransform::GetOutputStreamInfo,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) establezca la marca **MFT \_ OUTPUT STREAM \_ PROVIDES \_ \_ SAMPLES** en la estructura [**\_ MFT OUTPUT STREAM \_ \_ INFO.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) Esta marca notifica a la sesión multimedia que MFT asigna sus propios ejemplos de salida. Para asignar los ejemplos de salida, MFT realiza los pasos siguientes:

1.  Cree una matriz de texturas 2D llamando a [**ID3D11Device::CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d). En la [**estructura D3D11 \_ TEXTURE2D \_ DESC,**](/windows/win32/api/d3d11/ns-d3d11-d3d11_texture2d_desc) establezca **ArraySize** igual al número de superficies que necesita el descodificador. Esto incluye:
    -   Superficies para fotogramas de referencia.
    -   Superficies para desinterlazar (tres superficies).
    -   Superficies que el descodificador necesita para almacenar en búfer.

    Las marcas de enlace (**BindFlags**) deben incluir la marca BIND DECODER de **D3D11 \_ \_** y las marcas de enlace establecidas a través del atributo [MF SA \_ \_ D3D11 \_ BINDFLAGS](mf-sa-d3d11-bindflags.md) en los atributos del flujo de salida.
2.  Para cada superficie de la matriz de texturas, llame a [**ID3D11VideoDevice::CreateVideoDecoderOutputView para**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) crear una vista de salida del descodificador de vídeo. Durante lacodización, estas vistas de salida se pasarán al [**método ID3D11VideoContext::D ecoderBeginFrame.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)
3.  Para cada superficie de la matriz de texturas, cree un ejemplo multimedia como se muestra a continuación:
    1.  Cree un búfer multimedia DXGI mediante una llamada a [**la función MFCreateDXGISurfaceBuffer.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer) Pase el [**puntero ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) y el desplazamiento de cada elemento de la matriz de textura. La función devuelve un [**puntero IMFMediaBuffer.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
    2.  Cree un ejemplo multimedia vacío mediante una llamada a [**la función MFCreateVideoSampleFromSurface.**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) Establezca el *parámetro pUnkSurface* igual a **NULL.** La función devuelve un [**puntero DESEJEMPLO.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
    3.  Llame [**a IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) para agregar el búfer multimedia al ejemplo.

Debe destruir todas las texturas que cree al mismo tiempo, en lugar de destruir solo algunas y seguir utilizando el recordatorio.

## <a name="decoding"></a>Descodificación

Para crear el dispositivo descodificador, llame a [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder). El método devuelve un puntero a la [**interfaz ID3D11VideoDecoder.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) Lacoding debe producirse dentro del [**método IMFTransform::P rocessOutput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) En cada fotograma, llame [**a IMFDXGIDeviceManager::TestDevice**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-testdevice) para probar la disponibilidad de DXGI. Si el dispositivo ha cambiado, el descodificador de software debe volver a crear el dispositivo descodificador, como se muestra a continuación:

1.  Cierre el identificador del dispositivo mediante una llamada [**a IMFDXGIDeviceManager::CloseDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-closedevicehandle).
2.  Libere todos los recursos asociados al dispositivo Direct3D 11 anterior, incluidas las interfaces [**ID3D11VideoDecoder,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) [**ID3D11VideoContext,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext) [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d)e [**ID3D11VideoDecoderOutputView.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview)
3.  Abra un nuevo identificador de dispositivo.
4.  Negocie una nueva configuración de descodificador, como se describió anteriormente en [Buscar una configuración de descodificador.](#find-a-decoder-configuration) Este paso es necesario porque las funcionalidades del dispositivo podrían haber cambiado.
5.  Cree un nuevo dispositivo descodificador.

Suponiendo que el identificador del dispositivo es válido, el proceso de descodización funciona de la siguiente manera:

1.  Obtenga una superficie disponible que no esté actualmente en uso. Inicialmente, todas las superficies están disponibles.
2.  Consulte el ejemplo multimedia para la [**interfaz DESTRACKEDSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)
3.  Llame [**a IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) y proporcione un puntero a la [**interfaz IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) (El descodificador de software debe implementar esta interfaz). Cuando el representador de vídeo libera el ejemplo, se invoca la devolución de llamada. Use esta devolución de llamada para realizar un seguimiento de qué muestras están disponibles actualmente y cuáles están en uso.
4.  Llame [**a ID3D11VideoContext::D ecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe). Pase los punteros a la interfaz [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) del dispositivo descodificador y a la interfaz [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) para la vista de salida.
5.  Haga lo siguiente una o varias veces:
    1.  Llame [**a ID3D11VideoContext::GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) para obtener un búfer.
    2.  Rellene el búfer.
    3.  Llame [**a ID3D11VideoContext::ReleaseDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer).
    4.  Llame [**a ID3D11VideoContext::SubmitDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers). Este método indica al dispositivo descodificador que realice las operaciones de descodificación en el marco.
6.  Llame [**a ID3D11VideoContext::D ecoderEndFrame para**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) indicar el final de lacodización del marco actual.

Direct3D 11 usa las mismas estructuras de datos que DXVA 2.0 para las operaciones de decodificación. Para el conjunto original de perfiles DXVA (para H.261, H.263 y MPEG-2), estas estructuras de datos se describen en la especificación [DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration).

Dentro de cada par de [**llamadas DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) y [**SubmitDecoderBuffer,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) puede llamar a [**GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) varias veces, pero solo una vez para cada tipo de búfer. Si usa el mismo tipo de búfer dos veces sin llamar a **SubmitDecoderBuffer,** sobrescribirá los datos del búfer.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de vídeo de Direct3D 11](direct3d-11-video-apis.md)
</dt> <dt>

[Aceleración de vídeo de DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
