---
description: La API de Identity Manager le permite crear una identidad del mismo nivel para usarla en una red del mismo nivel.
ms.assetid: 44b85bbc-9594-4f68-b930-51a28422b571
title: Crear una identidad del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab240b9fa1265ba03bfb1ce584dabed92988620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002003"
---
# <a name="creating-a-peer-identity"></a><span data-ttu-id="71ca8-103">Crear una identidad del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="71ca8-103">Creating a Peer Identity</span></span>

<span data-ttu-id="71ca8-104">La API de Identity Manager le permite crear una identidad del mismo nivel para usarla en una red del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="71ca8-104">The Identity Manager API allows you to create a peer identity to use in a peer network.</span></span>

<span data-ttu-id="71ca8-105">Al crear una identidad del mismo nivel, puede proporcionar la siguiente información opcional:</span><span class="sxs-lookup"><span data-stu-id="71ca8-105">When you create a peer identity, you can provide the following optional information:</span></span>

-   [<span data-ttu-id="71ca8-106">Clasificador</span><span class="sxs-lookup"><span data-stu-id="71ca8-106">Classifier</span></span>](peer-names.md)
-   <span data-ttu-id="71ca8-107">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="71ca8-107">Friendly name</span></span>
-   <span data-ttu-id="71ca8-108">Proveedor de servicios de cifrado</span><span class="sxs-lookup"><span data-stu-id="71ca8-108">Cryptographic service provider</span></span>

> [!Note]  
> <span data-ttu-id="71ca8-109">Siempre que sea posible, vuelva a usar una identidad del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="71ca8-109">Whenever possible, re-use a peer identity.</span></span>

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a><span data-ttu-id="71ca8-110">Ejemplo de creación y eliminación de una identidad del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="71ca8-110">Example of Creating and Deleting a Peer Identity</span></span>

<span data-ttu-id="71ca8-111">En el siguiente fragmento de código se muestra cómo crear y eliminar una identidad del mismo nivel mediante un clasificador y un nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="71ca8-111">The following code snippet shows you how to create and delete a peer identity by using a classifier and friendly name.</span></span>


```C++
#define UNICODE
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: CreateIdentity
//
// Purpose:  Creates a new Identity.
//
// Returns:  HRESULT
//
HRESULT CreateIdentity(PWSTR pwzFriendlyName)
{
    HRESULT     hr              = S_OK;   
    PWSTR       pwzClassifier   = L"GroupMember";
    PWSTR       pwzIdentity     = NULL;

    hr = PeerIdentityCreate(pwzClassifier, pwzFriendlyName, 0, &pwzIdentity);
    if (FAILED(hr))
    {            
        printf("Failed to create identity.");
    }
    else
    {
        printf("Identity: %s", pwzFriendlyName);
    }
       
    PeerFreeData(pwzIdentity);    

    return hr;
}


//-----------------------------------------------------------------------------
// Function: DeleteIdentity
//
// Purpose:  Delete the identity created by CreateIdentity
//
// Returns:  HRESULT
//
HRESULT DeleteIdentity()
{
    HRESULT hr = S_OK;

    if (g_pwzIdentity)
    {
        hr = PeerIdentityDelete(g_pwzIdentity);
        g_pwzIdentity = NULL;
    }

    return hr;
}
```



 

 



