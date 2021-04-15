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
# <a name="authenticating-the-application"></a>Autenticación de la aplicación

El primer paso que debe realizar la aplicación es la autenticación. La autenticación comprueba la identidad de la aplicación para Windows Media Administrador de dispositivos. Después de autenticar la aplicación, puede llamar a **QueryInterface** para obtener la interfaz raíz [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) , que se puede consultar para otras interfaces necesarias, que se pueden consultar a sí mismas para todas las demás interfaces. La autenticación solo debe realizarse una vez, en el inicio.

Para autenticar la aplicación, siga estos pasos:

1.  Cocree el objeto **MediaDevMgr** (ID. de clase MediaDevMgr) y solicite una interfaz [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .
2.  Cree un objeto [CSecureChannelClient](csecurechannelclient-class.md) para controlar la autenticación.
3.  Pase la clave de aplicación y transfiera el certificado al objeto de canal seguro. Puede usar la clave o el certificado ficticios que se muestran en el siguiente código de ejemplo para obtener la funcionalidad básica de las funciones del SDK. Sin embargo, para obtener toda la funcionalidad (importante para pasar archivos hacia y desde el dispositivo), debe solicitar una clave y un certificado de Microsoft, tal y como se describe en [herramientas de desarrollo](tools-for-development.md).
4.  Pase la interfaz **IComponentAuthenticate** que creó en el paso 1 al objeto de canal seguro.
5.  Llame a [**CSecureChannelClient:: Authenticate**](/previous-versions/ms983906(v=msdn.10)) para autenticar la aplicación.
6.  Consulte **IComponentAuthenticate** de la interfaz **IWMDeviceManager** .

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

[**Crear una aplicación de Windows Media Administrador de dispositivos**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 