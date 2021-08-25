---
description: Una aplicación debe crear un contexto de cliente para poder usar Authz API para realizar comprobaciones de acceso o auditoría.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Inicializar un contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da8a3c3191f323cf6ce35fda90f4bd75299dac67183986998cf21a80c0ee6995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908045"
---
# <a name="initializing-a-client-context"></a>Inicializar un contexto de cliente

Una aplicación debe crear un contexto de cliente para poder usar Authz API para realizar comprobaciones de acceso o auditoría.

Una aplicación debe llamar a la [**función AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) para inicializar el administrador de recursos. A continuación, la aplicación puede llamar a una de varias funciones para crear un contexto de cliente. Además, si realiza comprobaciones de acceso o auditoría de forma remota, debe usar la función [**AuthzInitializeRemoteResourceManager.**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)

Para crear un contexto de cliente basado en un contexto de cliente existente, llame a la función [**AuthzInitializeContextFromAuthzContext.**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)

La [**función AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) crea un nuevo contexto de cliente mediante la información de un token de inicio de sesión. La [**función AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) crea un nuevo contexto de cliente mediante el [**SID especificado.**](/windows/desktop/api/Winnt/ns-winnt-sid)

Si es posible, llame a [**la función AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) en lugar de [**a AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid). **AuthzInitializeContextFromSid** intenta recuperar la información disponible en un token de inicio de sesión si el cliente hubiera iniciado sesión realmente. Un token de inicio de sesión real proporciona más información, como el tipo de inicio de sesión y las propiedades de inicio de sesión, y refleja el comportamiento del paquete de autenticación utilizado para el inicio de sesión. El contexto de cliente creado por **AuthzInitializeContextFromToken** usa un token de inicio de sesión y el contexto de cliente resultante es más completo y preciso que un contexto de cliente creado por **AuthzInitializeContextFromSid.**

> [!Note]  
> Las variables de atributo de seguridad deben estar presentes en el contexto de cliente si se hace referencia a en una expresión condicional; De lo contrario, el término de expresión condicional que hace referencia a ellos se evaluará como desconocido. Para obtener más información sobre las expresiones condicionales, vea el tema Lenguaje de definición de descriptores de seguridad [para ASE condicionales.](security-descriptor-definition-language-for-conditional-aces-.md)

 

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se inicializa el administrador de recursos de Authz y se llama a la función [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) para crear un contexto de cliente a partir del token de inicio de sesión asociado al proceso actual.


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

[Almacenamiento en caché de comprobaciones de acceso](caching-access-checks.md)
</dt> <dt>

[Comprobación del acceso con Authz API](checking-access-with-authz-api.md)
</dt> <dt>

[Funcionamiento de AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[Consulta de un contexto de cliente](querying-a-client-context.md)
</dt> <dt>

[Lenguaje de definición de descriptor de seguridad para AEE condicionales](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



