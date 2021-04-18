---
description: Uso de la caché de credenciales
ms.assetid: b58d0a6e-ecae-48a1-a3af-d4246caa272b
title: Uso de la caché de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d512d0bab8f45f50a587e3c8eda2a73c4832685f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720442"
---
# <a name="using-the-credential-cache"></a><span data-ttu-id="8eb02-103">Uso de la caché de credenciales</span><span class="sxs-lookup"><span data-stu-id="8eb02-103">Using the Credential Cache</span></span>

<span data-ttu-id="8eb02-104">Media Foundation proporciona una implementación predeterminada de la interfaz [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) .</span><span class="sxs-lookup"><span data-stu-id="8eb02-104">Media Foundation provides a default implementation of the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface.</span></span> <span data-ttu-id="8eb02-105">Una aplicación que implementa la interfaz [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) puede usar el objeto de caché de credenciales predeterminado para almacenar las credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="8eb02-105">An application that implements the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface can use the default credential cache object to store the user's credentials.</span></span>

<span data-ttu-id="8eb02-106">Para crear el objeto de caché de credenciales predeterminado, llame a la función [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) .</span><span class="sxs-lookup"><span data-stu-id="8eb02-106">To create the default credential cache object, call the [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) function.</span></span>


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



<span data-ttu-id="8eb02-107">Una vez creada la memoria caché de credenciales, la aplicación puede usar los métodos siguientes para obtener un objeto de credencial, establecer las credenciales de usuario y especificar las opciones de almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="8eb02-107">After the credential cache is created, the application can use the following methods to get a credential object, set user credentials, and specify the caching options.</span></span>

-   <span data-ttu-id="8eb02-108">Para obtener el objeto de credencial para una dirección URL, llame a [**IMFNetCredentialCache:: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span><span class="sxs-lookup"><span data-stu-id="8eb02-108">To get the credential object for a URL, call [**IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span></span>

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    <span data-ttu-id="8eb02-109">Si las credenciales de la dirección URL especificada no existen en la caché de credenciales, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) crea un nuevo objeto de credencial con valores de nombre de usuario y contraseña vacíos.</span><span class="sxs-lookup"><span data-stu-id="8eb02-109">If the credentials for the specified URL do not exist in the credential cache, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) creates a new credential object with empty user name and password values.</span></span>

-   <span data-ttu-id="8eb02-110">Para establecer el nombre de usuario y la contraseña en el objeto de credenciales, llame a [**IMFNetCredential:: SETUSER**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) y [**IMFNetCredential:: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).</span><span class="sxs-lookup"><span data-stu-id="8eb02-110">To set the user name and password on the credential object, call [**IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) and [**IMFNetCredential::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).</span></span>
-   <span data-ttu-id="8eb02-111">Para establecer las opciones de almacenamiento en caché en el objeto de credenciales, llame a [**IMFNetCredentialCache:: SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).</span><span class="sxs-lookup"><span data-stu-id="8eb02-111">To set the caching options on the credential object, call [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).</span></span>

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    <span data-ttu-id="8eb02-112">Los valores de parámetro *dwOptionsFlags* se definen en la enumeración [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) .</span><span class="sxs-lookup"><span data-stu-id="8eb02-112">The *dwOptionsFlags* parameter values are defined in the [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) enumeration.</span></span> <span data-ttu-id="8eb02-113">Para guardar las credenciales de usuario de una dirección URL en un almacenamiento persistente, establezca la marca de guardado de la \_ credencial MFNET \_ .</span><span class="sxs-lookup"><span data-stu-id="8eb02-113">To save user credentials for a URL in a persistent storage, set the MFNET\_CREDENTIAL\_SAVE flag.</span></span> <span data-ttu-id="8eb02-114">Si la llamada a [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) se completa correctamente, la llamada subsiguiente a [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) busca las credenciales en el almacenamiento persistente.</span><span class="sxs-lookup"><span data-stu-id="8eb02-114">If the [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) call completes successfully, then the subsequent call to [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) searches for the credentials in the persistent storage.</span></span> <span data-ttu-id="8eb02-115">Si se encuentra una coincidencia, este método devuelve un puntero al objeto de credencial que contiene la información.</span><span class="sxs-lookup"><span data-stu-id="8eb02-115">If a match is found, this method returns a pointer to the credential object that contains the information.</span></span>

    <span data-ttu-id="8eb02-116">De forma predeterminada, las credenciales de usuario enviadas a través de la red están cifradas.</span><span class="sxs-lookup"><span data-stu-id="8eb02-116">By default, user credentials sent over the network are encrypted.</span></span> <span data-ttu-id="8eb02-117">Para cambiar este valor a texto sin cifrar, establezca la marca MFNET de la \_ credencial \_ permitir \_ texto sin cifrar \_ .</span><span class="sxs-lookup"><span data-stu-id="8eb02-117">To change this to clear text, set the MFNET\_CREDENTIAL\_ALLOW\_CLEAR\_TEXT flag.</span></span>

    <span data-ttu-id="8eb02-118">Para quitar información del registro, llame a [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) para obtener el objeto de credenciales y, a continuación, llame a [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) y establezca *dwOptionsFlags* en MFNET \_ Credential no \_ \_ almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="8eb02-118">To remove information from the registry, call [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) to get the credential object, and then call [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) and set *dwOptionsFlags* to MFNET\_CREDENTIAL\_DONT\_CACHE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8eb02-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8eb02-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eb02-120">Autenticación de origen de red</span><span class="sxs-lookup"><span data-stu-id="8eb02-120">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



