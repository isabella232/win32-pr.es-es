---
description: Puede usar la DACL de un objeto contenedor para controlar quién puede crear objetos secundarios en el contenedor.
ms.assetid: 95f2f058-f847-4f58-b469-090bf599ae98
title: Controlar la creación de objetos secundarios en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598b2fd9a9889fbb77d2b3a4ecd004efcd823b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543542"
---
# <a name="controlling-child-object-creation-in-c"></a><span data-ttu-id="9c979-103">Controlar la creación de objetos secundarios en C++</span><span class="sxs-lookup"><span data-stu-id="9c979-103">Controlling Child Object Creation in C++</span></span>

<span data-ttu-id="9c979-104">Puede usar la DACL de un objeto contenedor para controlar quién puede crear objetos secundarios en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="9c979-104">You can use the DACL of a container object to control who is allowed to create child objects within the container.</span></span> <span data-ttu-id="9c979-105">Esto puede ser importante porque el creador de un objeto se asigna normalmente como el propietario del objeto y el propietario de un objeto puede controlar el acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="9c979-105">This can be important because the creator of an object is typically assigned as the object's owner, and an object's owner can control access to the object.</span></span>

<span data-ttu-id="9c979-106">Los distintos tipos de objetos de contenedor tienen derechos de acceso específicos que controlan la capacidad de crear objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="9c979-106">The various types of container objects have specific access rights that control the ability to create child objects.</span></span> <span data-ttu-id="9c979-107">Por ejemplo, un subproceso debe tener \_ \_ acceso de \_ subclave Create Key a una clave del registro para crear una subclave en la clave.</span><span class="sxs-lookup"><span data-stu-id="9c979-107">For example, a thread must have KEY\_CREATE\_SUB\_KEY access to a registry key to create a subkey under the key.</span></span> <span data-ttu-id="9c979-108">La DACL de una clave del registro puede contener ACE que permiten o deniegan este derecho de acceso.</span><span class="sxs-lookup"><span data-stu-id="9c979-108">The DACL of a registry key can contain ACEs that allow or deny this access right.</span></span> <span data-ttu-id="9c979-109">Del mismo modo, NTFS admite \_ los \_ derechos de acceso Agregar archivo y agregar archivo del \_ \_ subdirectorio para controlar la capacidad de crear archivos o directorios en un directorio.</span><span class="sxs-lookup"><span data-stu-id="9c979-109">Similarly, NTFS supports the FILE\_ADD\_FILE and FILE\_ADD\_SUBDIRECTORY access rights for controlling the ability to create files or directories in a directory.</span></span>

<span data-ttu-id="9c979-110">El derecho de acceso de la \_ \_ creación de secundario DS de ad Right \_ \_ controla la creación de objetos secundarios en un objeto de servicio de directorio (DS).</span><span class="sxs-lookup"><span data-stu-id="9c979-110">The ADS\_RIGHT\_DS\_CREATE\_CHILD access right controls the creation of child objects in a directory service (DS) object.</span></span> <span data-ttu-id="9c979-111">Sin embargo, los objetos DS pueden contener diferentes tipos de objetos, por lo que el sistema admite una granularidad más fina de control.</span><span class="sxs-lookup"><span data-stu-id="9c979-111">However, DS objects can contain different types of objects, so the system supports a finer granularity of control.</span></span> <span data-ttu-id="9c979-112">Puede usar las [ACE específicas del objeto](object-specific-aces.md) para permitir o denegar el derecho a crear un tipo especificado de objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="9c979-112">You can use [object-specific ACEs](object-specific-aces.md) to allow or deny the right to create a specified type of child object.</span></span> <span data-ttu-id="9c979-113">Puede permitir a un usuario crear un tipo de objeto secundario mientras evita que el usuario cree otros tipos de objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="9c979-113">You can allow a user to create one type of child object while preventing the user from creating other types of child objects.</span></span>

<span data-ttu-id="9c979-114">En el ejemplo siguiente se usa la función [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) para agregar una ACE específica del objeto a una ACL.</span><span class="sxs-lookup"><span data-stu-id="9c979-114">The following example uses the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to add an object-specific ACE to an ACL.</span></span> <span data-ttu-id="9c979-115">La ACE concede permiso para crear un tipo especificado de objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="9c979-115">The ACE grants permission to create a specified type of child object.</span></span> <span data-ttu-id="9c979-116">El miembro **grfAccessPermissions** de la estructura de [**\_ acceso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) está establecido en ADS \_ right \_ DS \_ Create \_ Child para indicar que la Ace controla la creación del objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="9c979-116">The **grfAccessPermissions** member of the [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structure is set to ADS\_RIGHT\_DS\_CREATE\_CHILD to indicate that the ACE controls the child object creation.</span></span> <span data-ttu-id="9c979-117">El miembro **ObjectsPresent** de la estructura [**Objects \_ y \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) se establece en el \_ tipo de objeto ACE \_ \_ presente para indicar que el miembro **ObjectTypeGuid** contiene un GUID válido.</span><span class="sxs-lookup"><span data-stu-id="9c979-117">The **ObjectsPresent** member of the [**OBJECTS\_AND\_SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) structure is set to ACE\_OBJECT\_TYPE\_PRESENT to indicate that the **ObjectTypeGuid** member contains a valid GUID.</span></span> <span data-ttu-id="9c979-118">El GUID identifica un tipo de objeto secundario cuya creación se controla.</span><span class="sxs-lookup"><span data-stu-id="9c979-118">The GUID identifies a type of child object whose creation is being controlled.</span></span>

<span data-ttu-id="9c979-119">En el ejemplo siguiente, pOldDACL debe ser un puntero válido a una estructura de [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) existente.</span><span class="sxs-lookup"><span data-stu-id="9c979-119">In the following example, pOldDACL must be a valid pointer to an existing [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) structure.</span></span> <span data-ttu-id="9c979-120">Para obtener información sobre cómo crear una estructura de **ACL** para un objeto, vea [crear un descriptor de seguridad para un nuevo objeto en C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="9c979-120">For information about how to create an **ACL** structure for an object, see [Creating a Security Descriptor for a New Object in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span></span>


```C++
DWORD dwRes;
PACL pOldDACL = NULL;
PACL pNewDACL = NULL;
GUID guidChildObjectType = GUID_NULL;   // GUID of object to control creation of
PSID pTrusteeSID = NULL;           // trustee for new ACE
EXPLICIT_ACCESS ea;
OBJECTS_AND_SID ObjectsAndSID;

// pOldDACL must be a valid pointer to an existing ACL structure.

// guidChildObjectType must be the GUID of an object type 
// that is a possible child of the object associated with pOldDACL.
 
// Initialize an OBJECTS_AND_SID structure with object type GUIDs and 
// the SID of the trustee for the new ACE. 

ZeroMemory(&ObjectsAndSID, sizeof(OBJECTS_AND_SID));
ObjectsAndSID.ObjectsPresent = ACE_OBJECT_TYPE_PRESENT;
ObjectsAndSID.ObjectTypeGuid = guidChildObjectType;
ObjectsAndSID.InheritedObjectTypeGuid  = GUID_NULL;
ObjectsAndSID.pSid = (SID *)pTrusteeSID;

// Initialize an EXPLICIT_ACCESS structure for the new ACE. 

ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
ea.grfAccessPermissions = ADS_RIGHT_DS_CREATE_CHILD;
ea.grfAccessMode = GRANT_ACCESS;
ea.grfInheritance= NO_INHERITANCE;
ea.Trustee.TrusteeForm = TRUSTEE_IS_OBJECTS_AND_SID;
ea.Trustee.ptstrName = (LPTSTR) &ObjectsAndSID;

// Create a new ACL that merges the new ACE
// into the existing DACL.

dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
```



 

 



