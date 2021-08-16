---
title: Modificar un objeto ADSI desde ADO
description: ADSI para Windows 2000 y DS Client incluye un proveedor de OLE DB lectura. Esto significa que, en este momento, no se puede emitir la instrucción UPDATE en el SQL dialecto.
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- Modificación de un objeto ADSI a partir de ADSI de ADO
- ActiveX adsi de objeto de datos , modificar un objeto ADSI desde ADO
- ADSI ADSI, código de ejemplo C/C++, modificar un objeto ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4562e67043ea168a0b158088ffe3c2772f3ae28a0a2fa8881e102574cf2eb97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839455"
---
# <a name="modifying-an-adsi-object-from-ado"></a>Modificar un objeto ADSI desde ADO

ADSI para Windows 2000 y DS Client incluye un proveedor de OLE DB lectura. Esto significa que, en este momento, no se puede emitir la instrucción UPDATE en el SQL dialecto.

**Para modificar un objeto devuelto desde una consulta ADO**

1.  Solicite **ADsPath al** especificar un nombre de atributo, como en "SELECT ADsPath, ..."
2.  Ejecute la consulta y obtenga el **atributo ADsPath.**
3.  Enlace al conjunto de registros mediante **ADsPath** y modifique los atributos.

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



 

 




