---
description: En este tema se describe cómo admitir DirectX Video Acceleration (DXVA) 2.0 en un filtro DirectShow descodificador.
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: Compatibilidad con DXVA 2.0 en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58631a407e42c0561ebee0ad2b3187e248fc2d25dc0bdf4e98ed0219d8dae916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238088"
---
# <a name="supporting-dxva-20-in-directshow"></a>Compatibilidad con DXVA 2.0 en DirectShow

En este tema se describe cómo admitir DirectX Video Acceleration (DXVA) 2.0 en un filtro DirectShow descodificador. En concreto, describe la comunicación entre el descodificador y el representador de vídeo. En este tema no se describe cómo implementar la decodificación de DXVA.

-   [Requisitos previos](#prerequisites)
-   [Notas de migración](#migration-notes)
-   [Buscar una configuración de descodificador](#finding-a-decoder-configuration)
-   [Notificación al representador de vídeo](#notifying-the-video-renderer)
-   [Asignación de búferes sin comprimir](#allocating-uncompressed-buffers)
-   [Descodificación](#decoding)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

En este tema se da por supuesto que está familiarizado con la escritura de DirectShow filtros. Para obtener más información, vea el tema [Writing DirectShow Filters (Escribir filtros de DirectShow](../directshow/writing-directshow-filters.md) SDK). En los ejemplos de código de este tema se supone que el filtro de descodificador se deriva de la [**clase CTransformFilter,**](../directshow/ctransformfilter.md) con la siguiente definición de clase:


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



En el resto de este tema, el término *descodificador* hace referencia al filtro de descodificador, que recibe vídeo comprimido y genera vídeo sin comprimir. El término *dispositivo descodificador* hace referencia a un acelerador de vídeo de hardware implementado por el controlador de gráficos.

Estos son los pasos básicos que debe realizar un filtro de descodificador para admitir DXVA 2.0:

1.  Negociar un tipo de medio.
2.  Busque una configuración de descodificador DXVA.
3.  Notifique al representador de vídeo que el descodificador usa la descodificación DXVA.
4.  Proporcione un asignador personalizado que asigne superficies de Direct3D.

Estos pasos se describen con más detalle en el resto de este tema.

## <a name="migration-notes"></a>Notas de migración

Si va a migrar desde DXVA 1.0, debe tener en cuenta algunas diferencias significativas entre las dos versiones:

-   DXVA 2.0 no usa las interfaces [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) y [**IAMVideoAcceleratorNotify,**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) ya que el descodificador puede acceder a las API de DXVA 2.0 directamente a través de la interfaz [**IDirectXVideoDecoder.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)
-   Durante la negociación del tipo de medio, el descodificador no usa un GUID de aceleración de vídeo como subtipo. En su lugar, el subtipo es simplemente el formato de vídeo sin comprimir (por ejemplo, NV12), como con la decodificación de software.
-   El procedimiento para configurar el acelerador ha cambiado. En DXVA 1.0, el descodificador llama a **Execute** con una estructura **\_ ConfigPictureDecode** de DXVA para configurar el accerlator. En DXVA 2.0, el descodificador usa la interfaz [**IDirectXVideoDecoderService,**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) como se describe en la sección siguiente.
-   El descodificador asigna los búferes sin comprimir. El representador de vídeo ya no los asigna.
-   En lugar de llamar [**a IAMVideoAccelerator::D isplayFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) para mostrar el marco descodificado, el descodificador entrega el fotograma al representador mediante una llamada a [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), como con la descodificación de software.
-   El descodificador ya no es responsable de comprobar cuándo los búferes de datos son seguros para las actualizaciones. Por lo tanto, DXVA 2.0 no tiene ningún método equivalente a [**IAMVideoAccelerator::QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).
-   La combinación de subimagen se realiza mediante el representador de vídeo, mediante las API del procesador de vídeo DXVA2.0. Los descodificadores que proporcionan subapictures (por ejemplo, descodificadores de DVD) deben enviar datos de subpicture en un pin de salida independiente.

Para las operaciones decoding, DXVA 2.0 usa las mismas estructuras de datos que DXVA 1.0.

El filtro de representador de vídeo mejorado (EVR) admite DXVA 2.0. Los filtros de representador de mezcla de vídeo (VMR-7 y VMR-9) solo admiten DXVA 1.0.

## <a name="finding-a-decoder-configuration"></a>Buscar una configuración de descodificador

Una vez que el descodificador negocia el tipo de medio de salida, debe encontrar una configuración compatible para el dispositivo descodificador DXVA. Puede realizar este paso dentro del método [**CBaseOutputPin::CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) del pin de salida. Este paso garantiza que el controlador de gráficos admite las funcionalidades necesarias para el descodificador, antes de que el descodificador se confirme en el uso de DXVA.

Para buscar una configuración para el dispositivo descodificador, haga lo siguiente:

1.  Consulte el pin de entrada del representador para la [**interfaz IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
2.  Llame [**a IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener un puntero a la [**interfaz IDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) El GUID del servicio es MR \_ VIDEO \_ ACCELERATION \_ SERVICE.
3.  Llame a [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obtener un identificador para el dispositivo Direct3D del representador.
4.  Llame [**a IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) y pase el identificador del dispositivo. Este método devuelve un puntero a la [**interfaz IDirectXVideoDecoderService.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)
5.  Llame [**a IDirectXVideoDecoderService::GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Este método devuelve una matriz de GUID de dispositivo descodificador.
6.  Recorrer en bucle la matriz de GUID de descodificador para buscar los que admite el filtro de descodificador. Por ejemplo, para un descodificador MPEG-2, buscaría **DXVA2 \_ ModeMPEG2 \_ MOCOMP,** **DXVA2 \_ ModeMPEG2 \_ IDCT** o **DXVA2 \_ ModeMPEG2 \_ VLD**.

7.  Cuando encuentre un GUID de dispositivo descodificador candidato, pase el GUID al método [**IDirectXVideoDecoderService::GetDecoderRenderTargets.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) Este método devuelve una matriz de formatos de destino de representación, especificados como **valores D3DFORMAT.**
8.  Recorrer en bucle los formatos de destino de representación y buscar uno que coincida con el formato de salida. Normalmente, un dispositivo descodificador admite un único formato de destino de representación. El filtro de descodificador debe conectarse al representador mediante este subtipo. En la primera llamada a [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), el descodificador puede degradar el formato de destino de representación y, a continuación, devolver este formato como un tipo de salida preferido.

9.  Llame [**a IDirectXVideoDecoderService::GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Pase el mismo GUID de dispositivo descodificador, junto con una [**estructura \_ DxVA2 VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) que describe el formato propuesto. El método devuelve una matriz de [**estructuras \_ ConfigPictureDecode de DXVA2.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) Cada estructura describe una posible configuración para el dispositivo descodificador.

10. Suponiendo que los pasos anteriores son correctos, almacene el identificador del dispositivo Direct3D, el GUID del dispositivo descodificador y la estructura de configuración. El filtro usará esta información para crear el dispositivo descodificador.

El código siguiente muestra cómo buscar una configuración de descodificador.


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



Dado que este ejemplo es genérico, parte de la lógica se ha colocado en funciones auxiliares que tendría que implementar el descodificador. En el código siguiente se muestran las declaraciones de estas funciones:


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a>Notificación al representador de vídeo

Si el descodificador encuentra una configuración de descodificador, el siguiente paso es notificar al representador de vídeo que el descodificador usará la aceleración de hardware. Puede realizar este paso dentro del [**método CompleteConnect.**](../directshow/cbaseoutputpin-completeconnect.md) Este paso debe producirse antes de seleccionar el asignador, ya que afecta a cómo se selecciona el asignador.

1.  Consulte el pin de entrada del representador para la [**interfaz IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
2.  Llame [**a IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener un puntero a la [**interfaz IDirectXVideoMemoryConfiguration.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) El GUID del servicio es **MR \_ VIDEO ACCELERATION \_ \_ SERVICE**.
3.  Llame a [**IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) en un bucle, lo que incrementa la variable *dwTypeIndex* de cero. Se detiene cuando el método devuelve el valor **DXVA2 \_ SurfaceType \_ DecoderRenderTarget** en el *parámetro pdwType.* Este paso garantiza que el representador de vídeo admite lacodización acelerada por hardware. Este paso siempre se realizará correctamente para el filtro EVR.
4.  Si el paso anterior se ha hecho correctamente, llame a [**IDirectXVideoMemoryConfiguration::SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) con el valor DXVA2 \_ SurfaceType \_ DecoderRenderTarget. Al **llamar a SetSurfaceType** con este valor, el representador de vídeo se pone en modo DXVA. Cuando el representador de vídeo está en este modo, el descodificador debe proporcionar su propio asignador.

El código siguiente muestra cómo notificar al representador de vídeo.


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



Si el descodificador encuentra una configuración válida y notifica correctamente al representador de vídeo, el descodificador puede usar DXVA para descodificar. El descodificador debe implementar un asignador personalizado para su pin de salida, como se describe en la sección siguiente.

## <a name="allocating-uncompressed-buffers"></a>Asignación de búferes sin comprimir

En DXVA 2.0, el descodificador es responsable de asignar superficies de Direct3D para usarlas como búferes de vídeo sin comprimir. Por lo tanto, el descodificador debe implementar un asignador personalizado que creará las superficies. Los ejemplos de medios proporcionados por este asignador contendrán punteros a las superficies de Direct3D. El EVR recupera un puntero a la superficie mediante una llamada [**a IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en el ejemplo multimedia. El identificador de servicio es **MR \_ BUFFER \_ SERVICE.**

Para proporcionar el asignador personalizado, realice los pasos siguientes:

1.  Defina una clase para los ejemplos multimedia. Esta clase puede derivar de la [**clase CMediaSample.**](../directshow/cmediasample.md) Dentro de esta clase, haga lo siguiente:
    -   Almacene un puntero a la superficie de Direct3D.
    -   Implemente [**la interfaz IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) En el [**método GetService,**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) si el GUID del servicio es **MR BUFFER \_ \_ SERVICE,** consulte la superficie de Direct3D para la interfaz solicitada. De lo contrario, **GetService** puede devolver **MF E \_ \_ UNSUPPORTED \_ SERVICE**.
    -   Invalide [**el método CMediaSample::GetPointer**](../directshow/cmediasample-getpointer.md) para devolver E \_ NOTIMPL.
2.  Defina una clase para el asignador. El asignador puede derivar de la [**clase CBaseAllocator.**](../directshow/cbaseallocator.md) Dentro de esta clase, haga lo siguiente.
    -   Invalide [**el método CBaseAllocator::Alloc.**](../directshow/cbaseallocator-alloc.md) Dentro de este método, llame [**a IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) para crear las superficies. (La [**interfaz IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) hereda este método de [**IDirectXVideoAccelerationService).**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice)
    -   Invalide [**el método CBaseAllocator::Free**](../directshow/cbaseallocator-free.md) para liberar las superficies.
3.  En el pin de salida del filtro, invalide el [**método CBaseOutputPin::InitAllocator.**](../directshow/cbaseoutputpin-initallocator.md) Dentro de este método, cree una instancia del asignador personalizado.
4.  En el filtro, implemente el [**método CTransformFilter::D ecideBufferSize.**](../directshow/ctransformfilter-decidebuffersize.md) El *parámetro pProperties* indica el número de superficies que requiere la EVR. Agregue a este valor el número de superficies que requiere el descodificador y llame a [**IMemAllocator::SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) en el asignador.

El código siguiente muestra cómo implementar la clase de ejemplo multimedia:


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



El código siguiente muestra cómo implementar el [**método Alloc**](../directshow/cbaseallocator-alloc.md) en el asignador.


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



Este es el código del [**método Free:**](../directshow/cbaseallocator-free.md)


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



Para obtener más información sobre la implementación de asignadores personalizados, vea el tema [Proporcionar un](../directshow/providing-a-custom-allocator.md) asignador personalizado en la documentación DirectShow SDK.

## <a name="decoding"></a>Descodificación

Para crear el dispositivo descodificador, llame [**a IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). El método devuelve un puntero a la [**interfaz IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) del dispositivo descodificador.

En cada fotograma, llame a [**IDirect3DDeviceManager9::TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) para probar el identificador del dispositivo. Si el dispositivo ha cambiado, el método devuelve DXVA2 \_ E \_ NEW VIDEO \_ \_ DEVICE. Si esto ocurre, haga lo siguiente:

1.  Cierre el identificador del dispositivo mediante una [**llamada a IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Libere los [**punteros IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) [**e IDirectXVideoDecoder.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)
3.  Abra un nuevo identificador de dispositivo.
4.  Negocie una nueva configuración de descodificador, como se describe en la sección [Búsqueda de una configuración de descodificador.](#finding-a-decoder-configuration)
5.  Cree un nuevo dispositivo descodificador.

Suponiendo que el identificador del dispositivo es válido, el proceso de descodización funciona de la siguiente manera:

1.  Llame [**a IDirectXVideoDecoder::BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
2.  Haga lo siguiente una o varias veces:
    1.  Llame [**a IDirectXVideoDecoder::GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) para obtener un búfer de descodificador DXVA.
    2.  Rellene el búfer.
    3.  Llame [**a IDirectXVideoDecoder::ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
3.  Llame [**a IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) para realizar las operaciones de descodificación en el marco.

DXVA 2.0 usa las mismas estructuras de datos que DXVA 1.0 para las operaciones de decodificación. Para el conjunto original de perfiles dxva (para H.261, H.263 y MPEG-2), estas estructuras de datos se describen en la especificación [DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration).

Dentro de cada par de [**llamadas BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)Execute, puede llamar a GetBuffer varias veces, pero solo una vez para / [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) cada tipo de búfer DXVA. [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) Si lo llama dos veces con el mismo tipo de búfer, sobrescribirá los datos.

Después de [**llamar a Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), llame a [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) para entregar el fotograma al representador de vídeo, como con lacoding de software. El **método Receive** es asincrónico; después de que vuelva, el descodificador puede seguir descodificando el fotograma siguiente. El controlador para mostrar evita que los comandos de decoding sobrescriban el búfer mientras el búfer está en uso. El descodificador no debe reutilizar una superficie para descodificar otro marco hasta que el representador haya publicado el ejemplo. Cuando el representador libera el ejemplo, el asignador vuelve a poner el ejemplo en su grupo de ejemplos disponibles. Para obtener el siguiente ejemplo disponible, llame a [**CBaseOutputPin::GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), que a su vez llama a [**IMemAllocator::GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer). Para obtener más información, vea el tema [Overview of Data Flow in DirectShow](../directshow/overview-of-data-flow-in-directshow.md) en la documentación DirectShow datos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aceleración de vídeo de DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
