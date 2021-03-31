---
title: Buscar objetos
description: Julia Bankert debe buscar los números de teléfono de todos los administradores de programas que trabajan en el Departamento 101. Puede crear un script que utilice ADO y ADSI para lograrlo.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- buscar objetos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3c26f05b63524e3a657c0c460efb921978bd19
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103904421"
---
# <a name="searching-for-objects"></a>Buscar objetos

Julia Bankert debe buscar los números de teléfono de todos los administradores de programas que trabajan en el Departamento 101. Puede crear un script que utilice ADO y ADSI para lograrlo.

Cuando se usa el proveedor de ADO para realizar una consulta, el conjunto de resultados solo devolverá los primeros 1000 objetos. Por esta razón, es importante usar una consulta paginada para poder recuperar todos los objetos del conjunto de resultados, siempre que no se haya establecido el servicio de directorio para limitar el número de elementos de un conjunto de resultados. Los conjuntos de valores devueltos contendrán el número de elementos que se especifican en el tamaño de página y se seguirán devolviendo los conjuntos paginados hasta que se devuelvan todos los elementos del conjunto de resultados.


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



Para realizar una búsqueda ADSI en Visual Basic o en un entorno de scripting, se necesitan tres componentes de ADO: **conexión**, **comando** y **conjunto de registros**. El objeto de **conexión** le permite especificar el nombre del proveedor, las credenciales alternativas, si procede, y otras marcas. El objeto de **comando** permite especificar preferencias de búsqueda y la cadena de consulta. Debe asociar el objeto de **conexión** a un objeto de **comando** antes de la ejecución de la consulta. Por último, el objeto de **conjunto de registros** se usa para recorrer en iteración el conjunto de resultados.

ADSI admite dos tipos de cadenas de consulta o dialectos. En el ejemplo de código anterior se usa el dialecto SQL. También puede usar el dialecto LDAP. La cadena de consulta de dialecto LDAP se basa en [rfc 2254](https://www.ietf.org/rfc/rfc2254.txt) (una RFC es una solicitud de documento de comentarios, que es la base para desarrollar estándares LDAP). El ejemplo anterior se puede traducir en el ejemplo de código siguiente.


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



¿Por qué aparece la palabra "subárbol" al final de la cadena? En el mundo del directorio, puede especificar el ámbito de la búsqueda. Las opciones son: "base", "ONELEVEL" y "subárbol". "base" se usa para leer el propio objeto; "ONELEVEL" hace referencia a los elementos secundarios inmediatos, similar al comando **dir** ; "subárbol" se usa para buscar varios niveles en profundidad o descendente (similar a **dir/s**).

Con el dialecto SQL, puede especificar el ámbito en la propiedad Command, como en el ejemplo de código siguiente.


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



Si no se especifica el ámbito, usa de forma predeterminada una búsqueda de subárbol.

> [!Note]  
> Si usa C++, puede usar la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) de ADSI.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reorganización](reorganization.md)
</dt> </dl>

 

 




