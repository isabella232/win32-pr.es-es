---
description: Una aplicación puede agregar identificadores de seguridad (SID) a un contexto de cliente existente mediante una llamada a la función AuthzAddSidsToContext.
ms.assetid: d49ce47b-e91a-452b-b423-07e8d282d28a
title: Agregar SID a un contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07805031d299efc400c491c7fff1c43653e90b53f6c753c81a8676d4b0941b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784927"
---
# <a name="adding-sids-to-a-client-context"></a>Agregar SID a un contexto de cliente

Una aplicación puede agregar [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) a un contexto de cliente existente mediante una llamada a la función [**AuthzAddSidsToContext.**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) La [**función AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) permite a una aplicación especificar una lista de SID y una lista de SID de restricción al contexto de cliente especificado.

El sistema usa la lista de SID de restricción cuando comprueba el acceso del token a un objeto protegible. Cuando un proceso o subproceso restringido intenta acceder a un objeto protegible, el sistema realiza dos comprobaciones de acceso: una con los SID habilitados del token y otra con la lista de SID de restricción. El acceso solo se concede si ambas comprobaciones de acceso permiten los derechos de acceso solicitados.

Las variables de atributo deben tener el formato de una expresión cuando se usan con operadores lógicos; De lo contrario, se evalúan como desconocidos.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se agrega un SID y un SID de restricción al contexto de cliente creado por el ejemplo de [Inicialización de un contexto de cliente](initializing-a-client-context.md).


```C++
BOOL AddSidsToContext(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{
    AUTHZ_CLIENT_CONTEXT_HANDLE        NewContext = NULL;
    PSID                            pEveryoneSid = NULL;
    PSID                            pLocalSid = NULL;
    SID_AND_ATTRIBUTES                Sids;
    SID_AND_ATTRIBUTES                RestrictedSids;
    DWORD                            SidCount = 0;
    DWORD                            RestrictedSidCount = 0;

    //Create a PSID from the "Everyone" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-1-0", &pEveryoneSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError());
        return FALSE;
    }

    //Create a PSID from the "Local" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-2-0", &pLocalSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError);
        return FALSE;
    }

    //Set the members of the SID_AND_ATTRIBUTES structure to be added.
    Sids.Sid = pEveryoneSid;
    Sids.Attributes = SE_GROUP_ENABLED;

    //Set the members of the SID_AND_ATTRIBUTES structure for the restricting SID.
    RestrictedSids.Sid = pLocalSid;
    RestrictedSids.Attributes = SE_GROUP_ENABLED;

    

    //Create a new context with the new "Everyone" SID and "Local" restricting SID.
    if(!AuthzAddSidsToContext(
        *phClientContext,
        &Sids,
        1,
        &RestrictedSids,
        1,
        &NewContext))
    {
        printf_s("AuthzAddSidsToContext failed with %d\n", GetLastError());
        if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        return FALSE;
    }

    if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        
        AuthzFreeContext(*phClientContext);
        *phClientContext = NewContext;

    return TRUE;

}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Almacenamiento en caché de comprobaciones de acceso](caching-access-checks.md)
</dt> <dt>

[Comprobación del acceso con Authz API](checking-access-with-authz-api.md)
</dt> <dt>

[Inicialización de un contexto de cliente](initializing-a-client-context.md)
</dt> <dt>

[Consulta de un contexto de cliente](querying-a-client-context.md)
</dt> </dl>

 

 
