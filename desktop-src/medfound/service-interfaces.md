---
description: Interfaces de servicio
ms.assetid: 264a0e86-49e9-4777-956b-a83e9db52a25
title: Interfaces de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31687cc1c1283eb59c7731743eaf4ece0127b392
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574801"
---
# <a name="service-interfaces"></a>Interfaces de servicio

Algunas interfaces de Media Foundation deben obtenerse llamando [**a IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en lugar de mediante una llamada **a QueryInterface**. El [**método GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) funciona como QueryInterface, pero con las siguientes diferencias:

-   Toma un GUID de identificador de servicio además del identificador de interfaz.
-   Puede devolver un puntero a otro objeto que implementa la interfaz, en lugar de devolver un puntero al objeto original que se consulta.

> [!Note]  
> La [**interfaz IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) es muy similar a la **interfaz IServiceProvider** que se usa en otras API.

 

Un *servicio* es una interfaz determinada obtenida de una clase determinada de objetos a través de la [**interfaz IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) Se definen los siguientes servicios.



| Identificador de servicio                          | Interfaz                                                                                                                                | Objetos que podrían exponer este servicio                                                                                                            |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| SERVICIO DEL \_ PROVEEDOR \_ DE METADATOS \_ MF             | [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)                                                                                       | Orígenes multimedia                                                                                                                                     |
| SERVICIO \_ MF \_ MEDIASOURCE                    | [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                                                                                 | Se admite en Windows 8.1 y versiones posteriores.<br/>                                                                                                    |
| CONTEXTO \_ DE SERVIDOR DE MF PMP \_ \_                    | [**IMFPMPServer**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)                                                                                                     | Sesión multimedia de ruta de acceso de medios protegida (PMP).                                                                                                         |
| MF \_ QUALITY \_ SERVICES                       | [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                                                                                             | Orígenes multimedia.                                                                                                                                    |
| MF \_ RATE \_ CONTROL \_ SERVICE                  | [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                                                                                                 | Orígenes multimedia, Sesión multimedia                                                                                                                      |
| MF \_ RATE \_ CONTROL \_ SERVICE                  | [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                                                                                                 | Orígenes multimedia, receptores de medios, sesión multimedia                                                                                                         |
| PROXY \_ REMOTO \_ MF                           | [**IMFRemoteProxy**](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)                                                                                                 | Servidores proxy para objetos remotos.                                                                                                                       |
| MF \_ SAMI \_ SERVICE                           | [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)                                                                                                     | Origen multimedia de intercambio multimedia accesible sincronizado (SAMI).                                                                                    |
| SERVICIO DE \_ PROVEEDOR DE PRESENTACIÓN DE ORIGEN \_ \_ \_ MF | [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider)                                                         | Origen del secuenciador                                                                                                                                  |
| SERVICIO \_ MF TIMECODE \_                       | [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)                                                                                     | Origen multimedia de ASF.                                                                                                                                 |
| SERVICIO DEL EDITOR DE ATRIBUTOS MF \_ TOPONODE \_ \_ \_    | [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)                                                                 | Sesión multimedia                                                                                                                                     |
| MF \_ WRAPPED \_ (OBJETO)                         | [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)                                                                                                   | Objetos encapsulados                                                                                                                                   |
| SERVICIO DE \_ \_ BÚFER \_ ENCAPSULADO MF                |                                                                                                                                          | Se admite en Windows 8.1 y versiones posteriores.<br/>                                                                                                    |
| MANTENIMIENTO DE \_ MUESTRAS \_ ENCAPSULADAS \_ EN MF                 |                                                                                                                                          | Se admite en Windows 8.1 y versiones posteriores.<br/>                                                                                                    |
| MF \_ WORKQUEUE \_ SERVICES                     | [**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)                                                                                     | Sesión multimedia                                                                                                                                     |
| SERVICIO \_ SAVEJOB DE MFNET \_                     | [**IMFSaveJob**](/windows/desktop/api/mfidl/nn-mfidl-imfsavejob)                                                                                                         | Secuencias de bytes                                                                                                                                      |
| SERVICIO DE \_ ESTADÍSTICAS \_ MFNETSOURCE            | **IPropertyStore**                                                                                                                       | Origen de red. Use este servicio para recuperar estadísticas de red. Vea [**PROPIEDAD MFNETSOURCE \_ STATISTICS**](mfnetsource-statistics-property.md). |
| SERVICIO DE \_ DIRECTIVA DE AUDIO DE \_ \_ MR                  | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)                                                                                                 | Representador de audio                                                                                                                                    |
| SERVICIO DE \_ BÚFER \_ DE MR                         | **IDirect3DSurface9**                                                                                                                    | Búferes de superficie de DirectX                                                                                                                           |
| SERVICIO DE \_ VOLUMEN DE DIRECTIVA DE CAPTURA DE \_ \_ \_ MR        | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Origen de captura de audio                                                                                                                              |
| SERVICIO DE \_ VOLUMEN DE DIRECTIVA DE \_ \_ MR                 | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Representador de audio                                                                                                                                    |
| SERVICIO DE VOLUMEN DE MR \_ STREAM \_ \_                 | [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume)                                                                                     | Representador de audio                                                                                                                                    |
| SERVICIO DE \_ \_ ACELERACIÓN DE \_ VÍDEO DE MR            | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9), [ **IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice) | Representador de vídeo mejorado (EVR)                                                                                                                     |
| SERVICIO DE \_ \_ ACELERACIÓN DE \_ VÍDEO DE MR            | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                             | Pines de entrada en el filtro DirectShow EVR                                                                                                           |
| SERVICIO DE \_ \_ ACELERACIÓN DE \_ VÍDEO DE MR            | [**INTERFAZ DE DISPOSITIVOVIDEOSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)                                                                     | Receptores de flujo EVR.                                                                                                                                 |
| SERVICIO MR \_ VIDEO \_ MIXER \_                   | Varias interfaces expuestas por el mezclador EVR. Consulte [Uso de los controles de Mixer vídeo.](using-the-video-mixer-controls.md)                   | EVR                                                                                                                                               |
| SERVICIO MR \_ VIDEO \_ RENDER \_                  | Varias interfaces expuestas por el presentador de EVR. Consulte [Uso de los controles de visualización de vídeo](using-the-video-display-controls.md).           | EVR                                                                                                                                               |



 

Debe usar [**GetService para obtener las**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) interfaces enumeradas en esta tabla de los objetos enumerados en esta tabla.

En algunos casos, una clase de objetos devuelve una interfaz como servicio y otra clase de objetos devuelve a través de **QueryInterface.** Las páginas de referencia de cada interfaz indican cuándo usar [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) y cuándo usar **QueryInterface**.

> [!Caution]  
> Un objeto podría implementarse de tal manera que devuelva una interfaz de servicio a través de **QueryInterface** y [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice). Sin embargo, el **uso de QueryInterface** cuando **se requiere GetService** puede provocar problemas de compatibilidad más adelante.

 

La [**función MFGetService es**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) una función auxiliar que consulta un objeto para [**MFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) y, a continuación, llama al [**método GetService del**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) objeto.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se consulta la sesión multimedia [**para ELSERVICIODEGETGET Y**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) se obtiene la [**interfaz DERRATEControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)


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



El ejemplo siguiente es equivalente al ejemplo anterior, pero usa la [**función MFGetService.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)


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

[**INTERFAZ DE SERVICIOGETGET**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
</dt> <dt>

[Media Foundation PLATFORM API](media-foundation-platform-apis.md)
</dt> </dl>

 

 




