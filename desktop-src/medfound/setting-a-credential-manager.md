---
description: Establecer un administrador de credenciales
ms.assetid: a20c2e6c-e9d9-438f-a57a-e3080587c11c
title: Establecer un administrador de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c98d9d9572438a63f93f916a0084f8a33a7bca5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715491"
---
# <a name="setting-a-credential-manager"></a><span data-ttu-id="4b29e-103">Establecer un administrador de credenciales</span><span class="sxs-lookup"><span data-stu-id="4b29e-103">Setting a Credential Manager</span></span>

<span data-ttu-id="4b29e-104">Una aplicación que proporciona credenciales para el origen de red debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4b29e-104">An application that provides credentials to the network source must do the following:</span></span>

1.  <span data-ttu-id="4b29e-105">Implemente un objeto de administrador de credenciales que exponga la interfaz [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="4b29e-105">Implement a credential manager object that exposes the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
2.  <span data-ttu-id="4b29e-106">Antes de crear el origen de red, cree un nuevo almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4b29e-106">Before you create the network source, create a new property store.</span></span>
3.  <span data-ttu-id="4b29e-107">Establezca la [**propiedad \_ \_ Administrador de credenciales de MFNETSOURCE**](mfnetsource-credential-manager-property.md) en el almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4b29e-107">Set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the property store.</span></span> <span data-ttu-id="4b29e-108">El valor de la propiedad es un puntero a la interfaz [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="4b29e-108">The value of the property is a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
4.  <span data-ttu-id="4b29e-109">Pase un puntero al almacén de propiedades para la resolución de origen, tal y como se describe en [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="4b29e-109">Pass a pointer to the property store to the source resolver, as described in [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="4b29e-110">Los orígenes de red usan el administrador de credenciales para obtener las credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="4b29e-110">The network sources uses the credential manager to get user credentials.</span></span> <span data-ttu-id="4b29e-111">Si el origen de red requiere credenciales para tener acceso a un recurso de red, llama al método [**IMFNetCredentialManager:: BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b29e-111">If the network source requires credentials to access a network resource, it calls the application's [**IMFNetCredentialManager::BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method.</span></span> <span data-ttu-id="4b29e-112">Esta llamada inicia una solicitud asincrónica para obtener las credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="4b29e-112">This call starts an asynchronous request to gets the user's credentials.</span></span> <span data-ttu-id="4b29e-113">El método **BeginGetCredentials** puede obtener las credenciales de la memoria caché de credenciales o del usuario.</span><span class="sxs-lookup"><span data-stu-id="4b29e-113">The **BeginGetCredentials** method can get the credentials either from the credential cache or from the user.</span></span> <span data-ttu-id="4b29e-114">Las credenciales se almacenan en un *objeto Credential*.</span><span class="sxs-lookup"><span data-stu-id="4b29e-114">Credentials are stored in a *credential object*.</span></span> <span data-ttu-id="4b29e-115">Una vez completada la operación, la aplicación invoca la interfaz de devolución de llamada para notificar al origen de red.</span><span class="sxs-lookup"><span data-stu-id="4b29e-115">When the operation is complete, the application invokes the callback interface to notify the network source.</span></span> <span data-ttu-id="4b29e-116">El origen de red llama a [**IMFNetCredentialManager:: EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) para completar la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="4b29e-116">The network source calls [**IMFNetCredentialManager::EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) to complete the asynchronous operation.</span></span>

<span data-ttu-id="4b29e-117">Dado que se trata de una operación asincrónica, la aplicación debe enviar la devolución de llamada al final de la operación.</span><span class="sxs-lookup"><span data-stu-id="4b29e-117">Because this is an asynchronous operation, the application must dispatch the callback at the end of the operation.</span></span> <span data-ttu-id="4b29e-118">Para obtener instrucciones paso a paso sobre cómo escribir un método asincrónico, consulte [escribir un método asincrónico](writing-an-asynchronous-method.md).</span><span class="sxs-lookup"><span data-stu-id="4b29e-118">For step-by-step instructions about writing an asynchronous method, see [Writing an Asynchronous Method](writing-an-asynchronous-method.md).</span></span>

<span data-ttu-id="4b29e-119">En el ejemplo siguiente se muestra cómo establecer la propiedad del [**\_ \_ Administrador de credenciales de MFNETSOURCE**](mfnetsource-credential-manager-property.md) en el origen de red.</span><span class="sxs-lookup"><span data-stu-id="4b29e-119">The following example shows how to set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the network source.</span></span>


```C++
// Creates a media source from a URL.
//
// Demonstrates how to set a credential manager on the network source.

HRESULT CreateMediaSourceWithCredentialManager(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CCredentialManager *pCredentials = new (std::nothrow) CCredentialManager();

    if (pCredentials == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_CREDENTIAL_MANAGER;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pCredentials->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(key, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pCredentials);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4b29e-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4b29e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b29e-121">Autenticación de origen de red</span><span class="sxs-lookup"><span data-stu-id="4b29e-121">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



