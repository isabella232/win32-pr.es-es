---
title: Ejemplo de creación de clave de contenido
description: Ejemplo de creación de clave de contenido
ms.assetid: 8e75bac3-d1fb-4a72-8088-fe5ff0899ac2
keywords:
- Windows SDK de formato multimedia, claves de contenido
- Windows SDK de formato multimedia, código de ejemplo
- Windows SDK de formato multimedia, ejemplos de código
- administración de derechos digitales (DRM), claves de contenido
- DRM (administración de derechos digitales), claves de contenido
- digital rights management (DRM), código de ejemplo
- DRM (administración de derechos digitales),código de ejemplo
- administración de derechos digitales (DRM), ejemplos de código
- DRM (administración de derechos digitales), ejemplos de código
- API extendidas de cliente DRM, claves de contenido
- API extendidas de cliente, claves de contenido
- API extendidas de cliente DRM, código de ejemplo
- API extendidas de cliente, código de ejemplo
- API extendidas de cliente DRM, ejemplos de código
- API extendidas de cliente, ejemplos de código
- claves de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881dfd0d318d7d699b44ca9c3f77f22f9acfc689
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256365"
---
# <a name="create-content-key-example"></a>Ejemplo de creación de clave de contenido

La clave de contenido se usa para cifrar ejemplos multimedia para la Windows DRM multimedia. En el ejemplo de código siguiente se muestra cómo crear e inicializar una estructura de clave de contenido.


```C++
HRESULT CreateContentKey( WMDRM_IMPORT_CONTENT_KEY **ppContentKey, DWORD *pcbContentKey)
{
    // TODO: Set this value to the desired number of bytes for the content key data. 
    const DWORD IV_DATA_SIZE = 16;
    HRESULT hr = S_OK;
    WMDRM_IMPORT_CONTENT_KEY *pContentKey = NULL;

    // The content key.
    const BYTE rgbContentKey[] = {
        0x67, 0x39, 0x83, 0xb9,
        0x52, 0xa8, 0xe3
    };        
    const DWORD CONTENT_KEY_DATA_SIZE = sizeof(rgbContentKey);

    // Compute the total size of the content key structure
    DWORD cbContentKey = sizeof( WMDRM_IMPORT_CONTENT_KEY ) +
      IV_DATA_SIZE + CONTENT_KEY_DATA_SIZE;

    // Make sure we have a valid 
    if( NULL == ppContentKey )
    {
        hr = E_POINTER;
        goto EXIT;
    }

    // Allocate the content key, locally first
    pContentKey = (WMDRM_IMPORT_CONTENT_KEY *)new BYTE[ cbContentKey ];
    
    // Check the allocation was successful 
    if( NULL == pContentKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }

    // Ininitalize the key
    ZeroMemory( pContentKey, cbContentKey );
    pContentKey->dwVersion = 0;
    pContentKey->cbStructSize = cbContentKey;

    // Set the initialization vector key type 
    pContentKey->dwIVKeyType = WMDRM_KEYTYPE_RC4;
    pContentKey->cbIVKey = IV_DATA_SIZE;
    
    // Generate a random initialization vector. Note that this random number
    //  generator is not very good. It is only intended to be demonstrative
    //  and it is not recommended for use in commercial strength code.
    srand((unsigned int)time(NULL));
    BYTE* pKeyData = pContentKey->rgbKeyData;
    for (size_t i = 0; i < IV_DATA_SIZE; ++i)
    {
        *pKeyData++ = (BYTE)(rand() & 0xFF); 
    }   
    
    // Set the content key type.
    pContentKey->dwContentKeyType = WMDRM_KEYTYPE_COCKTAIL;
    pContentKey->cbContentKey = CONTENT_KEY_DATA_SIZE;

    // Fill out the content key. 
    for (size_t i = 0; i < CONTENT_KEY_DATA_SIZE; ++i)
    {
        *pKeyData++ = rgbContentKey[i]; 
    }   
    

    // If all has been successful, set the parameters
    *ppContentKey = pContentKey;
    pContentKey = NULL;
    *pcbContentKey = cbContentKey;

EXIT:
    SAFE_ARRAY_DELETE( pContentKey );
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplos de importación de DRM**](drm-import-examples.md)
</dt> </dl>

 

 




