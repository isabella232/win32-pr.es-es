---
description: Uso de la caché de credenciales
ms.assetid: b58d0a6e-ecae-48a1-a3af-d4246caa272b
title: Uso de la caché de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603078c0dce4c3cd335a3efed57c9d698a372bca6d77e6b76631843be6307eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034583"
---
# <a name="using-the-credential-cache"></a>Uso de la caché de credenciales

Media Foundation proporciona una implementación predeterminada de la [**interfaz IMFNetCredentialCache.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) Una aplicación que implementa la interfaz [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) puede usar el objeto de caché de credenciales predeterminado para almacenar las credenciales del usuario.

Para crear el objeto de caché de credenciales predeterminado, llame a [**la función MFCreateCredentialCache.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache)


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



Una vez creada la caché de credenciales, la aplicación puede usar los métodos siguientes para obtener un objeto de credencial, establecer las credenciales de usuario y especificar las opciones de almacenamiento en caché.

-   Para obtener el objeto de credencial de una dirección URL, llame a [**IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    Si las credenciales de la dirección URL especificada no existen en la caché de credenciales, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) crea un nuevo objeto de credencial con valores de nombre de usuario y contraseña vacíos.

-   Para establecer el nombre de usuario y la contraseña en el objeto de credencial, llame a [**IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) y [**IMFNetCredential::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).
-   Para establecer las opciones de almacenamiento en caché en el objeto de credencial, llame a [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    Los *valores de parámetro dwOptionsFlags* se definen en la [**enumeración MFNetCredentialOptions.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) Para guardar las credenciales de usuario de una dirección URL en un almacenamiento persistente, establezca la marca MFNET \_ CREDENTIAL \_ SAVE. Si la [**llamada a SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) se completa correctamente, la llamada subsiguiente a [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) busca las credenciales en el almacenamiento persistente. Si se encuentra una coincidencia, este método devuelve un puntero al objeto de credencial que contiene la información.

    De forma predeterminada, se cifran las credenciales de usuario enviadas a través de la red. Para cambiar esto a texto no definido, establezca la marca MFNET \_ CREDENTIAL \_ ALLOW CLEAR \_ \_ TEXT.

    Para quitar información del Registro, llame a [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) para obtener el objeto de credencial y, a continuación, llame a [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) y establezca *dwOptionsFlags* en MFNET \_ CREDENTIAL \_ DONT \_ CACHE.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de origen de red](network-source-authentication.md)
</dt> </dl>

 

 



