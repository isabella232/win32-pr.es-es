---
description: Compruebe los derechos de acceso que un descriptor de seguridad permite para un cliente.
ms.assetid: de21968e-4590-4798-9152-43204d55521f
title: Comprobación del acceso de cliente con ACL en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda629338d731d6e93f316fc15a6338c99bc1609
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160809"
---
# <a name="verifying-client-access-with-acls-in-c"></a>Comprobación del acceso de cliente con ACL en C++

En el ejemplo siguiente se muestra cómo un servidor podría comprobar los derechos de acceso que un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) permite para un cliente. En el ejemplo se usa [**la función ImpersonateNamedPipeClient;**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) sin embargo, funcionaría igual con cualquiera de las otras funciones de suplantación. Después de suplantar al cliente, en el ejemplo se llama a la [**función OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para obtener el [*token de suplantación*](/windows/desktop/SecGloss/i-gly). A continuación, llama a la función [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) para convertir los derechos de acceso genéricos en los derechos específicos y estándar correspondientes según la asignación especificada en la [**estructura GENERIC \_ MAPPING.**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)

La [**función AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) comprueba los derechos de acceso solicitados con respecto a los derechos permitidos para el cliente en la DACL del descriptor de seguridad. Para comprobar el acceso y generar una entrada en el registro de eventos de seguridad, use la [**función AccessCheckAndAuditAlarm.**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)


```C++
#include <windows.h>
#pragma comment(lib, "advapi32.lib")

BOOL ImpersonateAndCheckAccess(
  HANDLE hNamedPipe,               // handle of pipe to impersonate
  PSECURITY_DESCRIPTOR pSD,        // security descriptor to check
  DWORD dwAccessDesired,           // access rights to check
  PGENERIC_MAPPING pGeneric,       // generic mapping for object
  PDWORD pdwAccessAllowed          // returns allowed access rights
) 
{
   HANDLE hToken;
   PRIVILEGE_SET PrivilegeSet;
   DWORD dwPrivSetSize = sizeof( PRIVILEGE_SET );
   BOOL fAccessGranted=FALSE;

// Impersonate the client.

   if (! ImpersonateNamedPipeClient(hNamedPipe) ) 
      return FALSE;

// Get an impersonation token with the client's security context.

   if (! OpenThreadToken( GetCurrentThread(), TOKEN_ALL_ACCESS,
         TRUE, &hToken ))
   {
      goto Cleanup;
   }

// Use the GENERIC_MAPPING structure to convert any 
// generic access rights to object-specific access rights.

   MapGenericMask( &dwAccessDesired, pGeneric );

// Check the client's access rights.

   if( !AccessCheck( 
      pSD,                 // security descriptor to check
      hToken,              // impersonation token
      dwAccessDesired,     // requested access rights
      pGeneric,            // pointer to GENERIC_MAPPING
      &PrivilegeSet,       // receives privileges used in check
      &dwPrivSetSize,      // size of PrivilegeSet buffer
      pdwAccessAllowed,    // receives mask of allowed access rights
      &fAccessGranted ))   // receives results of access check
   {
      goto Cleanup;
   }

Cleanup:

   RevertToSelf();

   if (hToken != INVALID_HANDLE_VALUE)
      CloseHandle(hToken);  

   return fAccessGranted;
}
```



 

 
