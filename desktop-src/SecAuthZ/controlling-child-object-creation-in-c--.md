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
# <a name="controlling-child-object-creation-in-c"></a>Controlar la creación de objetos secundarios en C++

Puede usar la DACL de un objeto contenedor para controlar quién puede crear objetos secundarios en el contenedor. Esto puede ser importante porque el creador de un objeto se asigna normalmente como el propietario del objeto y el propietario de un objeto puede controlar el acceso al objeto.

Los distintos tipos de objetos de contenedor tienen derechos de acceso específicos que controlan la capacidad de crear objetos secundarios. Por ejemplo, un subproceso debe tener \_ \_ acceso de \_ subclave Create Key a una clave del registro para crear una subclave en la clave. La DACL de una clave del registro puede contener ACE que permiten o deniegan este derecho de acceso. Del mismo modo, NTFS admite \_ los \_ derechos de acceso Agregar archivo y agregar archivo del \_ \_ subdirectorio para controlar la capacidad de crear archivos o directorios en un directorio.

El derecho de acceso de la \_ \_ creación de secundario DS de ad Right \_ \_ controla la creación de objetos secundarios en un objeto de servicio de directorio (DS). Sin embargo, los objetos DS pueden contener diferentes tipos de objetos, por lo que el sistema admite una granularidad más fina de control. Puede usar las [ACE específicas del objeto](object-specific-aces.md) para permitir o denegar el derecho a crear un tipo especificado de objeto secundario. Puede permitir a un usuario crear un tipo de objeto secundario mientras evita que el usuario cree otros tipos de objetos secundarios.

En el ejemplo siguiente se usa la función [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) para agregar una ACE específica del objeto a una ACL. La ACE concede permiso para crear un tipo especificado de objeto secundario. El miembro **grfAccessPermissions** de la estructura de [**\_ acceso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) está establecido en ADS \_ right \_ DS \_ Create \_ Child para indicar que la Ace controla la creación del objeto secundario. El miembro **ObjectsPresent** de la estructura [**Objects \_ y \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) se establece en el \_ tipo de objeto ACE \_ \_ presente para indicar que el miembro **ObjectTypeGuid** contiene un GUID válido. El GUID identifica un tipo de objeto secundario cuya creación se controla.

En el ejemplo siguiente, pOldDACL debe ser un puntero válido a una estructura de [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) existente. Para obtener información sobre cómo crear una estructura de **ACL** para un objeto, vea [crear un descriptor de seguridad para un nuevo objeto en C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).


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



 

 



