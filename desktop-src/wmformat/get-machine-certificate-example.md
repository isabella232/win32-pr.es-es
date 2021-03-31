---
title: Obtener ejemplo de certificado de equipo
description: Obtener ejemplo de certificado de equipo
ms.assetid: 4112e29e-7c86-4825-9798-dd1a81b82083
keywords:
- SDK de Windows Media Format, certificados de equipo
- SDK de Windows Media Format, certificados
- SDK de Windows Media Format, código de ejemplo
- SDK de Windows Media Format, ejemplos de código
- Administración de derechos digitales (DRM), certificados de equipo
- DRM (administración de derechos digitales), certificados de equipo
- Administración de derechos digitales (DRM), certificados
- DRM (administración de derechos digitales), certificados
- Administración de derechos digitales (DRM), código de ejemplo
- DRM (administración de derechos digitales), código de ejemplo
- Administración de derechos digitales (DRM), ejemplos de código
- DRM (administración de derechos digitales), ejemplos de código
- API extendidas del cliente DRM, certificados de equipo
- API extendidas de cliente, certificados de equipo
- API extendidas del cliente DRM, certificados
- API extendidas del cliente, certificados
- API extendidas del cliente DRM, código de ejemplo
- API extendidas de cliente, código de ejemplo
- API extendidas del cliente DRM, ejemplos de código
- API extendidas de cliente, ejemplos de código
- certificados, ejemplos de código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e68a8ecbaf3e3c0ba8001a7a2094ab2b4a7e09a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419015"
---
# <a name="get-machine-certificate-example"></a>Obtener ejemplo de certificado de equipo

En el ejemplo siguiente se muestra cómo recuperar la colección de certificados de equipo:


```C++
HRESULT GetMachineCert( BYTE **ppbCert, DWORD *pcbCert )
{
    HRESULT hr = S_OK;
    IWMDRMProvider *pProvider = NULL;
    IWMDRMSecurity *pSecurity = NULL;
    BYTE rgbVersion[4];

    // Create a provider object.
    hr = WMDRMCreateProvider( &pProvider );
    if( FAILED( hr ) ) goto EXIT;

    // Create a security object from a provider object.
    hr = pProvider->CreateObject( IID_IWMDRMSecurity, (void**) &pSecurity );
    if( FAILED( hr ) ) goto EXIT;

    // Query the security to get the machine certificate.
    hr = pSecurity->GetMachineCertificate( WMDRM_CERTIFICATE_TYPE_V2,
        rgbVersion, ppbCert, pcbCert );

    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pSecurity );
    SAFE_RELEASE( pProvider );

    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplos de importación de DRM**](drm-import-examples.md)
</dt> </dl>

 

 




