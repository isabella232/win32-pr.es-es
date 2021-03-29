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
# <a name="modifying-an-adsi-object-from-ado"></a><span data-ttu-id="2d1ba-107">Modificar un objeto ADSI desde ADO</span><span class="sxs-lookup"><span data-stu-id="2d1ba-107">Modifying an ADSI Object from ADO</span></span>

<span data-ttu-id="2d1ba-108">ADSI para Windows 2000 y el cliente de DS incluye un proveedor de OLE DB de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2d1ba-108">ADSI for Windows 2000 and DS Client includes a read-only OLE DB provider.</span></span> <span data-ttu-id="2d1ba-109">Esto significa que, en la actualidad, no se puede emitir la instrucción UPDATE en el dialecto SQL.</span><span class="sxs-lookup"><span data-stu-id="2d1ba-109">This means that you cannot, at present, issue the UPDATE statement in the SQL dialect.</span></span>

<span data-ttu-id="2d1ba-110">**Para modificar un objeto devuelto desde una consulta de ADO**</span><span class="sxs-lookup"><span data-stu-id="2d1ba-110">**To modify an object returned from an ADO query**</span></span>

1.  <span data-ttu-id="2d1ba-111">Solicite el **ADsPath** al especificar un nombre de atributo, como en "seleccionar ADsPath,..."</span><span class="sxs-lookup"><span data-stu-id="2d1ba-111">Request the **ADsPath** when specifying an attribute name, as in "SELECT ADsPath, ..."</span></span>
2.  <span data-ttu-id="2d1ba-112">Ejecute la consulta y obtenga el atributo **ADsPath** .</span><span class="sxs-lookup"><span data-stu-id="2d1ba-112">Execute the query and get the **ADsPath** attribute.</span></span>
3.  <span data-ttu-id="2d1ba-113">Enlace con el conjunto de registros mediante **ADsPath** y modifique los atributos.</span><span class="sxs-lookup"><span data-stu-id="2d1ba-113">Bind to the record set using **ADsPath**, and modify the attributes.</span></span>

<span data-ttu-id="2d1ba-114">En el ejemplo de código siguiente se muestra cómo modificar un objeto ADSI después de realizar los pasos descritos en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="2d1ba-114">The following code example shows how to modify an ADSI object after performing the steps outlined in the preceding example.</span></span>


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



 

 




