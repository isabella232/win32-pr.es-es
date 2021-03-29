---
title: Modificar un objeto ADSI desde ADO
description: ADSI para Windows 2000 y el cliente de DS incluye un proveedor de OLE DB de solo lectura. Esto significa que, en la actualidad, no se puede emitir la instrucción UPDATE en el dialecto SQL.
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- Modificar un objeto ADSI desde ADSI de ADO
- Objeto de datos ActiveX ADSI, modificar un objeto ADSI desde ADO
- ADSI ADSI, código de ejemplo C/C++, modificar un objeto ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7291088915a537231077e1d75161b57684caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772943"
---
# <a name="modifying-an-adsi-object-from-ado"></a>Modificar un objeto ADSI desde ADO

ADSI para Windows 2000 y el cliente de DS incluye un proveedor de OLE DB de solo lectura. Esto significa que, en la actualidad, no se puede emitir la instrucción UPDATE en el dialecto SQL.

**Para modificar un objeto devuelto desde una consulta de ADO**

1.  Solicite el **ADsPath** al especificar un nombre de atributo, como en "seleccionar ADsPath,..."
2.  Ejecute la consulta y obtenga el atributo **ADsPath** .
3.  Enlace con el conjunto de registros mediante **ADsPath** y modifique los atributos.

En el ejemplo de código siguiente se muestra cómo modificar un objeto ADSI después de realizar los pasos descritos en el ejemplo anterior.


```VB
Dim Con As New Connection
Dim rs As New Recordset
Dim command As New Command
Dim usr As IADsUser

' Replace department for all users in OU=sales.
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
 
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = con
 
command.CommandText = "SELECT AdsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=com' WHERE objectClass = 'user'"
 
command.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Set rs = command.Execute
While Not rs.EOF
    Set usr = GetObject(rs.Fields("AdsPath").Value)
    usr.Put "department", "1001"
    usr.SetInfo
    rs.MoveNext
Wend
```



 

 




