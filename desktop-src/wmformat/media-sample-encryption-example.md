---
title: Ejemplo de cifrado de ejemplo multimedia
description: Ejemplo de cifrado de ejemplo multimedia
ms.assetid: f57f9ffc-47fd-47fb-b553-07b9cd6abb70
keywords:
- SDK de formato de Windows Media, cifrado de ejemplo multimedia
- SDK de Windows Media Format, código de ejemplo
- SDK de Windows Media Format, ejemplos de código
- Administración de derechos digitales (DRM), cifrado de ejemplo multimedia
- DRM (administración de derechos digitales), cifrado de ejemplo multimedia
- Administración de derechos digitales (DRM), código de ejemplo
- DRM (administración de derechos digitales), código de ejemplo
- Administración de derechos digitales (DRM), ejemplos de código
- DRM (administración de derechos digitales), ejemplos de código
- API extendidas del cliente DRM, cifrado de ejemplo multimedia
- API extendidas de cliente, cifrado de ejemplo multimedia
- API extendidas del cliente DRM, código de ejemplo
- API extendidas de cliente, código de ejemplo
- API extendidas del cliente DRM, ejemplos de código
- API extendidas de cliente, ejemplos de código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a669ab957aa7510cdd57daca798ec3e3ac3bf73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076318"
---
# <a name="media-sample-encryption-example"></a>Ejemplo de cifrado de ejemplo multimedia

En el siguiente ejemplo incompleto se muestra cómo cifrar un ejemplo multimedia mediante el cifrado DRM. El algoritmo de cifrado RC4 se ha omitido del ejemplo debido a restricciones de espacio.


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

 

 




