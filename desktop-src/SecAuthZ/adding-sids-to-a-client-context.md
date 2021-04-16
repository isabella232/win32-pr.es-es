---
description: Una aplicación puede agregar identificadores de seguridad (SID) a un contexto de cliente existente llamando a la función AuthzAddSidsToContext.
ms.assetid: d49ce47b-e91a-452b-b423-07e8d282d28a
title: Agregar SID a un contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a601f485110ddacea0fdb54cb7dcef587a25cb9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546331"
---
# <a name="adding-sids-to-a-client-context"></a>Agregar SID a un contexto de cliente

Una aplicación puede agregar [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) a un contexto de cliente existente llamando a la función [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) . La función [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) permite a una aplicación especificar una lista de SID y una lista de restricciones de SID para el contexto de cliente especificado.

El sistema utiliza la lista de restricciones de SID cuando comprueba el acceso del token a un objeto protegible. Cuando un proceso o subproceso restringido intenta tener acceso a un objeto protegible, el sistema realiza dos comprobaciones de acceso: una con los SID habilitados del token y otra mediante la lista de SID restrictivos. El acceso se concede solo si ambas comprobaciones de acceso permiten los derechos de acceso solicitados.

Las variables de atributo deben tener el formato de una expresión cuando se utilizan con operadores lógicos; de lo contrario, se evalúan como Unknown.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se agrega un SID y un SID restrictivo al contexto del cliente creado por el ejemplo en la [inicialización de un contexto de cliente](initializing-a-client-context.md).


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

[Almacenar en caché comprobaciones de acceso](caching-access-checks.md)
</dt> <dt>

[Comprobación del acceso con la API de authz](checking-access-with-authz-api.md)
</dt> <dt>

[Inicializar un contexto de cliente](initializing-a-client-context.md)
</dt> <dt>

[Consultar un contexto de cliente](querying-a-client-context.md)
</dt> </dl>

 

 
