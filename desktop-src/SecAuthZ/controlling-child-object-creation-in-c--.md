---
description: Puede usar la DACL de un objeto contenedor para controlar quién puede crear objetos secundarios dentro del contenedor.
ms.assetid: 95f2f058-f847-4f58-b469-090bf599ae98
title: Controlar la creación de objetos secundarios en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598b2fd9a9889fbb77d2b3a4ecd004efcd823b8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160843"
---
# <a name="controlling-child-object-creation-in-c"></a>Controlar la creación de objetos secundarios en C++

Puede usar la DACL de un objeto contenedor para controlar quién puede crear objetos secundarios dentro del contenedor. Esto puede ser importante porque el creador de un objeto normalmente se asigna como propietario del objeto y el propietario de un objeto puede controlar el acceso al objeto.

Los distintos tipos de objetos de contenedor tienen derechos de acceso específicos que controlan la capacidad de crear objetos secundarios. Por ejemplo, un subproceso debe tener acceso KEY CREATE SUB KEY a una clave del Registro para \_ \_ crear una \_ subclave bajo la clave. La DACL de una clave del Registro puede contener ACE que permiten o deniegan este derecho de acceso. De forma similar, NTFS admite los derechos de acceso FILE ADD FILE y FILE ADD SUBDIRECTORY para controlar la capacidad de crear archivos \_ \_ o \_ \_ directorios en un directorio.

El derecho de acceso ADS RIGHT DS CREATE CHILD controla la creación de objetos secundarios en un objeto de \_ \_ servicio de directorio \_ \_ (DS). Sin embargo, los objetos DS pueden contener distintos tipos de objetos, por lo que el sistema admite una granularidad de control más fina. Puede usar ACE [específicas del](object-specific-aces.md) objeto para permitir o denegar el derecho a crear un tipo especificado de objeto secundario. Puede permitir que un usuario cree un tipo de objeto secundario al tiempo que impide que el usuario cree otros tipos de objetos secundarios.

En el ejemplo siguiente se [**usa la función SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) para agregar una ACE específica del objeto a una ACL. La ACE concede permiso para crear un tipo especificado de objeto secundario. El **miembro grfAccessPermissions** de la estructura [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) se establece en ADS RIGHT DS CREATE CHILD para indicar que la ACE controla la creación \_ del objeto \_ \_ \_ secundario. El **miembro ObjectsPresent** de la estructura [**OBJECTS AND \_ \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) se establece en ACE OBJECT TYPE PRESENT para indicar que el \_ miembro \_ \_ **ObjectTypeGuid** contiene un GUID válido. El GUID identifica un tipo de objeto secundario cuya creación se está controlando.

En el ejemplo siguiente, pOldDACL debe ser un puntero válido a una estructura [**de ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) existente. Para obtener información sobre cómo crear una estructura **de ACL** para un objeto, vea Crear un descriptor de seguridad para un nuevo objeto [en C++.](creating-a-security-descriptor-for-a-new-object-in-c--.md)


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



 

 



