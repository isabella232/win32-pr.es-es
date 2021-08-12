---
title: Autenticación del proveedor de servicios
description: Autenticación del proveedor de servicios
ms.assetid: e48a8a7c-0277-4f0c-bad2-5bc9d0286da8
keywords:
- Windows Media Administrador de dispositivos,authentication
- Administrador de dispositivos,authentication
- guía de programación, autenticación
- proveedores de servicios, autenticación
- crear proveedores de servicios, autenticación
- autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d6931acb4644d4222659d428be10877deb164a184c95609663a915c12b95d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586495"
---
# <a name="authenticating-the-service-provider"></a>Autenticación del proveedor de servicios

Para que sea accesible desde Windows media Administrador de dispositivos, un proveedor de servicios debe heredar e implementar la [**interfaz IComponentAuthenticate.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)

Para autenticarse, un proveedor de servicios realiza los pasos siguientes:

1.  En la creación de instancias, crea un nuevo objeto [CSecureChannelServer](csecurechannelserver-class.md) global y establece los valores de certificado y clave de su archivo de clave.
2.  Implementa los métodos [**IComponentAuthenticate::SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) e [**IComponentAuthenticate::SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) simplemente pasando los parámetros a su miembro CSecureChannelServer global.
3.  Antes de controlar los métodos implementados de Windows Media Administrador de dispositivos, el proveedor de servicios debe comprobar la autenticación del autor de la llamada llamando a CSecureChannelServer::fIsAuthenticated y con errores si el autor de la llamada no está autenticado.

Estos pasos se muestran en los siguientes ejemplos de C++.

**Creación del objeto CSecureChannelServer**


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



**Implementación de los métodos IComponentAuthenticate**


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



**Comprobación de la autenticación del autor de la llamada**

En el ejemplo de código siguiente se muestra un proveedor de servicios que comprueba la autenticación del autor de la llamada como parte de su implementación de la **interfaz IMDServiceProvider.**


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

 

 




