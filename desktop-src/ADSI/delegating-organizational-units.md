---
title: Delegación de unidades organizativas
description: La compañía de Fabrikam contrata dos administradores, Mike y Paul, para administrar las unidades organizativas este y oeste, respectivamente.
ms.assetid: ecf71ae6-9b6f-4e3c-878a-2c6fd193da33
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9928884c8be19f9668d6f81ed9462f6fb757286f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656187"
---
# <a name="delegating-organizational-units"></a>Delegación de unidades organizativas

La compañía de Fabrikam contrata dos administradores, Mike y Paul, para administrar las unidades organizativas este y oeste, respectivamente. Joe delega sus responsabilidades administrativas en ellos para que puedan crear y eliminar usuarios en sus unidades organizativas respectivas.

Antes de ver cómo configurar estas unidades organizativas en Mike y Paul, debe entender cómo configurar el acceso a los objetos en Active Directory. Cada objeto de Active Directory tiene un descriptor de seguridad. Con el descriptor de seguridad, puede modificar los permisos en el objeto, propagar los permisos, habilitar la auditoría, etc. El propio descriptor de seguridad tiene dos listas de control de acceso (ACL): una ACL discrecional (DACL) y una ACL del sistema (SACL). Cada ACL puede contener entradas de control de acceso (ACE). Con una ACE, puede establecer el acceso permitido o denegado en un objeto. Además, puede especificar acciones específicas para permitir o denegar. Algunos ejemplos de acciones son crear secundaria, eliminar secundaria, leer propiedad y escribir propiedad. Estos derechos se especifican con [**AccessMask**](iadsaccesscontrolentry-property-methods.md).

A continuación, puede especificar las clases o los atributos a los que está asociada esta ACE. En el ejemplo de Fabrikam siguiente, Joe selecciona la clase de usuario para que cada administrador pueda agregar usuarios al sistema. A continuación, debe responder a la pregunta: "¿quién será el beneficiario de esta ACE?" Joe especificará Mike.

Por último, puede establecer el comportamiento de la herencia ACE; por ejemplo, se pueden especificar ACE para propagar hacia abajo en la jerarquía. En Resumen, el ejemplo anterior hará que Mike sea capaz de crear y eliminar objetos de usuario en la unidad organizativa de ventas del este.

Joe usa el siguiente ejemplo de código para configurar las ACE y las ACL en la unidad organizativa East.


```VB
Set ou = GetObject("LDAP://OU=East, OU=Sales, DC=Fabrikam,DC=COM")
Set sec = ou.Get("ntSecurityDescriptor")
Set acl = sec.DiscretionaryAcl

Set ace = CreateObject("AccessControlEntry") 
' You can also use Set ace = new ADsAccessControlEntry.

' Grant access to the object.
ace.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT 

' Create and delete child objects.
ace.AccessMask = ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD 
' Create the user object with the user schema IDGUID.
ace.ObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 
' Propagate the ACE down.  
ace.AceFlags = ADS_ACEFLAG_INHERIT_ACE
' Provide an option that notifies that the objectType is filled.
ace.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT 
' Show the beneficiary of this ACE.
ace.Trustee = "FABRIKAM\Mike" 
acl.AddAce ace

sec.DiscretionaryAcl = acl
ou.Put "ntSecurityDescriptor", Array(sec)
' Use SetInfo to commit the data to Active Directory.
ou.SetInfo 

' Release the objects.
Set ace = Nothing
Set acl  = Nothing
Set sec = Nothing
```



En la ilustración siguiente se muestra el Active Directory menú **crear nueva vista** después de que se ejecute el código. Cuando Joe, el administrador inicia sesión, ve varias clases que puede crear. Sin embargo, cuando Mike inicia sesión, solo puede crear objetos de usuario.

![crear nuevo menú de opciones de vista](images/adadsi5.png)

Para obtener más información, vea [modelo de seguridad ADSI](adsi-security-model.md).

 

 




