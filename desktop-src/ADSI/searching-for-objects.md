---
title: Buscar objetos
description: Managers Bankert debe encontrar números de teléfono para todos los administradores de programas que trabajan en el departamento 101. Para ello, puede crear un script que use ADO y ADSI.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- buscar objetos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd41e87ad3396694b2f87158b15278c1dfbe28b044ad03ebbb09ddded705910a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973514"
---
# <a name="searching-for-objects"></a>Buscar objetos

Managers Bankert debe encontrar números de teléfono para todos los administradores de programas que trabajan en el departamento 101. Para ello, puede crear un script que use ADO y ADSI.

Cuando se usa el proveedor de ADO para realizar una consulta, el conjunto de resultados solo devolverá los primeros 1000 objetos. Por este motivo, es importante usar una consulta paginada para que pueda recuperar todos los objetos del conjunto de resultados, siempre y cuando no se haya establecido el servicio de directorio para limitar el número de elementos de un conjunto de resultados. Los conjuntos devueltos contendrán el número de elementos que especifique en el tamaño de página y los conjuntos paginados seguirán devolviendo hasta que se devuelvan todos los elementos del conjunto de resultados.


```VB
' Create the connection and command object.
Set oConnection1 = CreateObject("ADODB.Connection")
Set oCommand1 = CreateObject("ADODB.Command")
' Open the connection.
oConnection1.Provider = "ADsDSOObject"  ' This is the ADSI OLE-DB provider name
oConnection1.Open "Active Directory Provider"
' Create a command object for this connection.
Set oCommand1.ActiveConnection = oConnection1

' Compose a search string.
oCommand1.CommandText = "select name,telephoneNumber " & _
"from 'LDAP://DC=Fabrikam,DC=com'" & _
"WHERE objectCategory='Person'" & _
"AND objectClass='user'" & _
"AND title='Program Manager'" & _
"AND department=101"

' Execute the query.
Set rs = oCommand1.Execute
'--------------------------------------
' Navigate the record set
'--------------------------------------
While Not rs.EOF
    Debug.Print rs.Fields("Name") & " , " & rs.Fields("telephoneNumber")
    rs.MoveNext
Wend
```



Para realizar una búsqueda ADSI en Visual Basic un entorno de scripting, se requieren tres componentes de ADO: **Conexión,** **Comando** y Conjunto **de registros**. El **objeto Connection** permite especificar el nombre del proveedor, las credenciales alternativas, si procede, y otras marcas. El **objeto Command** permite especificar las preferencias de búsqueda y la cadena de consulta. Debe asociar el objeto **Connection** a un **objeto Command** antes de la ejecución de la consulta. Por último, el **objeto Recordset** se usa para iterar el conjunto de resultados.

ADSI admite dos tipos de cadenas de consulta o dialectos. En el ejemplo de código anterior se usa el SQL dialecto. También puede usar el dialecto LDAP. La cadena de consulta del dialecto LDAP se basa en [RFC 2254](https://www.ietf.org/rfc/rfc2254.txt) (una RFC es un documento de solicitud de comentarios, que es la base para desarrollar estándares LDAP). El ejemplo anterior se puede traducir al ejemplo de código siguiente.


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



¿Por qué está la palabra "subárbol" al final de la cadena? En el mundo de los directorios, puede especificar el ámbito de la búsqueda. Las opciones son: "base", "onelevel" y "subárbol". "base" se usa para leer el propio objeto; "onelevel" hace referencia a los secundarios inmediatos, de forma similar al **comando dir;** "subárbol" se usa para buscar en profundidad o hacia abajo varios niveles (similar a **dir /s).**

Con el SQL, puede especificar el ámbito en la propiedad de comando, como en el ejemplo de código siguiente.


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



Si no se especifica scope, usa de forma predeterminada una búsqueda de subárbol.

> [!Note]  
> Si usa C++, puede usar la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) de ADSI.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reorganización](reorganization.md)
</dt> </dl>

 

 




