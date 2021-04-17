---
description: Prueba de si un controlador de gráficos es compatible con COPP
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: Prueba de si un controlador de gráficos es compatible con COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f98a5bfc3f577d1acb45969ec5d10503ae87b27a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688209"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a><span data-ttu-id="e715f-103">Prueba de si un controlador de gráficos es compatible con COPP</span><span class="sxs-lookup"><span data-stu-id="e715f-103">Testing Whether a Graphics Driver Supports COPP</span></span>

<span data-ttu-id="e715f-104">El protocolo de protección de la salida certificada (COPP) permite a una aplicación proteger el contenido de vídeo mientras se desplaza desde la tarjeta de vídeo hasta el dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e715f-104">Certified Output Protection Protocol (COPP) enables an application to protect video content as it travels from the video card to the display device.</span></span> <span data-ttu-id="e715f-105">Si un controlador de gráficos admite COPP, el controlador contiene una cadena de certificados, firmada por Microsoft, que autentica el controlador.</span><span class="sxs-lookup"><span data-stu-id="e715f-105">If a graphics driver supports COPP, the driver holds a certificate chain, signed by Microsoft, authenticating the driver.</span></span> <span data-ttu-id="e715f-106">Las aplicaciones de reproducción que usan COPP para aplicar la protección de contenido deben validar la cadena de certificados para asegurarse de que el controlador no se ha alterado.</span><span class="sxs-lookup"><span data-stu-id="e715f-106">Playback applications that use COPP to enforce content protection must validate the certificate chain to ensure that the driver has not been tampered with.</span></span>

<span data-ttu-id="e715f-107">Sin embargo, es posible que desee comprobar si un controlador de gráficos es compatible con COPP, sin validar el certificado.</span><span class="sxs-lookup"><span data-stu-id="e715f-107">However, you might want to check whether a graphics driver supports COPP, without validating the certificate.</span></span> <span data-ttu-id="e715f-108">Por ejemplo, cuando un proveedor de medios digitales emite una licencia de administración de derechos digitales (DRM), es posible que desee comprobar si el usuario tiene un controlador de gráficos habilitado para COPP.</span><span class="sxs-lookup"><span data-stu-id="e715f-108">For example, when a digital media provider issues a digital rights management (DRM) license, it might want to check whether the user has a COPP-enabled graphics driver.</span></span> <span data-ttu-id="e715f-109">El proveedor no necesita aplicar COPP en el momento en que emite la licencia; solo necesita probar si el controlador es compatible con COPP.</span><span class="sxs-lookup"><span data-stu-id="e715f-109">The provider does not need to enforce COPP at the time it issues the license; it only needs to test whether the driver supports COPP.</span></span>

<span data-ttu-id="e715f-110">En el código siguiente se muestra cómo probar si un controlador es compatible con COPP.</span><span class="sxs-lookup"><span data-stu-id="e715f-110">The following code shows how to test whether a driver supports COPP.</span></span> <span data-ttu-id="e715f-111">La aplicación debe pasar el nombre de un archivo de vídeo que se utilizará para probar el controlador.</span><span class="sxs-lookup"><span data-stu-id="e715f-111">The application must pass in the name of a video file that will be used to test the driver.</span></span> <span data-ttu-id="e715f-112">Esto es necesario porque el filtro de representador de combinación de vídeo de Microsoft® DirectShow® no Inicializa una sesión de COPP hasta que el filtro está conectado.</span><span class="sxs-lookup"><span data-stu-id="e715f-112">This is required because the Video Mixing Renderer filter in Microsoft® DirectShow® does not initialize a COPP session until the filter is connected.</span></span> <span data-ttu-id="e715f-113">Esta función se puede incluir en una aplicación cliente para comprobar si el controlador es capaz de ejecutar COPP.</span><span class="sxs-lookup"><span data-stu-id="e715f-113">This function can be included in a client application to check if the driver is capable of running COPP.</span></span>

> [!Note]  
> <span data-ttu-id="e715f-114">Si el equipo del usuario tiene dos tarjetas gráficas, esta función prueba el controlador para la tarjeta de gráficos principal, pero no la tarjeta de gráficos secundaria.</span><span class="sxs-lookup"><span data-stu-id="e715f-114">If the user's computer has two graphics cards, this function tests the driver for the primary graphics card, but not the secondary graphics card.</span></span>

 


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



## <a name="related-topics"></a><span data-ttu-id="e715f-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e715f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e715f-116">Usar el protocolo de protección de salida certificada</span><span class="sxs-lookup"><span data-stu-id="e715f-116">Using Certified Output Protection Protocol</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



