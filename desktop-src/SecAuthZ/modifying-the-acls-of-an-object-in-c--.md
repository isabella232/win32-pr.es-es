---
description: En el ejemplo siguiente se agrega una entrada de control de acceso (ACE) a la lista de control de acceso discrecional (DACL) de un objeto.
ms.assetid: 0c168bb7-996f-42a8-96cd-2ba7870a3333
title: Modificar las ACL de un objeto en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21195b1164ce949d1305f0c1748d24b0dbb7525b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002750"
---
# <a name="modifying-the-acls-of-an-object-in-c"></a>Modificar las ACL de un objeto en C++

En el ejemplo siguiente se agrega una [*entrada de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) a la lista de control de [*acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) de un objeto.

El parámetro *AccessMode* determina el tipo de nueva ACE y cómo se combina la nueva ACE con las ACE existentes para el administrador de confianza especificado. Use las \_ marcas Grant Access, set \_ Access, deny \_ Access o REVOKE \_ Access en el parámetro *AccessMode* . Para obtener información acerca de estas marcas, consulte [**\_ modo de acceso**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Se puede usar código similar para trabajar con una [*lista de control de acceso*](/windows/desktop/SecGloss/s-gly) (SACL) del sistema. Especifique la \_ \_ información de seguridad de SACL en las funciones [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) y [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para obtener y establecer la SACL para el objeto. Use las \_ \_ marcas de acceso establecer auditoría correcta, establecer \_ error de auditoría \_ y revocar \_ acceso en el parámetro *AccessMode* . Para obtener información acerca de estas marcas, consulte [**\_ modo de acceso**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Use este código para agregar una [ACE específica del objeto](object-specific-aces.md) a la DACL de un objeto de servicio de directorio. Para especificar los GUID en una ACE específica de un objeto, establezca el parámetro *TrusteeForm* en Trustee \_ es \_ objetos \_ y \_ Name o Trustee \_ es \_ Objects \_ y \_ SID, y establezca el parámetro *pszTrustee* en un puntero a los [**objetos \_ , \_ el nombre**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) , los objetos y la estructura de [**\_ \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) .

En este ejemplo se usa la función [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para obtener la DACL existente. A continuación, rellena una estructura de [**\_ acceso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) con información sobre una ACE y usa la función [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) para combinar la nueva ACE con las ACE existentes en la DACL. Por último, en el ejemplo se llama a la función [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para adjuntar la nueva DACL al [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) del objeto.


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



 

 
