---
title: Ejemplo de inicialización de importación de DRM
description: Ejemplo de inicialización de importación de DRM
ms.assetid: 46a64305-9aac-47df-992d-6aea8ecb54bf
keywords:
- Windows SDK de formato multimedia, importación de DRM
- Windows SDK de formato multimedia, importación
- Windows SDK de formato multimedia, código de ejemplo
- Windows SDK de formato multimedia, ejemplos de código
- digital rights management (DRM),import
- DRM (administración de derechos digitales),importar
- administración de derechos digitales (DRM), inicializar la importación
- DRM (administración de derechos digitales), inicializar la importación
- digital rights management (DRM), código de ejemplo
- DRM (administración de derechos digitales),código de ejemplo
- administración de derechos digitales (DRM), ejemplos de código
- DRM (administración de derechos digitales), ejemplos de código
- API extendidas de cliente DRM, inicializar importación
- API extendidas de cliente, inicializar importación
- API extendidas de cliente DRM, importar
- API extendidas de cliente, importar
- API extendidas de cliente DRM, código de ejemplo
- API extendidas de cliente, código de ejemplo
- API extendidas de cliente DRM, ejemplos de código
- API extendidas de cliente, ejemplos de código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e91d0aac6e9d54dac4cd52de7d84140a9e6af580084bd22ccc0af7283900d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702126"
---
# <a name="initialize-drm-import-example"></a>Ejemplo de inicialización de importación de DRM

En el ejemplo de código siguiente se muestra cómo inicializar un objeto de escritor DRM para la importación de DRM:


```C++
HRESULT InitializeImport( IWMDRMWriter3 *pDRMWriter )
{
    // Set this value to the desired number of bytes in an encrypted 
    //  session key.
    const int MODULUS_SIZE = 32;

    HRESULT hr = S_OK;
    WMDRM_IMPORT_INIT_STRUCT ImportInit;

    BYTE *pbEncryptedSessionKey = NULL;
    DWORD cbEncryptedSessionKey = 0;

    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;
    DWORD cbSessionKey = 0;

    WMDRM_IMPORT_CONTENT_KEY *pContentKey = NULL;
    DWORD cbContentKey = 0;
        
    // Allocate memory for the encrypted session key.
    pbEncryptedSessionKey = new BYTE[ MODULUS_SIZE ];
    if( NULL == pbEncryptedSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    cbEncryptedSessionKey = MODULUS_SIZE;

    hr = CreateSessionKey( &pSessionKey, &cbSessionKey );
    if( FAILED( hr ) ) goto EXIT;

    if( cbSessionKey > MODULUS_SIZE )
    if( FAILED( hr ) ) goto EXIT;

    hr = CreateContentKey( &pContentKey, &cbContentKey );
    if( FAILED( hr ) ) goto EXIT;

    // TODO: Encrypt the content key with the session Key.    
    // TODO: Encrypt the session key with the machine certificate public key.   

    ImportInit.dwVersion = 0;
    ImportInit.pbEncryptedSessionKeyMessage = pbEncryptedSessionKey;
    ImportInit.cbEncryptedSessionKeyMessage = cbEncryptedSessionKey;
    ImportInit.pbEncryptedKeyMessage = (BYTE*)pContentKey;
    ImportInit.cbEncryptedKeyMessage = cbContentKey;

    hr = pDRMWriter->SetProtectStreamSamples( &ImportInit );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_ARRAY_DELETE( pContentKey );
    SAFE_ARRAY_DELETE( pSessionKey );

    return( hr );
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplo de creación de clave de contenido**](create-content-key-example.md)
</dt> <dt>

[**Ejemplo de creación de clave de sesión**](create-session-key-example.md)
</dt> <dt>

[**Ejemplos de importación de DRM**](drm-import-examples.md)
</dt> </dl>

 

 




