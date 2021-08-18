---
title: Ejemplo de obtener certificado de máquina
description: Ejemplo de obtener certificado de máquina
ms.assetid: 4112e29e-7c86-4825-9798-dd1a81b82083
keywords:
- Windows SDK de formato multimedia, certificados de máquina
- Windows SDK de formato multimedia, certificados
- Windows SDK de formato multimedia, código de ejemplo
- Windows SDK de formato multimedia, ejemplos de código
- administración de derechos digitales (DRM), certificados de máquina
- DRM (administración de derechos digitales), certificados de máquina
- administración de derechos digitales (DRM), certificados
- DRM (administración de derechos digitales), certificados
- digital rights management (DRM), código de ejemplo
- DRM (administración de derechos digitales),código de ejemplo
- administración de derechos digitales (DRM), ejemplos de código
- DRM (administración de derechos digitales), ejemplos de código
- API extendidas de cliente DRM, certificados de máquina
- API extendidas de cliente, certificados de máquina
- API extendidas de cliente DRM, certificados
- API extendidas de cliente, certificados
- API extendidas de cliente DRM, código de ejemplo
- API extendidas de cliente, código de ejemplo
- API extendidas de cliente DRM, ejemplos de código
- API extendidas de cliente, ejemplos de código
- certificates,code examples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855479e90095f204a3ba7abafadcb4a31bbcaeaf7c592221ab0d5906cb1d8b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964014"
---
# <a name="get-machine-certificate-example"></a>Ejemplo de obtener certificado de máquina

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

 

 




