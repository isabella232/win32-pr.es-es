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
# <a name="modifying-the-acls-of-an-object-in-c"></a><span data-ttu-id="6ff14-103">Modificar las ACL de un objeto en C++</span><span class="sxs-lookup"><span data-stu-id="6ff14-103">Modifying the ACLs of an Object in C++</span></span>

<span data-ttu-id="6ff14-104">En el ejemplo siguiente se agrega una [*entrada de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) a la lista de control de [*acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) de un objeto.</span><span class="sxs-lookup"><span data-stu-id="6ff14-104">The following example adds an [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) to the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of an object.</span></span>

<span data-ttu-id="6ff14-105">El parámetro *AccessMode* determina el tipo de nueva ACE y cómo se combina la nueva ACE con las ACE existentes para el administrador de confianza especificado.</span><span class="sxs-lookup"><span data-stu-id="6ff14-105">The *AccessMode* parameter determines the type of new ACE and how the new ACE is combined with any existing ACEs for the specified trustee.</span></span> <span data-ttu-id="6ff14-106">Use las \_ marcas Grant Access, set \_ Access, deny \_ Access o REVOKE \_ Access en el parámetro *AccessMode* .</span><span class="sxs-lookup"><span data-stu-id="6ff14-106">Use the GRANT\_ACCESS, SET\_ACCESS, DENY\_ACCESS, or REVOKE\_ACCESS flags in the *AccessMode* parameter.</span></span> <span data-ttu-id="6ff14-107">Para obtener información acerca de estas marcas, consulte [**\_ modo de acceso**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span><span class="sxs-lookup"><span data-stu-id="6ff14-107">For information about these flags, see [**ACCESS\_MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span></span>

<span data-ttu-id="6ff14-108">Se puede usar código similar para trabajar con una [*lista de control de acceso*](/windows/desktop/SecGloss/s-gly) (SACL) del sistema.</span><span class="sxs-lookup"><span data-stu-id="6ff14-108">Similar code can be used to work with a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="6ff14-109">Especifique la \_ \_ información de seguridad de SACL en las funciones [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) y [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para obtener y establecer la SACL para el objeto.</span><span class="sxs-lookup"><span data-stu-id="6ff14-109">Specify SACL\_SECURITY\_INFORMATION in the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) and [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) functions to get and set the SACL for the object.</span></span> <span data-ttu-id="6ff14-110">Use las \_ \_ marcas de acceso establecer auditoría correcta, establecer \_ error de auditoría \_ y revocar \_ acceso en el parámetro *AccessMode* .</span><span class="sxs-lookup"><span data-stu-id="6ff14-110">Use the SET\_AUDIT\_SUCCESS, SET\_AUDIT\_FAILURE, and REVOKE\_ACCESS flags in the *AccessMode* parameter.</span></span> <span data-ttu-id="6ff14-111">Para obtener información acerca de estas marcas, consulte [**\_ modo de acceso**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span><span class="sxs-lookup"><span data-stu-id="6ff14-111">For information about these flags, see [**ACCESS\_MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span></span>

<span data-ttu-id="6ff14-112">Use este código para agregar una [ACE específica del objeto](object-specific-aces.md) a la DACL de un objeto de servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="6ff14-112">Use this code to add an [object-specific ACE](object-specific-aces.md) to the DACL of a directory service object.</span></span> <span data-ttu-id="6ff14-113">Para especificar los GUID en una ACE específica de un objeto, establezca el parámetro *TrusteeForm* en Trustee \_ es \_ objetos \_ y \_ Name o Trustee \_ es \_ Objects \_ y \_ SID, y establezca el parámetro *pszTrustee* en un puntero a los [**objetos \_ , \_ el nombre**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) , los objetos y la estructura de [**\_ \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) .</span><span class="sxs-lookup"><span data-stu-id="6ff14-113">To specify the GUIDs in an object-specific ACE, set the *TrusteeForm* parameter to TRUSTEE\_IS\_OBJECTS\_AND\_NAME or TRUSTEE\_IS\_OBJECTS\_AND\_SID and set the *pszTrustee* parameter to be a pointer to an [**OBJECTS\_AND\_NAME**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) or [**OBJECTS\_AND\_SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) structure.</span></span>

<span data-ttu-id="6ff14-114">En este ejemplo se usa la función [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para obtener la DACL existente.</span><span class="sxs-lookup"><span data-stu-id="6ff14-114">This example uses the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) function to get the existing DACL.</span></span> <span data-ttu-id="6ff14-115">A continuación, rellena una estructura de [**\_ acceso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) con información sobre una ACE y usa la función [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) para combinar la nueva ACE con las ACE existentes en la DACL.</span><span class="sxs-lookup"><span data-stu-id="6ff14-115">Then it fills an [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structure with information about an ACE and uses the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to merge the new ACE with any existing ACEs in the DACL.</span></span> <span data-ttu-id="6ff14-116">Por último, en el ejemplo se llama a la función [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para adjuntar la nueva DACL al [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) del objeto.</span><span class="sxs-lookup"><span data-stu-id="6ff14-116">Finally, the example calls the [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) function to attach the new DACL to the [*security descriptor*](/windows/desktop/SecGloss/s-gly) of the object.</span></span>


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



 

 
