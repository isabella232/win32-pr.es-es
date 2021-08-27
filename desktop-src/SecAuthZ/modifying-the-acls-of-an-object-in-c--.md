---
description: En el ejemplo siguiente se agrega una entrada de control de acceso (ACE) a la lista de control de acceso discrecional (DACL) de un objeto .
ms.assetid: 0c168bb7-996f-42a8-96cd-2ba7870a3333
title: Modificar las ACL de un objeto en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42681a22e6b5f4b478d55d21f9b0b71dbe3f9c081ef5d18ba3da7a33f8709d32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912465"
---
# <a name="modifying-the-acls-of-an-object-in-c"></a>Modificar las ACL de un objeto en C++

En el ejemplo siguiente se agrega [*una entrada de control de*](/windows/desktop/SecGloss/a-gly) acceso (ACE) a la lista de control de acceso [*discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) de un objeto .

El *parámetro AccessMode* determina el tipo de nueva ACE y cómo se combina la nueva ACE con cualquier ACE existente para el administrador de confianza especificado. Use las marcas GRANT \_ ACCESS, SET ACCESS, DENY ACCESS o \_ REVOKE ACCESS en el parámetro \_ \_ *AccessMode.* Para obtener información sobre estas marcas, vea [**ACCESS \_ MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Se puede usar código similar para trabajar con una lista [*de control de acceso del sistema*](/windows/desktop/SecGloss/s-gly) (SACL). Especifique SACL SECURITY INFORMATION en las funciones \_ \_ [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) y [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para obtener y establecer la SACL del objeto. Use las marcas SET AUDIT SUCCESS, SET AUDIT FAILURE y \_ REVOKE ACCESS en el parámetro \_ \_ \_ \_ *AccessMode.* Para obtener información sobre estas marcas, vea [**ACCESS \_ MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Use este código para agregar una [ACE específica del objeto](object-specific-aces.md) a la DACL de un objeto de servicio de directorio. Para especificar los GUID en una ACE específica del objeto, establezca el parámetro *TrusteeForm* en TRUSTEE IS OBJECTS AND NAME o TRUSTEE IS OBJECTS AND SID y establezca el parámetro \_ \_ \_ \_ \_ \_ \_ \_ *pszTrustee* [**\_ \_**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) [**\_ \_**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) como puntero a una estructura OBJECTS AND NAME u OBJECTS AND SID.

En este ejemplo se [**usa la función GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para obtener la DACL existente. A continuación, rellena una estructura [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) con información sobre una ACE y usa la función [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) para combinar la nueva ACE con cualquier ACE existente en la DACL. Por último, en el ejemplo se llama a la función [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para asociar la nueva DACL al [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) del objeto .


```C++
#include <windows.h>
#include <stdio.h>

DWORD AddAceToObjectsSecurityDescriptor (
    LPTSTR pszObjName,          // name of object
    SE_OBJECT_TYPE ObjectType,  // type of object
    LPTSTR pszTrustee,          // trustee for new ACE
    TRUSTEE_FORM TrusteeForm,   // format of trustee structure
    DWORD dwAccessRights,       // access mask for new ACE
    ACCESS_MODE AccessMode,     // type of ACE
    DWORD dwInheritance         // inheritance flags for new ACE
) 
{
    DWORD dwRes = 0;
    PACL pOldDACL = NULL, pNewDACL = NULL;
    PSECURITY_DESCRIPTOR pSD = NULL;
    EXPLICIT_ACCESS ea;

    if (NULL == pszObjName) 
        return ERROR_INVALID_PARAMETER;

    // Get a pointer to the existing DACL.

    dwRes = GetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, &pOldDACL, NULL, &pSD);
    if (ERROR_SUCCESS != dwRes) {
        printf( "GetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Initialize an EXPLICIT_ACCESS structure for the new ACE. 

    ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
    ea.grfAccessPermissions = dwAccessRights;
    ea.grfAccessMode = AccessMode;
    ea.grfInheritance= dwInheritance;
    ea.Trustee.TrusteeForm = TrusteeForm;
    ea.Trustee.ptstrName = pszTrustee;

    // Create a new ACL that merges the new ACE
    // into the existing DACL.

    dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetEntriesInAcl Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Attach the new ACL as the object's DACL.

    dwRes = SetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, pNewDACL, NULL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    Cleanup:

        if(pSD != NULL) 
            LocalFree((HLOCAL) pSD); 
        if(pNewDACL != NULL) 
            LocalFree((HLOCAL) pNewDACL); 

        return dwRes;
}

```



 

 
