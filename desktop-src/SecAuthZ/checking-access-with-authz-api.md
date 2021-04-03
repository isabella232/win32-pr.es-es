---
description: Las aplicaciones determinan si se debe conceder acceso a los objetos protegibles mediante una llamada a la función AuthzAccessCheck.
ms.assetid: dad0a102-08ed-4cd2-bef5-87bc48fc7fc2
title: Comprobación del acceso con la API de authz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e129b690a7c1f701b5f669a8f0705c5a5e9a2eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908091"
---
# <a name="checking-access-with-authz-api"></a>Comprobación del acceso con la API de authz

Las aplicaciones determinan si se debe conceder acceso a los objetos protegibles mediante una llamada a la función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .

La función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) toma las estructuras de [**\_ \_ solicitud de acceso**](/windows/desktop/api/Authz/ns-authz-authz_access_request) y [**\_ descriptor de seguridad**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) de AUTHZ como parámetros. La estructura de **\_ \_ solicitud de acceso de AUTHZ** especifica un nivel de acceso solicitado. La función **AuthzAccessCheck** evalúa el acceso solicitado con el **\_ descriptor de seguridad** especificado para un contexto de cliente especificado. Para obtener información sobre cómo un descriptor de seguridad controla el acceso a un objeto, vea [Cómo controlan el acceso a un objeto las DACL](how-dacls-control-access-to-an-object.md).

Las variables de atributo deben tener el formato de una expresión cuando se utilizan con operadores lógicos; de lo contrario, se evalúan como Unknown.

## <a name="callback-function"></a>Función de devolución de llamada

Si la [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) del [**\_ descriptor de seguridad**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) del objeto que se va a comprobar contiene las [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) de devolución de llamada, [**AUTHZACCESSCHECK**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) llama a la función [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) para cada ACE de devolución de llamada contenida en la DACL. Una ACE de devolución de llamada es cualquier estructura ACE cuyo tipo ACE contenga la palabra "callback". La función **AuthzAccessCheckCallback** es una función definida por la aplicación que se debe registrar cuando se inicializa el administrador de recursos mediante una llamada a la función [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) .

Una función de devolución de llamada permite a una aplicación definir la lógica de negocios que se va a evaluar en tiempo de ejecución. Cuando se llama a la función [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) , se pasa la ACE de devolución de llamada que causó la llamada a la función de devolución de llamada para su evaluación. Si la lógica definida por la aplicación se evalúa como **true**, la ACE de devolución de llamada se incluye en la comprobación de acceso. De lo contrario, se omite.

## <a name="caching-access-results"></a>Almacenar en caché los resultados de acceso

Los resultados de una comprobación de acceso se pueden almacenar en caché y usar en futuras llamadas a la función [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) . Para obtener más información sobre las comprobaciones de acceso de almacenamiento en caché, incluido un ejemplo, vea [caching Access Checks](caching-access-checks.md).

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se crea un [**\_ descriptor de seguridad**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) que permite el acceso de **\_ control de lectura** a los administradores integrados. Usa ese descriptor de seguridad para comprobar el acceso del cliente especificado por el contexto de cliente creado en el ejemplo de [inicializar un contexto de cliente](initializing-a-client-context.md).


```C++
BOOL CheckAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR    pSecurityDescriptor = NULL;
    ULONG                    cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST    Request;
    CHAR                    ReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY        pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    DWORD                    AuthzError =0;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

    //Create security descriptor.
    if(!ConvertStringSecurityDescriptorToSecurityDescriptor(
        L"O:LAG:BAD:(A;;RC;;;BA)",
        SDDL_REVISION_1,
        &pSecurityDescriptor,
        NULL))
    {
        printf_s("ConvertStringSecurityDescriptorToSecurityDescriptor failed with %d\n", GetLastError()); 
        return FALSE;
    }

    //Call AuthzAccessCheck.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        NULL))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
    
        return FALSE;
    }


    //Print results.
    if(*pReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }

  LocalFree(pSecurityDescriptor);
    return TRUE;

}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agregar SID a un contexto de cliente](adding-sids-to-a-client-context.md)
</dt> <dt>

[Almacenar en caché comprobaciones de acceso](caching-access-checks.md)
</dt> <dt>

[Inicializar un contexto de cliente](initializing-a-client-context.md)
</dt> <dt>

[Consultar un contexto de cliente](querying-a-client-context.md)
</dt> </dl>

 

 
