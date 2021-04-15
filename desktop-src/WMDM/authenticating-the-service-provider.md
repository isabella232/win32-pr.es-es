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
# <a name="authenticating-the-service-provider"></a>Autenticación del proveedor de servicios

Para ser accesible desde Windows Media Administrador de dispositivos, un proveedor de servicios debe heredar e implementar la interfaz [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .

Para autenticarse, un proveedor de servicios realiza los siguientes pasos:

1.  Al crear una instancia, se crea un nuevo objeto [CSecureChannelServer](csecurechannelserver-class.md) global y se establecen los valores de certificado y clave a partir de su archivo de clave.
2.  Implementa los métodos [**IComponentAuthenticate:: SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) y [**IComponentAuthenticate:: SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) simplemente pasando los parámetros a su miembro global CSecureChannelServer.
3.  Antes de controlar los métodos de Administrador de dispositivos de Windows Media implementados, el proveedor de servicios debe comprobar la autenticación del llamador llamando a CSecureChannelServer:: fIsAuthenticated y generar un error si el autor de la llamada no está autenticado.

Estos pasos se muestran en los siguientes ejemplos de C++.

**Crear el objeto CSecureChannelServer**


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



**Implementar los métodos IComponentAuthenticate**


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



**Comprobando la autenticación del llamador**

En el ejemplo de código siguiente se muestra un proveedor de servicios que comprueba la autenticación del autor de la llamada como parte de su implementación de la interfaz **IMDServiceProvider** .


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> </dl>

 

 




