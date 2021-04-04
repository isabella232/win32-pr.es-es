---
title: Ejemplo de creación de una clave de sesión
description: Ejemplo de creación de una clave de sesión
ms.assetid: 4347502b-3900-4306-b58c-16d151200e6c
keywords:
- SDK de Windows Media Format, claves de sesión
- SDK de Windows Media Format, claves de contenido
- SDK de Windows Media Format, código de ejemplo
- SDK de Windows Media Format, ejemplos de código
- Administración de derechos digitales (DRM), claves de sesión
- DRM (administración de derechos digitales), claves de sesión
- Administración de derechos digitales (DRM), claves de contenido
- DRM (administración de derechos digitales), claves de contenido
- Administración de derechos digitales (DRM), código de ejemplo
- DRM (administración de derechos digitales), código de ejemplo
- Administración de derechos digitales (DRM), ejemplos de código
- DRM (administración de derechos digitales), ejemplos de código
- API extendidas del cliente DRM, claves de sesión
- API extendidas del cliente, claves de sesión
- API extendidas del cliente DRM, claves de contenido
- API extendidas del cliente, claves de contenido
- API extendidas del cliente DRM, código de ejemplo
- API extendidas de cliente, código de ejemplo
- API extendidas del cliente DRM, ejemplos de código
- API extendidas de cliente, ejemplos de código
- claves de sesión
- claves de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b757f5d67df0aea1dd70ee45ad2d1b0732040be2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076343"
---
# <a name="create-session-key-example"></a>Ejemplo de creación de una clave de sesión

La clave de sesión se usa para proteger la clave de contenido. El código siguiente muestra cómo crear una clave de sesión, pero deja los detalles de la generación de claves aleatorias.


```C++
HRESULT CreateSessionKey( WMDRM_IMPORT_SESSION_KEY **ppSessionKey, DWORD *pcbSessionKey )
{
    // TODO: Set this value to the desired number of bytes for the session key data. 
    const DWORD SESSION_KEY_DATA_SIZE = 20; 

    HRESULT hr = S_OK;
    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;

    if( NULL == ppSessionKey )
    {
        hr = E_POINTER;
        goto EXIT;
    }
    
    // Compute the size of the session key structure plus the session key.
    DWORD cbSessionKey = sizeof( WMDRM_IMPORT_SESSION_KEY ) + SESSION_KEY_DATA_SIZE;

    // Allocate memory for the session key.
    pSessionKey = (WMDRM_IMPORT_SESSION_KEY *)new BYTE[ cbSessionKey ];
    if( NULL == pSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    ZeroMemory( pSessionKey, cbSessionKey );

    // Set the key type and the key size.
    pSessionKey->dwKeyType = WMDRM_KEYTYPE_RC4;
    pSessionKey->cbKey = SESSION_KEY_DATA_SIZE;
    
    // Set the key to a random value. Note that the random number
    //  generator is not very good. It is only intended to be demonstrative
    //  and it is not recommended for use in shipping code.
    srand((unsigned int)time(NULL));
    BYTE* pKeyData = pSessionKey->rgbKey;
    for (size_t i = 0; i < SESSION_KEY_DATA_SIZE; ++i)
    {
        *pKeyData++ = (BYTE)(rand() & 0xFF); 
    }
    
    // If all has been successful set the parameters.
    *ppSessionKey = pSessionKey;
    pSessionKey = NULL;
    *pcbSessionKey = cbSessionKey;

EXIT:
    
    SAFE_ARRAY_DELETE( pSessionKey );
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplos de importación de DRM**](drm-import-examples.md)
</dt> </dl>

 

 




