---
title: Ejemplo de cifrado de ejemplo de medios
description: Ejemplo de cifrado de ejemplo de medios
ms.assetid: f57f9ffc-47fd-47fb-b553-07b9cd6abb70
keywords:
- Windows SDK de formato multimedia, cifrado de ejemplo multimedia
- Windows SDK de formato multimedia, código de ejemplo
- Windows SDK de formato multimedia, ejemplos de código
- administración de derechos digitales (DRM), cifrado de ejemplo multimedia
- DRM (administración de derechos digitales), cifrado de ejemplo multimedia
- administración de derechos digitales (DRM),código de ejemplo
- DRM (administración de derechos digitales),código de ejemplo
- administración de derechos digitales (DRM),ejemplos de código
- DRM (administración de derechos digitales),ejemplos de código
- API extendidas de cliente DRM, cifrado de ejemplo multimedia
- API extendidas de cliente, cifrado de ejemplo multimedia
- API extendidas de cliente DRM, código de ejemplo
- API extendidas de cliente, código de ejemplo
- API extendidas de cliente DRM, ejemplos de código
- API extendidas de cliente, ejemplos de código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccab97c5a27518d1a31c8c5cdcdbe0defe897bd2bdd47fee1c709a9192262bc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846572"
---
# <a name="media-sample-encryption-example"></a>Ejemplo de cifrado de ejemplo de medios

En el ejemplo incompleto siguiente se muestra cómo cifrar un ejemplo multimedia mediante el cifrado DRM. El algoritmo de cifrado RC4 se ha quedado fuera del ejemplo debido a restricciones de espacio.


```C++
QWORD GetNextSalt(QWORD qwSalt)
{
   return InterlockedIncrement64( (volatile LONGLONG*)&qwSalt );
}

HRESULT EncryptSample( INSSBuffer *pSample )
{
    HRESULT hr = S_OK;
    INSSBuffer3 *pNSSBuffer3 = NULL;
    QWORD qwSalt = 0;
    BYTE *pbData = NULL;
    DWORD cbData = 0;

    hr = pSample->QueryInterface( IID_INSSBuffer3, (void**)&pNSSBuffer3 );
    if( FAILED( hr ) ) goto EXIT;

    hr = pSample->GetBufferAndLength( &pbData, &cbData );
    if( FAILED( hr ) ) goto EXIT;

    qwSalt = GetNextSalt(qwSalt);

    // TODO: Encrypt the sample by concatenating the initialization vector
    //   and using RC4 encryption.

    hr = pNSSBuffer3->SetProperty( 
        WM_SampleExtensionGUID_SampleProtectionSalt, 
        &qwSalt, sizeof( qwSalt ) );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pNSSBuffer3 );
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplos de importación de DRM**](drm-import-examples.md)
</dt> </dl>

 

 




