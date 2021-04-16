---
description: Active Directory objetos se pueden usar para buscar recursos en un dominio de red del equipo, como usuarios, directivas de seguridad, impresoras, componentes distribuidos y otros recursos.
ms.assetid: 96f89537-9419-495e-819c-fd07ba546620
ms.tgt_platform: multiple
title: Crear y actualizar objetos Active Directory
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0b36a12860ea2c2dc9085b784fdaf85cd95ab87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706171"
---
# <a name="creating-and-updating-active-directory-objects"></a>Crear y actualizar objetos Active Directory

Active Directory objetos se pueden usar para buscar recursos en un dominio de red del equipo, como usuarios, directivas de seguridad, impresoras, componentes distribuidos y otros recursos. Active Directory objetos se pueden crear y actualizar mediante WMI. Puede actualizar un objeto de Active Directory cuando la nueva información sobre el objeto está disponible mediante la notificación de eventos WMI. Por ejemplo, una vez creado un objeto de usuario Active Directory, puede detectar su creación con una consulta de evento en WMI y, cuando se recibe el evento, puede actualizar el objeto con información nueva.

En el ejemplo de código siguiente se crea una nueva instancia de WMI de la clase que representa el objeto de usuario Active Directory. En el ejemplo se muestra cómo asignar valores a diversas propiedades requeridas para crear la nueva instancia de usuario de Active Directory.


```VB
Const cUserID = "WMIUser"
Const cComputerName = "LocalHost"
Const cWMInamespace = "root/directory/LDAP"
Const cWMIclass = "ds_user"

Const ADS_UF_ACCOUNTDISABLE = &h000002

Set objWMILocator = _
    CreateObject("WbemScripting.SWbemLocator")
objWMILocator.Security_.AuthenticationLevel = _
    wbemAuthenticationLevelDefault

Set objWMIServices = objWMILocator. _
    ConnectServer(cComputerName, cWMInamespace, "", "")

Set objWMIClass = objWMIServices.Get(cWMIclass)

Set objWMIInstance = objWMIClass.SpawnInstance_

objWMIInstance.DS_sAMAccountName = userID
objWMIInstance.ADSIPath = "LDAP://CN=" & userID & _
    ",CN=Users,DC=LissWare,DC=Net"

objWMIInstance.Put_ (wbemChangeFlagCreateOrUpdate Or _
    wbemFlagReturnWhenComplete)

WScript.Echo "Active Directory user created."
```



En el siguiente ejemplo de código se actualiza una instancia de WMI de un objeto Active Directory. En este ejemplo, se actualiza el atributo DisplayName.


```VB
set svc = getObject("Winmgmts:root\directory\ldap")

' A context object is used to tell the provider which
' specific properties are going to be updated.  
' In most cases, when you update a WMI object you do not
' need to specify an additional context object. 
' However,  if a context object is not supplied for a
' directory service provider, the update fails.

set octx = createobject( _
    "wbemscripting.swbemnamedvalueset")
octx.add "__PUT_EXT_PROPERTIES", array("ds_displayname")
octx.add "__PUT_EXTENSIONS", true
octx.add "__PUT_EXT_CLIENT_REQUEST", true


set objEnum = svc.execQuery( _
    "select * from ds_computer where ds_cn = 'userName'", "WQL", 32)

for each obj in objEnum
 obj.ds_DisplayName = "updatedName"
 obj.put_ 1, octx
next

WScript.Echo "Active Directory user successfully updated"
```



 

 



