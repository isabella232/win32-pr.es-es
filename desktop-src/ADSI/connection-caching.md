---
title: Almacenamiento en caché de conexiones
description: Cuando se establece una conexión a un servidor, el identificador de conexión se almacena en caché en el equipo cliente para ese proceso hasta que se cierra esa conexión.
ms.assetid: 927afd35-8703-4234-b6a8-6320a3667532
ms.tgt_platform: multiple
keywords:
- ADSI de almacenamiento en caché de conexión
- almacenamiento en caché de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0fbf63d65a6941e986069289db201a237deb9ddc7058f291218c1496d0a40e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429032"
---
# <a name="connection-caching"></a>Almacenamiento en caché de conexiones

Cuando se establece una conexión a un servidor, el identificador de conexión se almacena en caché en el equipo cliente para ese proceso hasta que se cierra esa conexión. Si se usan el mismo servidor, puerto y credenciales en una conexión posterior y solo las marcas de autenticación BIND o **ADS \_ SERVER \_ BIND** de **ADS \_ FAST \_** difieren, ADSI reutilizará la conexión existente. ADSI realiza este almacenamiento en caché de conexiones por proceso.

Para aumentar el rendimiento, reutilice las conexiones existentes cuando sea posible.

En el ejemplo de código siguiente se muestra cómo funciona el almacenamiento en caché de conexiones.


```VB
Dim cachedConn As IADs
Dim obj As IADs
Dim cachedName As String
Dim objName As String
 
' Connect to the server and maintain this handle to cache the connection.
Set cachedConn = GetObject("LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com")
 
cachedName = cachedConn.Get("distinguishedName")
Debug.Print (cachedName)
 
' Reuse the connection to MyMachine opened by cachedConn.
' Be aware that this line executes quickly because it is not required
' to transmit over the network again.
Set obj = GetObject("LDAP://MyMachine/CN=Bob,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection.
Set obj = Nothing
 
' Reuse the connection to MyMachine opened by cachedConn again.
Set obj = GetObject("LDAP://MyMachine/CN=Administrator,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection again.
Set obj = Nothing
 
' Release the first connection.
Set cachedConn = Nothing
 
' The connection to MyMachine is closed.
```



 

 




