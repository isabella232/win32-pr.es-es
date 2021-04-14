---
description: Una aplicación debe crear un contexto de cliente para poder usar la API de authz para realizar comprobaciones de acceso o auditoría.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Inicializar un contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be229a60a12e33ab0c2bbd3e52fc533cf29ed1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668398"
---
# <a name="initializing-a-client-context"></a>Inicializar un contexto de cliente

Una aplicación debe crear un contexto de cliente para poder usar la API de authz para realizar comprobaciones de acceso o auditoría.

Una aplicación debe llamar a la función [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) para inicializar el administrador de recursos. A continuación, la aplicación puede llamar a una de varias funciones para crear un contexto de cliente. Además, si está realizando comprobaciones de acceso o auditorías de forma remota, debe usar la función [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) .

Para crear un contexto de cliente basado en un contexto de cliente existente, llame a la función [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) .

La función [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) crea un nuevo contexto de cliente usando información en un token de inicio de sesión. La función [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) crea un nuevo contexto de cliente mediante el [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid)especificado.

Si es posible, llame a la función [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) en lugar de a [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid). **AuthzInitializeContextFromSid** intenta recuperar la información disponible en un token de inicio de sesión en el que el cliente ha iniciado sesión realmente. Un token de inicio de sesión real proporciona más información, como el tipo de inicio de sesión y las propiedades de inicio de sesión, y refleja el comportamiento del paquete de autenticación usado para el inicio de sesión. El contexto de cliente creado por **AuthzInitializeContextFromToken** utiliza un token de inicio de sesión y el contexto de cliente resultante es más completo y preciso que un contexto de cliente creado por **AuthzInitializeContextFromSid**.

> [!Note]  
> Las variables de atributo de seguridad deben estar presentes en el contexto del cliente si se hace referencia a ellas en una expresión condicional; de lo contrario, el término de expresión condicional que hace referencia a ellos se evaluará como desconocido. Para obtener más información sobre las expresiones condicionales, vea el tema [lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md) .

 

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se inicializa el administrador de recursos de authz y se llama a la función [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) para crear un contexto de cliente a partir del token de inicio de sesión asociado al proceso actual.


```C++
BOOL AuthzInitFromToken(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{

    HANDLE                            hToken = NULL;
    LUID                            Luid = {0, 0};

    
    ULONG                            uFlags = 0;


    //Initialize Resource Manager
    if(!AuthzInitializeResourceManager(
        AUTHZ_RM_FLAG_NO_AUDIT,
        NULL,
        NULL,
        NULL,
        L"My Resource Manager",
        &g_hResourceManager
        ))
    {
        printf_s("AuthzInitializeResourceManager failed with %d\n", GetLastError);
        return FALSE;
    }
    

    //Get the current token.

    if(!OpenProcessToken(GetCurrentProcess(), TOKEN_ALL_ACCESS, &hToken))
    {
        printf_s("OpenProcessToken failed with %d\n", GetLastError);
        return FALSE;
    }


    //Initialize the client context

    if(!AuthzInitializeContextFromToken(
        0,
        hToken,
        g_hResourceManager,
        NULL,
        Luid,
        NULL,
        phClientContext
        ))
    {    
        printf_s("AuthzInitializeContextFromToken failed with %d\n", GetLastError);
        return FALSE;
    }

    
    printf_s("Initialized client context. \n");
    return TRUE;

}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agregar SID a un contexto de cliente](adding-sids-to-a-client-context.md)
</dt> <dt>

[Almacenar en caché comprobaciones de acceso](caching-access-checks.md)
</dt> <dt>

[Comprobación del acceso con la API de authz](checking-access-with-authz-api.md)
</dt> <dt>

[Cómo funciona AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[Consultar un contexto de cliente](querying-a-client-context.md)
</dt> <dt>

[Lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



