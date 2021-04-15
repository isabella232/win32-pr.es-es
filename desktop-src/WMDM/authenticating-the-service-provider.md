---
title: Autenticación del proveedor de servicios
description: Autenticación del proveedor de servicios
ms.assetid: e48a8a7c-0277-4f0c-bad2-5bc9d0286da8
keywords:
- Windows Media Administrador de dispositivos, autenticación
- Administrador de dispositivos, autenticación
- Guía de programación, autenticación
- proveedores de servicios, autenticación
- crear proveedores de servicios, autenticación
- autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271bf5594e4adaede01bb8e3795780f8f5c5177a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695418"
---
# <a name="authenticating-the-service-provider"></a><span data-ttu-id="00dab-109">Autenticación del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="00dab-109">Authenticating the Service Provider</span></span>

<span data-ttu-id="00dab-110">Para ser accesible desde Windows Media Administrador de dispositivos, un proveedor de servicios debe heredar e implementar la interfaz [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="00dab-110">To be accessible from Windows Media Device Manager, a service provider must inherit and implement the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span>

<span data-ttu-id="00dab-111">Para autenticarse, un proveedor de servicios realiza los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="00dab-111">To authenticate itself, a service provider performs the following steps:</span></span>

1.  <span data-ttu-id="00dab-112">Al crear una instancia, se crea un nuevo objeto [CSecureChannelServer](csecurechannelserver-class.md) global y se establecen los valores de certificado y clave a partir de su archivo de clave.</span><span class="sxs-lookup"><span data-stu-id="00dab-112">On instantiation, it creates a new global [CSecureChannelServer](csecurechannelserver-class.md) object and sets the certificate and key values from its key file.</span></span>
2.  <span data-ttu-id="00dab-113">Implementa los métodos [**IComponentAuthenticate:: SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) y [**IComponentAuthenticate:: SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) simplemente pasando los parámetros a su miembro global CSecureChannelServer.</span><span class="sxs-lookup"><span data-stu-id="00dab-113">It implements the [**IComponentAuthenticate::SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) and [**IComponentAuthenticate::SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) methods by simply passing the parameters into its global CSecureChannelServer member.</span></span>
3.  <span data-ttu-id="00dab-114">Antes de controlar los métodos de Administrador de dispositivos de Windows Media implementados, el proveedor de servicios debe comprobar la autenticación del llamador llamando a CSecureChannelServer:: fIsAuthenticated y generar un error si el autor de la llamada no está autenticado.</span><span class="sxs-lookup"><span data-stu-id="00dab-114">Before handling any implemented Windows Media Device Manager methods, the service provider must verify the caller's authentication by calling CSecureChannelServer::fIsAuthenticated, and failing if the caller is not authenticated.</span></span>

<span data-ttu-id="00dab-115">Estos pasos se muestran en los siguientes ejemplos de C++.</span><span class="sxs-lookup"><span data-stu-id="00dab-115">These steps are shown in the following C++ examples.</span></span>

<span data-ttu-id="00dab-116">**Crear el objeto CSecureChannelServer**</span><span class="sxs-lookup"><span data-stu-id="00dab-116">**Creating the CSecureChannelServer object**</span></span>


```C++
CMyServiceProvider::CMyServiceProvider()
{
    HRESULT hr = S_OK;

    // Create the persistent SAC object.
    g_pSAC = new CSecureChannelServer();

    // Set the SAC certificate.
    if (g_pSAC)
    {
        hr = g_pSAC->SetCertificate(
             SAC_CERT_V1,
            (BYTE*)abCert, sizeof(abCert), // SP's certificate.
            (BYTE*)abPVK, sizeof(abPVK)    // SP's key.
        );
    }   
    if (FAILED(hr)) return hr;

    //... Perform other class initialization here ...

    return hr;
}
```



<span data-ttu-id="00dab-117">**Implementar los métodos IComponentAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="00dab-117">**Implementing the IComponentAuthenticate methods**</span></span>


```C++
STDMETHODIMP CMDServiceProvider::SACAuth(
    DWORD   dwProtocolID,
    DWORD   dwPass,
    BYTE   *pbDataIn,
    DWORD   dwDataInLen,
    BYTE  **ppbDataOut,
    DWORD  *pdwDataOutLen)
{
    HRESULT hr = S_OK;

    // Verify that the global CSecureChannelServer member still exists.
    if (!g_pSAC)
        return E_FAIL;

    // Just pass the call to the global SAC member.
    hr = g_pSAC->SACAuth(
        dwProtocolID,
        dwPass,
        pbDataIn, dwDataInLen,
        ppbDataOut, pdwDataOutLen
    );
    return hr;
}

STDMETHODIMP CMDServiceProvider::SACGetProtocols(
    DWORD **ppdwProtocols,
    DWORD  *pdwProtocolCount)
{
    HRESULT hr = E_FAIL;

    if (!g_pSAC)
        return hr;

    hr = g_pSAC->SACGetProtocols(
        ppdwProtocols,
        pdwProtocolCount
    );
    return hr;
}
```



<span data-ttu-id="00dab-118">**Comprobando la autenticación del llamador**</span><span class="sxs-lookup"><span data-stu-id="00dab-118">**Verifying the caller's authentication**</span></span>

<span data-ttu-id="00dab-119">En el ejemplo de código siguiente se muestra un proveedor de servicios que comprueba la autenticación del autor de la llamada como parte de su implementación de la interfaz **IMDServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="00dab-119">The following code example shows a service provider checking the caller's authentication as part of its implementation of the **IMDServiceProvider** interface.</span></span>


```C++
STDMETHODIMP CMyServiceProvider::GetDeviceCount(DWORD * pdwCount)
{
    HRESULT hr = S_OK;
    if (!g_pSAC)
        return E_FAIL;

    if (!(g_pSAC->fIsAuthenticated()))
        return WMDM_E_NOTCERTIFIED;

    *pdwCount = m_DeviceCount;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="00dab-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00dab-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00dab-121">**Creación de un proveedor de servicios**</span><span class="sxs-lookup"><span data-stu-id="00dab-121">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




