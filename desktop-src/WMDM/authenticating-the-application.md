---
title: Autenticación de la aplicación
description: Autenticación de la aplicación
ms.assetid: 011815fa-d55c-4abc-9ec8-55d754827342
keywords:
- Windows Media Administrador de dispositivos,authentication
- Administrador de dispositivos,autenticación
- guía de programación, autenticación
- aplicaciones de escritorio, autenticación
- crear Windows aplicaciones de Administrador de dispositivos multimedia,autenticación
- autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b67ad7c603bbfd3a56667bfcfe8742775c8ae5683888d72661e0a0974aa5358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586740"
---
# <a name="authenticating-the-application"></a>Autenticación de la aplicación

El primer paso que debe realizar la aplicación es la autenticación. La autenticación comprueba la identidad de la aplicación para Windows media Administrador de dispositivos. Una vez que autentique la aplicación, puede llamar a **QueryInterface** para obtener la interfaz [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) raíz, que se puede consultar para otras interfaces necesarias, que a su vez se pueden consultar para todas las demás interfaces. La autenticación solo debe realizarse una vez, en el inicio.

Para autenticar la aplicación, realice estos pasos:

1.  CoCree el **objeto MediaDevMgr** (id. de clase MediaDevMgr) y solicite una [**interfaz IComponentAuthenticate.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
2.  Cree un [objeto CSecureChannelClient](csecurechannelclient-class.md) para controlar la autenticación.
3.  Pase la clave de aplicación y transfiera el certificado al objeto de canal seguro. Puede usar la clave ficticia o el certificado que se muestra en el código de ejemplo siguiente para obtener la funcionalidad básica de las funciones del SDK. Sin embargo, para obtener una funcionalidad completa (importante para pasar archivos hacia y desde el dispositivo), debe solicitar una clave y un certificado a Microsoft como se describe en [Herramientas de desarrollo](tools-for-development.md).
4.  Pase la **interfaz IComponentAuthenticate** que creó en el paso 1 al objeto de canal seguro.
5.  Llame [**a CSecureChannelClient::Authenticate**](/previous-versions/ms983906(v=msdn.10)) para autenticar la aplicación.
6.  Consulte **IComponentAuthenticate para** la **interfaz IWMDeviceManager.**

Estos pasos se muestran en el siguiente código de C++.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de una Windows de Administrador de dispositivos multimedia**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 