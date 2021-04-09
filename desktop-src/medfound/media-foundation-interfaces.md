---
description: Interfaces de Media Foundation
ms.assetid: 3e367190-4c88-430e-adbf-9837e1bf0d2b
title: Interfaces de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12379dc83287b2a03ae0223a5a9a7d945d8fa77
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003323"
---
# <a name="media-foundation-interfaces"></a>Interfaces de Media Foundation

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Mfmediacapture/nn-mfmediacapture-iadvancedmediacapture"><strong>IAdvancedMediaCapture</strong></a><br/></td>
<td>Habilita la captura multimedia avanzada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediacapture/nn-mfmediacapture-iadvancedmediacaptureinitializationsettings"><strong>IAdvancedMediaCaptureInitializationSettings</strong></a><br/></td>
<td>Proporciona la configuración de inicialización para la captura multimedia avanzada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mfmediacapture/nn-mfmediacapture-iadvancedmediacapturesettings"><strong>IAdvancedMediaCaptureSettings</strong></a><br/></td>
<td>Proporciona la configuración de la captura multimedia avanzada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9"><strong>IDirect3DDeviceManager9</strong></a><br/></td>
<td>Habilita dos subprocesos para compartir el mismo dispositivo de Direct3D 9 y proporciona acceso a las características de aceleración de vídeo de DirectX (DXVA) del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice"><strong>IDirectXVideoAccelerationService</strong></a><br/></td>
<td>Proporciona servicios de aceleración de vídeo DirectX (DXVA) desde un dispositivo Direct3D.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder"><strong>IDirectXVideoDecoder</strong></a><br/></td>
<td>Representa un dispositivo de descodificador de vídeo de aceleración de vídeo de DirectX (DXVA).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice"><strong>IDirectXVideoDecoderService</strong></a><br/></td>
<td>Proporciona acceso a los servicios de descodificador de aceleración de vídeo de DirectX (DXVA).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a><br/></td>
<td>Establece el tipo de memoria de vídeo para las superficies de vídeo sin comprimir.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor"><strong>IDirectXVideoProcessor</strong></a><br/></td>
<td>Representa un dispositivo de procesador de vídeo de aceleración de vídeo de DirectX (DXVA).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice"><strong>IDirectXVideoProcessorService</strong></a><br/></td>
<td>Proporciona acceso a los servicios de procesamiento de vídeo de DirectX video Acceleration (DXVA).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a><br/></td>
<td>Establece el número de clavijas de entrada en el filtro de <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter"><strong>representador de vídeo mejorado</strong></a> (EVR) de DirectShow.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfigex"><strong>IEVRFilterConfigEx</strong></a><br/></td>
<td>Configura el filtro de <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter"><strong>representador de vídeo mejorado</strong></a> (EVR) de DirectShow.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin"><strong>IEVRTrustedVideoPlugin</strong></a><br/></td>
<td>Habilita un componente de complemento para el representador de vídeo mejorado (EVR) para que funcione con medios protegidos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a><br/></td>
<td>No se admite esta interfaz.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer"><strong>IMF2DBuffer</strong></a><br/></td>
<td>Representa un búfer que contiene una superficie bidimensional, como un fotograma de vídeo. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer2"><strong>IMF2DBuffer2</strong></a><br/></td>
<td>Representa un búfer que contiene una superficie bidimensional, como un fotograma de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate"><strong>IMFActivate</strong></a><br/></td>
<td>Permite a la aplicación diferir la creación de un objeto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo"><strong>IMFASFContentInfo</strong></a><br/></td>
<td>Proporciona métodos para trabajar con la sección de encabezado de los archivos que se ajustan a la especificación de Advanced Systems Format (ASF). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer"><strong>IMFASFIndexer</strong></a><br/></td>
<td>Proporciona métodos para trabajar con índices en archivos con formato de sistema (ASF).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer"><strong>IMFASFMultiplexer</strong></a><br/></td>
<td>Proporciona métodos para crear paquetes de datos de formato de sistema avanzado (ASF).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion"><strong>IMFASFMutualExclusion</strong></a><br/></td>
<td>Configura un objeto de exclusión mutua de Advanced Systems Format (ASF), que administra la información acerca de un grupo de secuencias en un perfil ASF que se excluyen mutuamente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile"><strong>IMFASFProfile</strong></a><br/></td>
<td>Administra un perfil de Advanced Systems Format (ASF).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter"><strong>IMFASFSplitter</strong></a><br/></td>
<td>Proporciona métodos para leer datos de un archivo de formato de sistema avanzado (ASF).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig"><strong>IMFASFStreamConfig</strong></a><br/></td>
<td>Configura los valores de una secuencia en un archivo ASF.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamprioritization"><strong>IMFASFStreamPrioritization</strong></a><br/></td>
<td>Sin implementar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector"><strong>IMFASFStreamSelector</strong></a><br/></td>
<td>Selecciona secuencias en un archivo de formato de sistema avanzado (ASF), basándose en la información de exclusión mutua del encabezado ASF.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback"><strong>IMFAsyncCallback</strong></a><br/></td>
<td>Interfaz de devolución de llamada para notificar a la aplicación cuando se completa un método asincrónico. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mfobjects/nn-mfobjects-imfasynccallbacklogging"><strong>IMFAsyncCallbackLogging</strong></a><br/></td>
<td>Proporciona información de registro sobre el objeto primario al que está asociada la devolución de llamada asincrónica.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a><br/></td>
<td>Proporciona información sobre el resultado de una operación asincrónica. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes"><strong>IMFAttributes</strong></a><br/></td>
<td>Proporciona una manera genérica de almacenar pares de clave y valor en un objeto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfaudiomediatype"><strong>IMFAudioMediaType</strong></a><br/></td>
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfaudiomediatype"><strong>IMFAudioMediaType</strong></a> ya no está disponible para su uso a partir de Windows 7.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy"><strong>IMFAudioPolicy</strong></a><br/></td>
<td>Configura la sesión de audio que está asociada con streaming audio renderer (SAR).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume"><strong>IMFAudioStreamVolume</strong></a><br/></td>
<td>Controla los niveles de volumen de canales de audio individuales.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfbufferlistnotify"><strong>IMFBufferListNotify</strong></a><br/></td>
<td>Habilita el objeto <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebufferlist"><strong>IMFSourceBufferList</strong></a> para notificar a sus clientes cambios importantes en el estado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream"><strong>IMFByteStream</strong></a><br/></td>
<td>Representa una secuencia de bytes de algún origen de datos, que puede ser un archivo local, un archivo de red o algún otro origen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering"><strong>IMFByteStreamBuffering</strong></a><br/></td>
<td>Controla el modo en que una secuencia de bytes almacena en búfer los datos de una red. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol"><strong>IMFByteStreamCacheControl</strong></a><br/></td>
<td>Controla el modo en que una secuencia de bytes de red transfiere datos a una memoria caché local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol2"><strong>IMFByteStreamCacheControl2</strong></a><br/></td>
<td>Controla el modo en que una secuencia de bytes de red transfiere datos a una memoria caché local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler"><strong>IMFByteStreamHandler</strong></a><br/></td>
<td>Crea un origen multimedia a partir de una secuencia de bytes. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestreamproxyclassfactory"><strong>IMFByteStreamProxyClassFactory</strong></a><br/></td>
<td>Crea un proxy en una secuencia de bytes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamtimeseek"><strong>IMFByteStreamTimeSeek</strong></a><br/></td>
<td>Busca una secuencia de bytes por posición de tiempo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine"><strong>IMFCaptureEngine</strong></a><br/></td>
<td>Controla uno o más dispositivos de captura.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineclassfactory"><strong>IMFCaptureEngineClassFactory</strong></a><br/></td>
<td>Crea una instancia del motor de captura.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineoneventcallback"><strong>IMFCaptureEngineOnEventCallback</strong></a><br/></td>
<td>Interfaz de devolución de llamada para recibir eventos del motor de captura.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback"><strong>IMFCaptureEngineOnSampleCallback</strong></a><br/></td>
<td>Interfaz de devolución de llamada para recibir datos del motor de captura.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback2"><strong>IMFCaptureEngineOnSampleCallback2</strong></a><br/></td>
<td>Extensiones para la interfaz de devolución de llamada <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback"><strong>IMFCaptureEngineOnSampleCallback</strong></a> que se usa para recibir datos del motor de captura.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink"><strong>IMFCapturePhotoSink</strong></a><br/></td>
<td>Controla el receptor de fotos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink"><strong>IMFCapturePreviewSink</strong></a><br/></td>
<td>Controla el receptor de vista previa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink"><strong>IMFCaptureRecordSink</strong></a><br/></td>
<td>Controla el receptor de la grabación.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink"><strong>IMFCaptureSink</strong></a><br/></td>
<td>Controla un receptor de captura, que es un objeto que recibe una o más secuencias de un dispositivo de captura.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink2"><strong>IMFCaptureSink2</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink"><strong>IMFCaptureSink</strong></a> para proporcionar la funcionalidad para establecer de forma dinámica el tipo de medio de salida del receptor de registros o del receptor de vista previa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource"><strong>IMFCaptureSource</strong></a><br/></td>
<td>Controla el objeto de origen de la captura. El origen de captura administra los dispositivos de captura de audio y vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify"><strong>IMFCdmSuspendNotify</strong></a><br/></td>
<td>Se usa para permitir que el cliente notifique al módulo de descifrado de contenido (CDM) cuando los recursos globales deben pasar a un estado coherente antes de la suspensión. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock"><strong>IMFClock</strong></a><br/></td>
<td>Proporciona información de tiempo de un reloj en Microsoft Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockconsumer"><strong>IMFClockConsumer</strong></a><br/></td>
<td>Implementado por una aplicación para obtener acceso a <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock"><strong>IMFPresentationClock</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink"><strong>IMFClockStateSink</strong></a><br/></td>
<td>Recibe notificaciones de cambio de estado del reloj de presentación. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection"><strong>IMFCollection</strong></a><br/></td>
<td>Representa una colección genérica de punteros <strong>IUnknown</strong> . <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentdecryptorcontext"><strong>IMFContentDecryptorContext</strong></a><br/></td>
<td>Permite a un descifrador administrar las claves de hardware y descifrar los ejemplos de hardware.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler"><strong>IMFContentEnabler</strong></a><br/></td>
<td>Implementa un paso que se debe realizar para que el usuario tenga acceso al contenido multimedia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectiondevice"><strong>IMFContentProtectionDevice</strong></a><br/></td>
<td>Permite que un descifrador se comunique con el procesador de seguridad que implementa el descifrado de hardware para un sistema de protección. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager"><strong>IMFContentProtectionManager</strong></a><br/></td>
<td>Habilita la reproducción de contenido protegido proporcionando a la aplicación un puntero a un objeto habilitador de contenido.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfdesiredsample"><strong>IMFDesiredSample</strong></a><br/></td>
<td>Permite al presentador de vídeo mejorado (EVR) solicitar un fotograma específico del mezclador de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmp2dlna/nn-mfmp2dlna-imfdlnasinkinit"><strong>IMFDLNASinkInit</strong></a><br/></td>
<td>Inicializa el receptor de medios de la Alianza de redes digitales (DLNA). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfdrmnethelper"><strong>IMFDRMNetHelper</strong></a><br/></td>
<td>Configura Windows Media Digital Rights Management (DRM) para dispositivos de red en un receptor de red.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgibuffer"><strong>IMFDXGIBuffer</strong></a><br/></td>
<td>Representa un búfer que contiene una superficie de Microsoft DirectX Graphics Infrastructure (DXGI).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager"><strong>IMFDXGIDeviceManager</strong></a><br/></td>
<td>Habilita dos subprocesos para compartir el mismo dispositivo de Microsoft Direct3D 11.<br/></td>
</tr>
<tr class="odd">
<td><a href="imfdxgidevicemanagersource.md"><strong>IMFDXGIDeviceManagerSource</strong></a><br/></td>
<td>Proporciona funcionalidad para obtener el <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager"><strong>IMFDXGIDeviceManager</strong></a> del receptor de representación de vídeo Media Foundation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock"><strong>IMFFieldOfUseMFTUnlock</strong></a><br/></td>
<td>Permite que una aplicación use una transformación de Media Foundation (MFT) que tenga restricciones en su uso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink"><strong>IMFFinalizableMediaSink</strong></a><br/></td>
<td>Opcionalmente, compatible con los receptores de medios para realizar las tareas necesarias antes del cierre.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a><br/></td>
<td>Consulta un objeto para una interfaz de servicio especificada. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest"><strong>IMFHttpDownloadRequest</strong></a><br/></td>
<td>Las aplicaciones implementan esta interfaz para invalidar la implementación predeterminada de los protocolos HTTP y HTTPS usados por Microsoft Media Foundation. Las aplicaciones proporcionan la interfaz <strong>IMFHttpDownloadRequest</strong> para Media Foundation a través del método <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsession-createrequest"><strong>CreateRequest</strong></a> en la interfaz <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession"><strong>IMFHttpDownloadSession</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession"><strong>IMFHttpDownloadSession</strong></a><br/></td>
<td>Las aplicaciones implementan esta interfaz para invalidar la implementación predeterminada de los protocolos HTTP y HTTPS usados por Microsoft Media Foundation. Las aplicaciones proporcionan la interfaz <strong>IMFHttpDownloadSession</strong> para Media Foundation a través del método <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession"><strong>CreateHttpDownloadSession</strong></a> en la interfaz <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsessionprovider"><strong>IMFHttpDownloadSessionProvider</strong></a> . Microsoft Media Foundation usa esta interfaz para realizar una descarga de "streaming" o "progresiva" de un recurso identificado por una dirección URL HTTP o HTTPS. Se pueden enviar varias solicitudes HTTP para descargar el recurso. La interfaz <strong>IMFHttpDownloadSession</strong> se utiliza para crear estas solicitudes HTTP individuales.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsessionprovider"><strong>IMFHttpDownloadSessionProvider</strong></a><br/></td>
<td>Las aplicaciones implementan esta interfaz con el fin de proporcionar una implementación personalizada de descarga HTTP o HTTPS. Use la interfaz <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver"><strong>IMFSourceResolver</strong></a> para registrar el proveedor. Para obtener más información, vea <a href="using-the-source-resolver.md">usar el solucionador de origen</a>. Una vez registrado, el Microsoft Media Foundation invocará el método <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession"><strong>CreateHttpDownloadSession</strong></a> de la implementación del proveedor para abrir las direcciones URL http o https en lugar de usar la implementación predeterminada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengine"><strong>IMFImageSharingEngine</strong></a><br/></td>
<td>Habilita el uso compartido de imágenes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengineclassfactory"><strong>IMFImageSharingEngineClassFactory</strong></a><br/></td>
<td>Crea una instancia de <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengine"><strong>IMFImageSharingEngine</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfinputtrustauthority"><strong>IMFInputTrustAuthority</strong></a><br/></td>
<td>Permite que otros componentes de la ruta de acceso a medios protegidos (PMP) usen el sistema de protección de entrada proporcionado por una autoridad de confianza de entrada (ITA).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imflocalmftregistration"><strong>IMFLocalMFTRegistration</strong></a><br/></td>
<td>Registra Media Foundation transformaciones (MFTs) en el proceso del llamador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer"><strong>IMFMediaBuffer</strong></a><br/></td>
<td>Representa un bloque de memoria que contiene datos multimedia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMFMediaEngine</strong></a><br/></td>
<td>Permite que una aplicación reproduzca archivos de audio o vídeo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory"><strong>IMFMediaEngineClassFactory</strong></a><br/></td>
<td>Crea una instancia del motor multimedia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory2"><strong>IMFMediaEngineClassFactory2</strong></a><br/></td>
<td>Crea una instancia del objeto <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys"><strong>IMFMediaKeys</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex"><strong>IMFMediaEngineClassFactoryEx</strong></a><br/></td>
<td>Extensión de la interfaz <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory"><strong>IMFMediaEngineClassFactory</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme"><strong>IMFMediaEngineEME</strong></a><br/></td>
<td>Implementado por el motor multimedia para agregar métodos de extensiones de medios cifrados.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex"><strong>IMFMediaEngineEx</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMFMediaEngine</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension"><strong>IMFMediaEngineExtension</strong></a><br/></td>
<td>Permite a una aplicación cargar recursos multimedia en el motor multimedia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify"><strong>IMFMediaEngineNeedKeyNotify</strong></a><br/></td>
<td>Representa una devolución de llamada al motor multimedia para notificar los datos de la solicitud de clave.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify"><strong>IMFMediaEngineNotify</strong></a><br/></td>
<td>Interfaz de devolución de llamada para la interfaz <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMFMediaEngine</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineopminfo"><strong>IMFMediaEngineOPMInfo</strong></a><br/></td>
<td>Proporciona métodos para obtener información sobre el <a href="output-protection-manager.md">Administrador de protección de salida</a> (OPM).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineprotectedcontent"><strong>IMFMediaEngineProtectedContent</strong></a><br/></td>
<td>Permite al motor multimedia reproducir contenido de vídeo protegido.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements"><strong>IMFMediaEngineSrcElements</strong></a><br/></td>
<td>Proporciona al motor multimedia una lista de recursos multimedia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelementsex"><strong>IMFMediaEngineSrcElementsEx</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements"><strong>IMFMediaEngineSrcElements</strong></a> para proporcionar funcionalidades adicionales.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesupportssourcetransfer"><strong>IMFMediaEngineSupportsSourceTransfer</strong></a><br/></td>
<td>Permite que el origen de medios se transfiera entre el motor multimedia y el motor de uso compartido para reproducirse en.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginewebsupport"><strong>IMFMediaEngineWebSupport</strong></a><br/></td>
<td>Habilita la reproducción de audio Web.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaerror"><strong>IMFMediaError</strong></a><br/></td>
<td>Proporciona el estado de error actual para el motor multimedia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent"><strong>IMFMediaEvent</strong></a><br/></td>
<td>Representa un evento generado por un objeto Media Foundation. Utilice esta interfaz para obtener información sobre el evento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator"><strong>IMFMediaEventGenerator</strong></a><br/></td>
<td>Recupera los eventos de cualquier Media Foundation objeto que genera eventos. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue"><strong>IMFMediaEventQueue</strong></a><br/></td>
<td>Proporciona una cola de eventos para las aplicaciones que necesitan implementar la interfaz <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator"><strong>IMFMediaEventGenerator</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys"><strong>IMFMediaKeys</strong></a><br/></td>
<td>Representa las claves multimedia que se usan para descifrar los datos multimedia mediante un sistema de claves Digital Rights Management (DRM). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession"><strong>IMFMediaKeySession</strong></a><br/></td>
<td>Representa una sesión con el sistema de claves Digital Rights Management (DRM).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysessionnotify"><strong>IMFMediaKeySessionNotify</strong></a><br/></td>
<td>Proporciona un mecanismo para notificar a la aplicación información relacionada con la sesión de clave multimedia. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession"><strong>IMFMediaSession</strong></a><br/></td>
<td>Proporciona controles de reproducción para contenido protegido y no protegido.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengine"><strong>IMFMediaSharingEngine</strong></a><br/></td>
<td>Habilita el uso compartido de multimedia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengineclassfactory"><strong>IMFMediaSharingEngineClassFactory</strong></a><br/></td>
<td>Crea una instancia de <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengine"><strong>IMFMediaSharingEngine</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink"><strong>IMFMediaSink</strong></a><br/></td>
<td>Implementado por objetos de receptor de medios.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll"><strong>IMFMediaSinkPreroll</strong></a><br/></td>
<td>Permite que un receptor de medios reciba muestras antes de que se inicie el reloj de la presentación.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>IMFMediaSource</strong></a><br/></td>
<td>Implementado por objetos de origen multimedia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex"><strong>IMFMediaSourceEx</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>IMFMediaSource</strong></a> para proporcionar funcionalidades adicionales para un origen de multimedia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>IMFMediaSourceExtension</strong></a><br/></td>
<td>Proporciona funcionalidad para la extensión de origen de medios (MSE).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextensionnotify"><strong>IMFMediaSourceExtensionNotify</strong></a><br/></td>
<td>Proporciona la funcionalidad para generar eventos asociados a <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>IMFMediaSourceExtension</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider"><strong>IMFMediaSourcePresentationProvider</strong></a><br/></td>
<td>Proporciona notificaciones al origen del secuenciador.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider"><strong>IMFMediaSourceTopologyProvider</strong></a><br/></td>
<td>Permite a una aplicación obtener una topología del origen del secuenciador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediastream"><strong>IMFMediaStream</strong></a><br/></td>
<td>Representa una secuencia en un origen de multimedia. <br/></td>
</tr>
<tr class="odd">
<td><a href="imfmediastreamsourcesamplerequest.md"><strong>IMFMediaStreamSourceSampleRequest</strong></a><br/></td>
<td>Representa una solicitud para un ejemplo de un MediaStreamSource. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange"><strong>IMFMediaTimeRange</strong></a><br/></td>
<td>Representa una lista de intervalos de tiempo, donde cada intervalo se define mediante una hora de inicio y de finalización.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype"><strong>IMFMediaType</strong></a><br/></td>
<td>Representa una descripción de un formato multimedia. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler"><strong>IMFMediaTypeHandler</strong></a><br/></td>
<td>Obtiene y establece los tipos de medios de un objeto, como un origen multimedia o un receptor multimedia. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata"><strong>IMFMetadata</strong></a><br/></td>
<td>Administra los metadatos de un objeto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a><br/></td>
<td>Obtiene los metadatos de un origen de medios u otro objeto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager"><strong>IMFMuxStreamAttributesManager</strong></a><br/></td>
<td>Proporciona acceso al <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes"><strong>IMFAttributes</strong></a> de los subflujos de un origen de medios multiplexado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager"><strong>IMFMuxStreamSampleManager</strong></a><br/></td>
<td>Proporciona la capacidad de recuperar objetos <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample"><strong>IMFSample</strong></a> para subflujos individuales dentro de la salida de un origen de medios multiplexado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager"><strong>IMFMuxStreamMediaTypeManager</strong></a><br/></td>
<td>Habilita la administración de configuraciones de secuencia para un origen de medios multiplexado. Una configuración de flujo define un conjunto de subsecuencias que se pueden incluir en la salida multiplexada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential"><strong>IMFNetCredential</strong></a><br/></td>
<td>Establece y recupera información de nombre de usuario y contraseña para fines de autenticación. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache"><strong>IMFNetCredentialCache</strong></a><br/></td>
<td>Obtiene las credenciales de la memoria caché de credenciales.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager"><strong>IMFNetCredentialManager</strong></a><br/></td>
<td>Implementado por aplicaciones para proporcionar las credenciales de usuario para un origen de red.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcrossoriginsupport"><strong>IMFNetCrossOriginSupport</strong></a><br/></td>
<td>Implementado por clientes que desean aplicar una directiva de origen cruzado para las descargas de medios HTML5. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator"><strong>IMFNetProxyLocator</strong></a><br/></td>
<td>Determina el proxy que se va a usar al conectarse a un servidor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory"><strong>IMFNetProxyLocatorFactory</strong></a><br/></td>
<td>Crea un objeto de localizador proxy, que determina el proxy que se va a usar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter"><strong>IMFNetResourceFilter</strong></a><br/></td>
<td>Notifica a la aplicación cuando una secuencia de bytes solicita una dirección URL y permite que la aplicación bloquee la redirección de direcciones URL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig"><strong>IMFNetSchemeHandlerConfig</strong></a><br/></td>
<td>Configura un complemento de esquema de red. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfobjectreferencestream"><strong>IMFObjectReferenceStream</strong></a><br/></td>
<td>Calcula las referencias de un puntero de interfaz a y desde una secuencia. <br/> Los objetos de secuencia que admiten <strong>IStream</strong> pueden exponer esta interfaz para proporcionar serialización personalizada para punteros de interfaz.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy"><strong>IMFOutputPolicy</strong></a><br/></td>
<td>Encapsula una directiva de uso de una autoridad de confianza de entrada (ITA).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema"><strong>IMFOutputSchema</strong></a><br/></td>
<td>Encapsula información sobre un sistema de protección de salida y sus datos de configuración correspondientes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority"><strong>IMFOutputTrustAuthority</strong></a><br/></td>
<td>Encapsula la funcionalidad de uno o más sistemas de protección de salida que admite una salida de confianza.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol"><strong>IMFPluginControl</strong></a><br/></td>
<td>Controla cómo se enumeran las transformaciones y los orígenes multimedia en Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol2"><strong>IMFPluginControl2</strong></a><br/></td>
<td>Controla cómo se enumeran las transformaciones y los orígenes multimedia en Media Foundation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem"><strong>IMFPMediaItem</strong></a><br/></td>
<td>Representa un elemento multimedia. (En desuso).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer"><strong>IMFPMediaPlayer</strong></a><br/></td>
<td>Contiene métodos para reproducir archivos multimedia. (En desuso).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback"><strong>IMFPMediaPlayerCallback</strong></a><br/></td>
<td>Interfaz de devolución de llamada para la interfaz <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer"><strong>IMFPMediaPlayer</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient"><strong>IMFPMPClient</strong></a><br/></td>
<td>Permite a un origen de medios recibir un puntero a la interfaz <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphost"><strong>IMFPMPHost</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpclientapp"><strong>IMFPMPClientApp</strong></a><br/></td>
<td>Proporciona un mecanismo para que un origen multimedia implemente la funcionalidad de protección de contenido en las aplicaciones de la tienda Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphost"><strong>IMFPMPHost</strong></a><br/></td>
<td>Habilita un origen multimedia en el proceso de la aplicación para crear objetos en el proceso de la ruta de acceso a medios protegidos (PMP).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphostapp"><strong>IMFPMPHostApp</strong></a><br/></td>
<td>Permite a un origen de medios crear un objeto de <a href="/windows/desktop/WinRT/reference">Windows Runtime</a> en el proceso de la <a href="protected-media-path.md">ruta de acceso a medios protegidos</a> (PMP). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver"><strong>IMFPMPServer</strong></a><br/></td>
<td>Permite que dos instancias de la <a href="media-session.md">sesión multimedia</a> compartan el mismo proceso de la ruta de acceso a medios protegidos (PMP). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock"><strong>IMFPresentationClock</strong></a><br/></td>
<td>Representa un reloj de presentación, que se usa para programar Cuándo se representan los ejemplos y sincronizar varias secuencias.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor"><strong>IMFPresentationDescriptor</strong></a><br/></td>
<td>Describe los detalles de una presentación. Una <em>presentación</em> es un conjunto de flujos multimedia relacionados que comparten un tiempo de presentación común. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource"><strong>IMFPresentationTimeSource</strong></a><br/></td>
<td>Proporciona las horas de reloj para el reloj de presentación. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfprotectedenvironmentaccess"><strong>IMFProtectedEnvironmentAccess</strong></a><br/></td>
<td>Proporciona un método que permite que los sistemas de protección de contenido realicen un protocolo de enlace con el entorno protegido. Esto es necesario porque las API de <strong>CreateFile</strong> y <strong>DeviceIoControl</strong> no están disponibles para las aplicaciones de la tienda Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a><br/></td>
<td>Permite que el administrador de calidad ajuste la calidad de audio o de vídeo de un componente en la canalización.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a><br/></td>
<td>Permite que un objeto de canalización ajuste su propia calidad de audio o vídeo, en respuesta a los mensajes de calidad.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadviselimits"><strong>IMFQualityAdviseLimits</strong></a><br/></td>
<td>Consulta un objeto para el número de <em>modos de calidad</em> que admite.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager"><strong>IMFQualityManager</strong></a><br/></td>
<td>Ajusta la calidad de la reproducción. Esta interfaz la expone el administrador de calidad. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a><br/></td>
<td>Obtiene o establece la velocidad de reproducción. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a><br/></td>
<td>Consulta el intervalo de velocidades de reproducción que se admiten, incluida la reproducción inversa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfreadwriteclassfactory"><strong>IMFReadWriteClassFactory</strong></a><br/></td>
<td>Crea una instancia del escritor de receptor o del lector de origen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a><br/></td>
<td>Notifica a un objeto de canalización que se registre con el servicio de programador de clases multimedia (MMCSS).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex"><strong>IMFRealTimeClientEx</strong></a><br/></td>
<td>Notifica a un objeto de canalización que se registre con el servicio de programador de clases multimedia (MMCSS). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfremoteasynccallback"><strong>IMFRemoteAsyncCallback</strong></a><br/></td>
<td>Lo utiliza el archivo DLL de Media Foundation proxy/stub para calcular las referencias de ciertas llamadas de método asincrónicas a través de los límites del proceso.<br/> Las aplicaciones no usan ni implementan esta interfaz.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfremotedesktopplugin"><strong>IMFRemoteDesktopPlugin</strong></a><br/></td>
<td>Modifica una topología para su uso en un entorno de Terminal Services. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy"><strong>IMFRemoteProxy</strong></a><br/></td>
<td>Expuesto por objetos que actúan como proxy para un objeto remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle"><strong>IMFSAMIStyle</strong></a><br/></td>
<td>Establece y recupera los estilos de intercambio de medios accesibles (SAMI) sincronizados en el <a href="sami-media-source.md">origen de medios Sami</a>. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample"><strong>IMFSample</strong></a><br/></td>
<td>Representa un ejemplo multimedia, que es un objeto contenedor para los datos multimedia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback"><strong>IMFSampleGrabberSinkCallback</strong></a><br/></td>
<td>Interfaz de devolución de llamada para obtener los datos multimedia del receptor de captura de muestras. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback2"><strong>IMFSampleGrabberSinkCallback2</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback"><strong>IMFSampleGrabberSinkCallback</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsampleoutputstream"><strong>IMFSampleOutputStream</strong></a><br/></td>
<td>Escribe ejemplos multimedia en una secuencia de bytes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsampleprotection"><strong>IMFSampleProtection</strong></a><br/></td>
<td>Proporciona cifrado para los datos multimedia dentro de la ruta de acceso a medios protegidos (PMP). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsavejob"><strong>IMFSaveJob</strong></a><br/></td>
<td>Conserva los datos multimedia de una secuencia de bytes de origen en una secuencia de bytes proporcionada por la aplicación.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler"><strong>IMFSchemeHandler</strong></a><br/></td>
<td>Crea un origen de medios o un flujo de bytes a partir de una dirección URL. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsecurechannel"><strong>IMFSecureChannel</strong></a><br/></td>
<td>Establece un canal seguro unidireccional entre dos objetos. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfseekinfo"><strong>IMFSeekInfo</strong></a><br/></td>
<td>Para una posición de búsqueda determinada, obtiene los dos fotogramas clave más cercanos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreport"><strong>IMFSensorActivitiesReport</strong></a><br/></td>
<td>Proporciona acceso a los objetos <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport"><strong>IMFSensorActivityReport</strong></a> que describen la actividad actual de un sensor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreportcallback"><strong>IMFSensorActivitiesReportCallback</strong></a><br/></td>
<td>Interfaz implementada por el cliente para recibir devoluciones de llamada cuando los informes de actividad del sensor están disponibles.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitymonitor"><strong>IMFSensorActivityMonitor</strong></a><br/></td>
<td>Proporciona métodos para controlar un monitor de actividad de sensor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport"><strong>IMFSensorActivityReport</strong></a><br/></td>
<td>Representa un informe de actividad para un sensor.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice"><strong>IMFSensorDevice</strong></a><br/></td>
<td>Representa un dispositivo de sensor que puede pertenecer a un grupo de sensores, que se representa mediante la interfaz <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup"><strong>IMFSensorGroup</strong></a> . El término &quot; dispositivo &quot; en este contexto podría hacer referencia a un dispositivo físico, a un origen multimedia personalizado o a un proveedor de fotogramas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup"><strong>IMFSensorGroup</strong></a><br/></td>
<td>Representa un grupo de dispositivos de sensor desde el que se puede crear un <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>IMFMediaSource</strong></a> . El término &quot; dispositivo &quot; en este contexto podría hacer referencia a un dispositivo físico, a un origen multimedia personalizado o a un proveedor de fotogramas. Es posible que un grupo de sensores contenga varios dispositivos de sensor o que solo contenga un único dispositivo, pero sigue siendo un grupo de sensores.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity"><strong>IMFSensorProcessActivity</strong></a><br/></td>
<td>Representa la actividad de un proceso asociado a un sensor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofilecollection"><strong>IMFSensorProfileCollection</strong></a><br/></td>
<td>Contiene una colección de objetos de Perfil de sensor de Media Foundation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofile"><strong>IMFSensorProfile</strong></a><br/></td>
<td>Describe un perfil de sensor de Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorstream"><strong>IMFSensorStream</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensortransformfactory"><strong>IMFSensorTransformFactory</strong></a><br/></td>
<td>La interfaz implementada por el sensor se transforma para permitir que la canalización multimedia consulte los requisitos de la transformación del sensor y para crear una instancia en tiempo de ejecución de la transformación del sensor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource"><strong>IMFSequencerSource</strong></a><br/></td>
<td>Implementado por el <a href="sequencer-source.md">origen del secuenciador</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfsharingengineclassfactory"><strong>IMFSharingEngineClassFactory</strong></a><br/></td>
<td>Crea una instancia del motor de uso compartido de multimedia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfshutdown"><strong>IMFShutdown</strong></a><br/></td>
<td>Expuesto por algunos objetos Media Foundation que se deben apagar explícitamente. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsignedlibrary"><strong>IMFSignedLibrary</strong></a><br/></td>
<td>Proporciona un método que permite a los sistemas de protección de contenido obtener la dirección del procedimiento de una función de la biblioteca firmada. Este método proporciona la misma funcionalidad que <strong>GetProcAddress</strong> , que no está disponible para las aplicaciones de la tienda Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume"><strong>IMFSimpleAudioVolume</strong></a><br/></td>
<td>Controla el nivel de volumen maestro de la sesión de audio asociada al representador de audio de streaming (SAR) y el origen de captura de audio.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter"><strong>IMFSinkWriter</strong></a><br/></td>
<td>Implementado por el objeto de escritor de receptor de Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback"><strong>IMFSinkWriterCallback</strong></a><br/></td>
<td>Interfaz de devolución de llamada para el escritor de Media Foundation receptor. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback2"><strong>IMFSinkWriterCallback2</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback"><strong>IMFSinkWriterCallback</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterencoderconfig"><strong>IMFSinkWriterEncoderConfig</strong></a><br/></td>
<td>Proporciona funcionalidad adicional en el escritor del receptor para cambiar de forma dinámica el tipo de medio y la configuración del codificador. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex"><strong>IMFSinkWriterEx</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter"><strong>IMFSinkWriter</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMFSourceBuffer</strong></a><br/></td>
<td>Representa un búfer que contiene datos multimedia para un <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>IMFMediaSourceExtension</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebufferlist"><strong>IMFSourceBufferList</strong></a><br/></td>
<td>Representa una colección de objetos <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMFSourceBuffer</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify"><strong>IMFSourceBufferNotify</strong></a><br/></td>
<td>Proporciona la funcionalidad para generar eventos asociados a <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMFSourceBuffer</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor"><strong>IMFSourceOpenMonitor</strong></a><br/></td>
<td>Interfaz de devolución de llamada para recibir notificaciones de un origen de red en el progreso de una operación de apertura asincrónica.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader"><strong>IMFSourceReader</strong></a><br/></td>
<td>Implementado por el objeto lector de origen de Media Foundation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback"><strong>IMFSourceReaderCallback</strong></a><br/></td>
<td>Interfaz de devolución de llamada para el lector de origen de Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback2"><strong>IMFSourceReaderCallback2</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback"><strong>IMFSourceReaderCallback</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex"><strong>IMFSourceReaderEx</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader"><strong>IMFSourceReader</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver"><strong>IMFSourceResolver</strong></a><br/></td>
<td>Crea un origen multimedia a partir de una dirección URL o de una secuencia de bytes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer"><strong>IMFSpatialAudioObjectBuffer</strong></a><br/></td>
<td>Representa una sección de datos de audio con metadatos de posición y representación asociados. Los objetos de audio espacial se almacenan en instancias de <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMFSpatialAudioSample</strong></a> y permiten pasar información de audio espacial entre Media Foundation componentes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMFSpatialAudioSample</strong></a><br/></td>
<td>Representa un ejemplo multimedia con información de sonido espacial. Cada <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMFSpatialAudioSample</strong></a> contiene uno o varios objetos <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer"><strong>IMFSpatialAudioObjectBuffer</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager"><strong>IMFSSLCertificateManager</strong></a><br/></td>
<td>Implementado por un cliente y llamado por Media Foundation para obtener el certificado de Capa de sockets seguros de cliente (SSL) solicitado por el servidor. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor"><strong>IMFStreamDescriptor</strong></a><br/></td>
<td>Obtiene información acerca de una secuencia en un origen de multimedia. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamingsinkconfig"><strong>IMFStreamingSinkConfig</strong></a><br/></td>
<td>Pasa información de configuración a los receptores de medios que se usan para transmitir por secuencias el contenido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink"><strong>IMFStreamSink</strong></a><br/></td>
<td>Representa una secuencia en un objeto de receptor de multimedia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsystemid"><strong>IMFSystemId</strong></a><br/></td>
<td>Proporciona un método que retireves los datos de identificador del sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate"><strong>IMFTimecodeTranslate</strong></a><br/></td>
<td>Convierte entre la sociedad de códigos de tiempo de imágenes de movimiento y de ingeniería de televisión (SMPTE) y las unidades de tiempo de 100-nanosegundos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext"><strong>IMFTimedText</strong></a><br/></td>
<td>Un objeto de texto con hora representa un componente de texto con tiempo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextbinary"><strong>IMFTimedTextBinary</strong></a><br/></td>
<td>Representa el contenido de datos de un objeto de texto con hora.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextcue"><strong>IMFTimedTextCue</strong></a><br/></td>
<td>Representa el objeto de la señal de texto con hora. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextformattedtext"><strong>IMFTimedTextFormattedText</strong></a><br/></td>
<td>Representa un bloque de texto con hora con formato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextnotify"><strong>IMFTimedTextNotify</strong></a><br/></td>
<td>Interfaz que define las devoluciones de llamada para Media Foundation notificaciones de texto con tiempo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion"><strong>IMFTimedTextRegion</strong></a><br/></td>
<td>Representa la región de presentación de un objeto de texto con hora.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle"><strong>IMFTimedTextStyle</strong></a><br/></td>
<td>Representa el estilo del texto con hora.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack"><strong>IMFTimedTextTrack</strong></a><br/></td>
<td>Representa una pista de texto con hora.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist"><strong>IMFTimedTextTrackList</strong></a><br/></td>
<td>Representa una lista de pistas de texto con tiempo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftimer"><strong>IMFTimer</strong></a><br/></td>
<td>Proporciona un temporizador que invoca una devolución de llamada en un momento especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopoloader"><strong>IMFTopoLoader</strong></a><br/></td>
<td>Convierte una topología parcial en una topología completa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology"><strong>IMFTopology</strong></a><br/></td>
<td>Representa una topología. Una <em>topología</em> describe una colección de orígenes de medios, receptores y transformaciones que están conectados en un determinado orden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode"><strong>IMFTopologyNode</strong></a><br/></td>
<td>Representa un nodo en una topología.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor"><strong>IMFTopologyNodeAttributeEditor</strong></a><br/></td>
<td>Actualiza los atributos de uno o más nodos en la topología actual de la sesión multimedia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookup"><strong>IMFTopologyServiceLookup</strong></a><br/></td>
<td>Habilita un mezclador de vídeo personalizado o un presentador de vídeo para obtener punteros de interfaz del <a href="enhanced-video-renderer.md">representador de vídeo mejorado</a> (EVR).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient"><strong>IMFTopologyServiceLookupClient</strong></a><br/></td>
<td>Inicializa un mezclador o presentador de vídeo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrackedsample"><strong>IMFTrackedSample</strong></a><br/></td>
<td>Realiza un seguimiento de los recuentos de referencias en un ejemplo de vídeo multimedia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile"><strong>IMFTranscodeProfile</strong></a><br/></td>
<td>Implementado por el objeto de Perfil de Transcode.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodesinkinfoprovider"><strong>IMFTranscodeSinkInfoProvider</strong></a><br/></td>
<td>Implementado por el objeto de activación del receptor de transcodificación.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a><br/></td>
<td>Implementado por todas las <a href="media-foundation-transforms.md">transformaciones de Media Foundation</a> (MFTs).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput"><strong>IMFTrustedInput</strong></a><br/></td>
<td>Implementado por componentes que proporcionan autoridades de confianza de entrada (ITAs). Esta interfaz se usa para obtener la ITA para cada flujo del componente. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput"><strong>IMFTrustedOutput</strong></a><br/></td>
<td>Implementado por componentes que proporcionan las entidades de confianza de salida (OTAs).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideodeviceid"><strong>IMFVideoDeviceID</strong></a><br/></td>
<td>Devuelve el identificador de dispositivo admitido por un componente de representador de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol"><strong>IMFVideoDisplayControl</strong></a><br/></td>
<td>Controla cómo se muestra el vídeo en el <a href="enhanced-video-renderer.md">representador de vídeo mejorado</a> (EVR).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype"><strong>IMFVideoMediaType</strong></a><br/></td>
<td>Representa una descripción de un formato de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap"><strong>IMFVideoMixerBitmap</strong></a><br/></td>
<td>Alpha: combina una imagen de mapa de bits estática con el vídeo mostrado por el <a href="enhanced-video-renderer.md">representador de vídeo mejorado</a> (EVR).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol"><strong>IMFVideoMixerControl</strong></a><br/></td>
<td>Controla la forma en que el <a href="enhanced-video-renderer.md">representador de vídeo mejorado</a> (EVR) combina subsecuencias de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2"><strong>IMFVideoMixerControl2</strong></a><br/></td>
<td>Controla las preferencias del desentrelazado de vídeo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a><br/></td>
<td>Asigna una posición en una secuencia de vídeo de entrada a la posición correspondiente en una secuencia de vídeo de salida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideopresenter"><strong>IMFVideoPresenter</strong></a><br/></td>
<td>Representa un presentador de vídeo. Un <em>presentador de vídeo</em> es un objeto que recibe fotogramas de vídeo, normalmente de un mezclador de vídeo, y los presenta de alguna manera, normalmente mediante su representación en la pantalla.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor"><strong>IMFVideoProcessor</strong></a><br/></td>
<td>Controla el procesamiento de vídeo en el <a href="enhanced-video-renderer.md">representador de vídeo mejorado</a> (EVR).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol"><strong>IMFVideoProcessorControl</strong></a><br/></td>
<td>Configura la MFT del <a href="video-processor-mft.md"><strong>procesador de vídeo</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol2"><strong>IMFVideoProcessorControl2</strong></a><br/></td>
<td>Configura la MFT del <a href="video-processor-mft.md"><strong>procesador de vídeo</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a><br/></td>
<td>Establece un nuevo mezclador o presentador para el <a href="enhanced-video-renderer.md">representador de vídeo mejorado</a> (EVR).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator"><strong>IMFVideoSampleAllocator</strong></a><br/></td>
<td>Asigna ejemplos de vídeo para un receptor de multimedia de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMFVideoSampleAllocatorCallback</strong></a><br/></td>
<td>Permite que una aplicación realice el seguimiento de ejemplos de vídeo asignados por el representador de vídeo mejorado (EVR).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex"><strong>IMFVideoSampleAllocatorEx</strong></a><br/></td>
<td>Asigna muestras de vídeo que contienen superficies de textura de Direct3D 11.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotify"><strong>IMFVideoSampleAllocatorNotify</strong></a><br/></td>
<td>Devolución de llamada para la interfaz <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMFVideoSampleAllocatorCallback</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotifyex"><strong>IMFVideoSampleAllocatorNotifyEx</strong></a><br/></td>
<td>Devolución de llamada para la interfaz <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMFVideoSampleAllocatorCallback</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices"><strong>IMFWorkQueueServices</strong></a><br/></td>
<td>Controla las colas de trabajo creadas por la <a href="media-session.md">sesión multimedia</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex"><strong>IMFWorkQueueServicesEx</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices"><strong>IMFWorkQueueServices</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytocontrol"><strong>IPlayToControl</strong></a><br/></td>
<td>Habilita el objeto <strong>PlayToConnection</strong> para conectarse a un elemento multimedia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytocontrolwithcapabilities"><strong>IPlayToControlWithCapabilities</strong></a><br/></td>
<td>Proporciona funcionalidad para que los <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytosourceclassfactory"><strong>IPlayToSource</strong></a> determinen las capacidades del contenido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytosourceclassfactory"><strong>IPlayToSourceClassFactory</strong></a><br/></td>
<td>Crea una instancia del objeto <a href="/uwp/api/Windows.Media.PlayTo.PlayToSource"><strong>PlayToSource</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket"><strong>IWMCodecLeakyBucket</strong></a><br/></td>
<td>Configura los &quot; &quot; parámetros de depósito de fugas en un codificador de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecoutputtimestamp"><strong>IWMCodecOutputTimestamp</strong></a><br/></td>
<td>Obtiene la marca de tiempo del siguiente fotograma de vídeo que se va a descodificar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata"><strong>IWMCodecPrivateData</strong></a><br/></td>
<td>Obtiene los datos del códec privado que se deben anexar al tipo de medio de salida. Estos datos de códec son necesarios para descodificar correctamente el contenido de Windows Media Video.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprops"><strong>IWMCodecProps</strong></a><br/></td>
<td>Proporciona métodos que recuperan propiedades de códec específicas del formato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecstrings"><strong>IWMCodecStrings</strong></a><br/></td>
<td>Recupera nombres y cadenas descriptivas para códecs y formatos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops"><strong>IWMColorConvProps</strong></a><br/></td>
<td>Establece las propiedades del DSP del convertidor de colores. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops"><strong>IWMResamplerProps</strong></a><br/></td>
<td>Establece propiedades en el DSP del remuestreador de audio. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops"><strong>IWMResizerProps</strong></a><br/></td>
<td>Establece las propiedades del DSP de tamaño de vídeo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmsampleextensionsupport"><strong>IWMSampleExtensionSupport</strong></a><br/></td>
<td>Configura la compatibilidad con códecs para las extensiones de ejemplo. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderhurryup"><strong>IWMVideoDecoderHurryup</strong></a><br/></td>
<td>Controla la velocidad del descodificador de vídeo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderreconbuffer"><strong>IWMVideoDecoderReconBuffer</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta interfaz está obsoleta y no debe usarse.
</blockquote>
<br/> Administra fotogramas de vídeo reconstruidos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideoforcekeyframe"><strong>IWMVideoForceKeyFrame</strong></a><br/></td>
<td>Obliga al codificador a codificar el fotograma actual como un fotograma clave. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de Media Foundation](media-foundation-programming-reference.md)
</dt> </dl>

 

 
