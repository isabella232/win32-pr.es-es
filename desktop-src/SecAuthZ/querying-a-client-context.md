---
description: Las aplicaciones pueden llamar a la función AuthzGetInformationFromContext para consultar información sobre un contexto de cliente existente.
ms.assetid: 32655e54-499e-439e-8d4f-f2b4eaa0b184
title: Consultar un contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101c35466e675d9ecba942089bbe7b5e82cffd90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666666"
---
# <a name="querying-a-client-context"></a>Consultar un contexto de cliente

Las aplicaciones pueden llamar a la función [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) para consultar información sobre un contexto de cliente existente.

El parámetro *InfoClass* de la función [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) toma un valor de la enumeración de la [**\_ \_ \_ clase de información de contexto de AUTHZ**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) que especifica qué tipo de información consulta la función.

Las variables de atributo de seguridad deben estar presentes en el contexto del cliente si se hace referencia a ellas en una expresión condicional; de lo contrario, el término de expresión condicional que hace referencia a ellos se evaluará como desconocido. Para obtener más información sobre las expresiones condicionales, vea el tema [lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md) .

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se consulta el contexto de cliente creado en el ejemplo de [inicialización de un contexto de cliente](initializing-a-client-context.md) para recuperar la lista de [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) de grupos asociados a ese contexto de cliente.


```C++
BOOL GetGroupsFromContext(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{

    DWORD                cbSize = 0;
    PTOKEN_GROUPS        pTokenGroups=NULL;
    LPTSTR                StringSid = NULL;
    BOOL                bResult = FALSE;
    int i = 0;

    //Call the AuthzGetInformationFromContext function with a NULL output buffer to get the required buffer size.
    AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, 0, &cbSize, NULL);
    
        
    

    //Allocate the buffer for the TOKEN_GROUPS structure.
    pTokenGroups = (PTOKEN_GROUPS)malloc(cbSize);
    if (!pTokenGroups)
        return FALSE;

    //Get the SIDs of groups associated with the client context. 
    if(!AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, cbSize, &cbSize, pTokenGroups))
    {    
        printf_s("AuthzGetInformationFromContext failed with %d\n", GetLastError);
        free(pTokenGroups);
        return FALSE;
    }

    //Enumerate and display the group SIDs.
    for (i=pTokenGroups->GroupCount-1; i >= 0; --i)
    {
        //Convert a SID to a string.
        if(!ConvertSidToStringSid(
            pTokenGroups->Groups[i].Sid,
            &StringSid
            ))
        {
            LocalFree(StringSid);
            return FALSE;
        }


        wprintf_s(L"%s \n", StringSid);
        
    }

    free(pTokenGroups);

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

[Inicializar un contexto de cliente](initializing-a-client-context.md)
</dt> <dt>

[Lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



