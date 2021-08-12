---
description: Comprobar si un controlador de gráficos admite COPP
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: Comprobar si un controlador de gráficos admite COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22280f880ba01a8e51acda74a2a46dff595d5569f885ce1da3a3631bacd8db06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651835"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a>Comprobar si un controlador de gráficos admite COPP

El Protocolo de protección de salida certificado (COPP) permite a una aplicación proteger el contenido de vídeo a medida que viaja desde la tarjeta de vídeo al dispositivo para mostrar. Si un controlador de gráficos admite COPP, el controlador contiene una cadena de certificados, firmada por Microsoft, que autentica el controlador. Las aplicaciones de reproducción que usan COPP para aplicar la protección de contenido deben validar la cadena de certificados para asegurarse de que el controlador no se ha alterado.

Sin embargo, es posible que quiera comprobar si un controlador de gráficos admite COPP, sin validar el certificado. Por ejemplo, cuando un proveedor de medios digitales emite una licencia de administración de derechos digitales (DRM), es posible que desee comprobar si el usuario tiene un controlador de gráficos habilitado para COPP. El proveedor no necesita aplicar COPP en el momento en que emite la licencia; solo tiene que probar si el controlador admite COPP.

El código siguiente muestra cómo probar si un controlador admite COPP. La aplicación debe pasar el nombre de un archivo de vídeo que se usará para probar el controlador. Esto es necesario porque el filtro Representador de mezcla de vídeo de Microsoft® DirectShow® inicializa una sesión COPP hasta que se conecta el filtro. Esta función se puede incluir en una aplicación cliente para comprobar si el controlador es capaz de ejecutar COPP.

> [!Note]  
> Si el equipo del usuario tiene dos tarjetas gráficas, esta función prueba al controlador la tarjeta gráfica principal, pero no la tarjeta gráfica secundaria.

 


```C++
#include <dshow.h>
// Link to strmiids.lib

#define SAFE_RELEASE(p) if (NULL != (p)) { (p)->Release(); (p) = NULL; }
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }

enum COPPSupport 
{
    SUPPORTS_COPP,
    DOES_NOT_SUPPORT_COPP,
    CANNOT_DETERMINE_COPP_SUPPORT
};

//------------------------------------------------------------------------
// Name:        IsDriverCoppEnabled
// Description: Test whether the user's graphics driver supports
//              COPP.
// wszTestFile: Name of a video file to use for testing.
//
// If this method returns the value SUPPORTS_COPP, it does *not* guarantee 
// that the driver is a valid COPP-enabled driver. If you want to use COPP 
// to enforce video output protection, the application *must* validate 
// the certificate returned by the KeyExchange method. 
// 
// The purpose of this function is only to test whether the driver 
// claims to support COPP. 
//------------------------------------------------------------------------

COPPSupport IsDriverCoppEnabled(const WCHAR *wszTestFile)
{
    COPPSupport SupportResult = CANNOT_DETERMINE_COPP_SUPPORT; 

    IGraphBuilder *pGB = NULL;
    IBaseFilter *pRenderer = NULL;
    IAMCertifiedOutputProtection  *pCOPPDevice = NULL;
    BYTE *pbCertificate = NULL;
    GUID  RandomValue = GUID_NULL;
    ULONG cbCertificateLength = NULL;
    
    HRESULT hr = S_OK;

    CHECK_HR(hr = CoInitializeEx(NULL, COINIT_MULTITHREADED));
   
    // Create the Filter Graph Manager.
    CHECK_HR(hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void**)&pGB));

    // Create the VMR-9. 
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9,
        NULL, CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
        (void**)&pRenderer
        ));

    if (FAILED(hr))
    {
        // Try the VMR-7 instead.
        CHECK_HR(hr = CoCreateInstance(CLSID_VideoMixingRenderer,
                NULL, CLSCTX_INPROC, IID_IBaseFilter, 
                (void**)&pRenderer
                ));
    }

    // Add the VMR to the filter graph.
    CHECK_HR(hr = pGB->AddFilter(pRenderer, L"Video Renderer"));

    // Build a default playback graph.
    CHECK_HR(hr = pGB->RenderFile(wszTestFile, NULL));

    // Query for IAMCertifiedOutputProtection.
    CHECK_HR(hr = pRenderer->QueryInterface(IID_IAMCertifiedOutputProtection,
            (void**)&pCOPPDevice));

    // Get the driver's COPP certificate.
    hr = pCOPPDevice->KeyExchange(&RandomValue, &pbCertificate,
        &cbCertificateLength);

    if (SUCCEEDED(hr))
    {
        SupportResult = SUPPORTS_COPP;
    }
    else
    {
        SupportResult = DOES_NOT_SUPPORT_COPP;
    }

done:
    // Clean up.
    CoTaskMemFree(pbCertificate);
    SAFE_RELEASE(pCOPPDevice);
    SAFE_RELEASE(pRenderer);
    SAFE_RELEASE(pGB);
    CoUninitialize();

    return SupportResult;
} 

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del protocolo de protección de salida certificado](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



