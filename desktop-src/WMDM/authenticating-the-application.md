---
title: Autenticación de la aplicación
description: Autenticación de la aplicación
ms.assetid: 011815fa-d55c-4abc-9ec8-55d754827342
keywords:
- Windows Media Administrador de dispositivos, autenticación
- Administrador de dispositivos, autenticación
- Guía de programación, autenticación
- aplicaciones de escritorio, autenticación
- crear aplicaciones de Windows Media Administrador de dispositivos, autenticación
- autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7779cdbb874278e6b62517cc2c1983dd2ce8fa1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695623"
---
# <a name="authenticating-the-application"></a><span data-ttu-id="76f80-109">Autenticación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="76f80-109">Authenticating the Application</span></span>

<span data-ttu-id="76f80-110">El primer paso que debe realizar la aplicación es la autenticación.</span><span class="sxs-lookup"><span data-stu-id="76f80-110">The first step your application must perform is authentication.</span></span> <span data-ttu-id="76f80-111">La autenticación comprueba la identidad de la aplicación para Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="76f80-111">Authentication verifies the application's identity to Windows Media Device Manager.</span></span> <span data-ttu-id="76f80-112">Después de autenticar la aplicación, puede llamar a **QueryInterface** para obtener la interfaz raíz [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) , que se puede consultar para otras interfaces necesarias, que se pueden consultar a sí mismas para todas las demás interfaces.</span><span class="sxs-lookup"><span data-stu-id="76f80-112">Once you authenticate your application, you can call **QueryInterface** to get the root [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) interface, which can be queried for other required interfaces, which can themselves be queried for all other interfaces.</span></span> <span data-ttu-id="76f80-113">La autenticación solo debe realizarse una vez, en el inicio.</span><span class="sxs-lookup"><span data-stu-id="76f80-113">Authentication need only take place once, on startup.</span></span>

<span data-ttu-id="76f80-114">Para autenticar la aplicación, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="76f80-114">To authenticate your application, perform these steps:</span></span>

1.  <span data-ttu-id="76f80-115">Cocree el objeto **MediaDevMgr** (ID. de clase MediaDevMgr) y solicite una interfaz [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="76f80-115">CoCreate the **MediaDevMgr** object (class ID MediaDevMgr), and request an [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span>
2.  <span data-ttu-id="76f80-116">Cree un objeto [CSecureChannelClient](csecurechannelclient-class.md) para controlar la autenticación.</span><span class="sxs-lookup"><span data-stu-id="76f80-116">Create a [CSecureChannelClient](csecurechannelclient-class.md) object to handle the authentication.</span></span>
3.  <span data-ttu-id="76f80-117">Pase la clave de aplicación y transfiera el certificado al objeto de canal seguro.</span><span class="sxs-lookup"><span data-stu-id="76f80-117">Pass your application key and transfer certificate to the secure channel object.</span></span> <span data-ttu-id="76f80-118">Puede usar la clave o el certificado ficticios que se muestran en el siguiente código de ejemplo para obtener la funcionalidad básica de las funciones del SDK.</span><span class="sxs-lookup"><span data-stu-id="76f80-118">You can use the dummy key/certificate shown in the following example code to get basic functionality from SDK functions.</span></span> <span data-ttu-id="76f80-119">Sin embargo, para obtener toda la funcionalidad (importante para pasar archivos hacia y desde el dispositivo), debe solicitar una clave y un certificado de Microsoft, tal y como se describe en [herramientas de desarrollo](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="76f80-119">However, to get full functionality (important for passing files to and from the device), you must request a key and certificate from Microsoft as described in [Tools for Development](tools-for-development.md).</span></span>
4.  <span data-ttu-id="76f80-120">Pase la interfaz **IComponentAuthenticate** que creó en el paso 1 al objeto de canal seguro.</span><span class="sxs-lookup"><span data-stu-id="76f80-120">Pass the **IComponentAuthenticate** interface you created in step 1 to the secure channel object.</span></span>
5.  <span data-ttu-id="76f80-121">Llame a [**CSecureChannelClient:: Authenticate**](/previous-versions/ms983906(v=msdn.10)) para autenticar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="76f80-121">Call [**CSecureChannelClient::Authenticate**](/previous-versions/ms983906(v=msdn.10)) to authenticate your application.</span></span>
6.  <span data-ttu-id="76f80-122">Consulte **IComponentAuthenticate** de la interfaz **IWMDeviceManager** .</span><span class="sxs-lookup"><span data-stu-id="76f80-122">Query **IComponentAuthenticate** for the **IWMDeviceManager** interface.</span></span>

<span data-ttu-id="76f80-123">Estos pasos se muestran en el siguiente código de C++.</span><span class="sxs-lookup"><span data-stu-id="76f80-123">These steps are shown in the following C++ code.</span></span>


```C++
HRESULT CWMDMController::Authenticate()
{
    // Use a dummy key/certificate pair to allow basic functionality.
    // An authentic keypair is required for full SDK functionality.
    BYTE abPVK[] = {0x00};
    BYTE abCert[] = {0x00};
    HRESULT hr;
    CComPtr<IComponentAuthenticate> pAuth;

    // Create the WMDM object and acquire 
    // its authentication interface.
    hr = CoCreateInstance(
        __uuidof(MediaDevMgr),
        NULL,
        CLSCTX_INPROC_SERVER,
        __uuidof(IComponentAuthenticate),
        (void**)&pAuth);

    if (FAILED(hr)) return hr;

    // Create the secure channel client class needed to authenticate the application.
    // We'll use a global member variable to hold the secure channel client
    // in case we need to handle encryption, decryption, or MAC verification
    // during this session.
    m_pSAC = new CSecureChannelClient;
    if (m_pSAC == NULL) return E_FAIL;

    // Send the application's transfer certificate and the associated 
    // private key to the secure channel client.
    hr = m_pSAC->SetCertificate(
        SAC_CERT_V1,
        (BYTE *)abCert, sizeof(abCert),
        (BYTE *)abPVK,  sizeof(abPVK));
    if (FAILED(hr)) return hr;
            
    // Send the authentication interface we created to the secure channel 
    // client and authenticate the application with the V1 protocol.
    // (This is the only protocol currently supported.)
    m_pSAC->SetInterface(pAuth);
    hr = m_pSAC->Authenticate(SAC_PROTOCOL_V1);
    if (FAILED(hr)) return hr;

    // Authentication succeeded, so we can use WMDM.
    // Query for the root WMDM interface.
    hr = pAuth->QueryInterface( __uuidof(IWMDeviceManager), (void**)&m_IWMDMDeviceMgr);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="76f80-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76f80-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76f80-125">**Crear una aplicación de Windows Media Administrador de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="76f80-125">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 