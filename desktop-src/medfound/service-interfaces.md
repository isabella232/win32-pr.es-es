---
description: Interfaces de servicio
ms.assetid: 264a0e86-49e9-4777-956b-a83e9db52a25
title: Interfaces de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31687cc1c1283eb59c7731743eaf4ece0127b392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715493"
---
# <a name="service-interfaces"></a>Interfaces de servicio

Algunas interfaces de Media Foundation se deben obtener llamando a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en lugar de llamando a **QueryInterface**. El método [**GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) funciona como QueryInterface, pero con las siguientes diferencias:

-   Toma un GUID de identificador de servicio además del identificador de interfaz.
-   Puede devolver un puntero a otro objeto que implementa la interfaz, en lugar de devolver un puntero al objeto original que se consulta.

> [!Note]  
> La interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) es muy similar a la interfaz **IServiceProvider** utilizada en otras API.

 

Un *servicio* es una interfaz determinada obtenida de una clase determinada de objetos a través de la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . Se definen los siguientes servicios.



| Identificador de servicio                          | Interfaz                                                                                                                                | Objetos que pueden exponer este servicio                                                                                                            |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| \_servicio de proveedor de metadatos MF \_ \_             | [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)                                                                                       | Orígenes multimedia                                                                                                                                     |
| \_servicio MF MEDIASOURCE \_                    | [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                                                                                 | Se admite en Windows 8.1 y versiones posteriores.<br/>                                                                                                    |
| contexto de servidor de MF \_ PMP \_ \_                    | [**IMFPMPServer**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)                                                                                                     | Sesión de medios de la ruta de acceso multimedia protegida (PMP).                                                                                                         |
| \_servicios de calidad MF \_                       | [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                                                                                             | Orígenes multimedia.                                                                                                                                    |
| \_servicio de \_ control de tasa MF \_                  | [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                                                                                                 | Orígenes multimedia, sesión multimedia                                                                                                                      |
| \_servicio de \_ control de tasa MF \_                  | [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                                                                                                 | Orígenes multimedia, receptores multimedia, sesión multimedia                                                                                                         |
| \_proxy remoto \_ MF                           | [**IMFRemoteProxy**](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)                                                                                                 | Servidores proxy para objetos remotos.                                                                                                                       |
| \_servicio MF Sami \_                           | [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)                                                                                                     | Origen de medios de intercambio de medios accesibles (SAMI) sincronizado.                                                                                    |
| \_servicio de \_ proveedor de presentación de origen MF \_ \_ | [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider)                                                         | Origen del secuenciador                                                                                                                                  |
| \_servicio de código de tiempo MF \_                       | [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)                                                                                     | Origen de medios ASF.                                                                                                                                 |
| \_servicio de \_ Editor de atributos \_ \_ de MF TOPONODE    | [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)                                                                 | Sesión multimedia                                                                                                                                     |
| MF \_ ( \_ objeto ajustado)                         | [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)                                                                                                   | Objetos ajustados                                                                                                                                   |
| \_servicio de \_ búfer \_ ajustado MF                |                                                                                                                                          | Se admite en Windows 8.1 y versiones posteriores.<br/>                                                                                                    |
| \_servicio de \_ ejemplo \_ empaquetado de MF                 |                                                                                                                                          | Se admite en Windows 8.1 y versiones posteriores.<br/>                                                                                                    |
| MF \_ WORKQUEUE \_ Services                     | [**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)                                                                                     | Sesión multimedia                                                                                                                                     |
| \_servicio MFNET SAVEJOB \_                     | [**IMFSaveJob**](/windows/desktop/api/mfidl/nn-mfidl-imfsavejob)                                                                                                         | Secuencias de bytes                                                                                                                                      |
| MFNETSOURCE \_ Statistics \_ Service            | **IPropertyStore**                                                                                                                       | Origen de red. Use este servicio para recuperar estadísticas de red. Consulte [**\_ propiedad MFNETSOURCE Statistics**](mfnetsource-statistics-property.md). |
| \_servicio de \_ Directiva de audio Mr \_                  | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)                                                                                                 | Representador de audio                                                                                                                                    |
| \_servicio de búfer Mr \_                         | **IDirect3DSurface9**                                                                                                                    | Búferes de la superficie de DirectX                                                                                                                           |
| servicio de volumen de la \_ Directiva de captura Mr \_ \_ \_        | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Origen de captura de audio                                                                                                                              |
| MR \_ Policy \_ Volume \_ Service                 | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Representador de audio                                                                                                                                    |
| \_servicio de volumen de streaming Mr \_ \_                 | [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume)                                                                                     | Representador de audio                                                                                                                                    |
| \_servicio de \_ aceleración de vídeo Mr \_            | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9), [ **IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice) | Representador de vídeo mejorado (EVR)                                                                                                                     |
| \_servicio de \_ aceleración de vídeo Mr \_            | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                             | Clavijas de entrada en el filtro EVR de DirectShow                                                                                                           |
| \_servicio de \_ aceleración de vídeo Mr \_            | [**Interfaz IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)                                                                     | Receptores de flujo de EVR.                                                                                                                                 |
| \_servicio de \_ mezclador de vídeo Mr \_                   | Varias interfaces expuestas por el mezclador EVR. Consulte [uso de los controles del mezclador de vídeo](using-the-video-mixer-controls.md).                   | EVR                                                                                                                                               |
| \_servicio de \_ representación de vídeo Mr \_                  | Varias interfaces expuestas por el presentador de EVR. Vea [usar los controles de presentación de vídeo](using-the-video-display-controls.md).           | EVR                                                                                                                                               |



 

Debe usar [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener las interfaces enumeradas en esta tabla a partir de los objetos enumerados en esta tabla.

En algunos casos, una interfaz se devuelve como un servicio mediante una clase de objetos y se devuelve a través de **QueryInterface** por otra clase de objetos. Las páginas de referencia de cada interfaz indican Cuándo usar [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) y Cuándo usar **QueryInterface**.

> [!Caution]  
> Un objeto se puede implementar de forma que devuelva una interfaz de servicio a través de **QueryInterface** y [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice). Sin embargo, el uso de **QueryInterface** cuando se requiere **GetService** podría provocar problemas de compatibilidad más adelante.

 

La función [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) es una función auxiliar que consulta un objeto para [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) y, a continuación, llama al método [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) del objeto.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se consulta la sesión multimedia para [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) y se obtiene la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .


```C++
IMFGetService *pGetService = NULL;
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = pMediaSession->QueryInterface(
    IID_IMFGetService, 
    (void**)&pGetService);

if (SUCCEEDED(hr))
{
    hr = pGetService->GetService(
        MF_RATE_CONTROL_SERVICE, 
        IID_IMFRateControl,
        (void**)&pRateControl);
}
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_REELEASE(pGetService);
SAFE_RELEASE(pRateControl);
```



El ejemplo siguiente es equivalente al ejemplo anterior, pero usa la función [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) .


```C++
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = MFGetService(
    pMediaSession, 
    MF_RATE_CONTROL_SERVICE, 
    IID_IMFRateControl, 
    (void**) &pRateCtl 
); 
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_RELEASE(pRateControl);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
</dt> <dt>

[API de Media Foundation Platform](media-foundation-platform-apis.md)
</dt> </dl>

 

 




