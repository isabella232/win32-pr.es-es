---
description: La API de Identity Manager permite crear una identidad del mismo nivel para usarla en una red del mismo nivel.
ms.assetid: 44b85bbc-9594-4f68-b930-51a28422b571
title: Creación de una identidad del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d7e2a1bfba386ede4bf3f10e8b009794c3e17676abc65d797d42e203f214f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887825"
---
# <a name="creating-a-peer-identity"></a>Creación de una identidad del mismo nivel

La API de Identity Manager permite crear una identidad del mismo nivel para usarla en una red del mismo nivel.

Al crear una identidad del mismo nivel, puede proporcionar la siguiente información opcional:

-   [Clasificador](peer-names.md)
-   Nombre descriptivo
-   Proveedor de servicios criptográficos

> [!Note]  
> Siempre que sea posible, vuelva a usar una identidad del mismo nivel.

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a>Ejemplo de creación y eliminación de una identidad del mismo nivel

El fragmento de código siguiente muestra cómo crear y eliminar una identidad del mismo nivel mediante un clasificador y un nombre descriptivo.


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



 

 



