---
title: Buscar con Objetos de datos ActiveX (ADO)
description: El modelo de objetos de datos ActiveX (ADO) consta de los objetos que se muestran en la tabla siguiente.
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- Objetos de datos ActiveX ADSI, buscar con ADO
- Buscar con Objetos de datos ActiveX ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e73f630892169c7086daf9bb1e7b6c13bfdf0a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656421"
---
# <a name="searching-with-activex-data-objects-ado"></a>Buscar con Objetos de datos ActiveX (ADO)

El modelo de objetos de datos ActiveX (ADO) consta de los objetos que se muestran en la tabla siguiente.



| Object         | Descripción                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| **Connection** | Conexión abierta a un origen de datos de OLE DB, como ADSI.                                                                          |
| **Comando**    | Define un comando específico que se ejecutará en el origen de datos.                                                                         |
| **Parámetro**  | Colección opcional para los parámetros que se van a proporcionar al objeto de comando.                                                        |
| **DataRecordsets**  | Un conjunto de registros de una tabla, un objeto de comando o una sintaxis SQL. Se puede crear un conjunto de registros sin ningún objeto de conexión subyacente. |
| **Campo**      | Una única columna de datos en un conjunto de registros.                                                                                            |
| **Propiedad**   | Colección de valores proporcionados por el proveedor para ADO.                                                                           |
| **Error**      | Contiene datos sobre errores de acceso a datos. Se actualiza cuando se produce un error en una sola operación.                                      |



 

Para que ADO se comunique con ADSI, debe haber, como mínimo, dos objetos ADO: **Connection** y **Recordset**. Estos objetos ADO sirven para autenticar a los usuarios y enumerar los resultados, respectivamente. Normalmente, también usará un objeto de **comando** para mantener una conexión activa, especificar parámetros de consulta, como el tamaño de página y el ámbito de búsqueda, y realizar una consulta. Para obtener más información sobre la sintaxis del filtro de búsqueda, consulte [Sintaxis de filtro de búsqueda](search-filter-syntax.md).

El objeto de **conexión** carga el proveedor de OLE DB y valida las credenciales del usuario. En Visual Basic, llame a la función **CreateObject** con "ADODB. Conexión "para crear una instancia de un objeto de **conexión** y, a continuación, establezca la propiedad **Provider** del objeto de **conexión** en" ADsDSOObject ". ADODB. Connection "es el ProgID del objeto de **conexión** y" ADsDSOObject "es el nombre del proveedor de OLE DB en ADSI. Si no se especifica ninguna credencial, se usan las credenciales del usuario que ha iniciado sesión actualmente.

En el ejemplo de código siguiente se muestra cómo crear una instancia de un objeto de **conexión** .


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



En el ejemplo de código siguiente se muestra cómo crear una instancia de un objeto de **conexión** .


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



En el ejemplo de código siguiente se muestra cómo crear una instancia de un objeto de **conexión** . Tenga en cuenta que debe incluir la biblioteca de tipos de ADO (msadoXX.dll) como una de las referencias del proyecto Visual Basic.


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



Especifique los datos de autenticación del usuario estableciendo las propiedades del objeto de **conexión** . En la tabla siguiente se enumeran las propiedades de autenticación de usuario compatibles con ADSI.



| Propiedad           | Descripción                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "ID. de usuario"          | Cadena que identifica al usuario cuyo contexto de seguridad se utiliza al realizar la búsqueda. Para obtener más información sobre el formato de la cadena de nombre de usuario, vea [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). Si no se especifica, el valor predeterminado es el usuario que ha iniciado sesión o el usuario suplantado por el proceso que realiza la llamada. |
| "Password"         | Una cadena que especifica la contraseña del usuario identificado por "ID. de usuario".                                                                                                                                                                                                                                                                      |
| "Cifrar contraseña" | Valor booleano que especifica si la contraseña está cifrada. El valor predeterminado es **false**.                                                                                                                                                                                                                                                    |
| "Marca ADSI"        | Un conjunto de marcas de la enumeración de la enumeración de [**\_ \_ autenticación ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) que especifican las opciones de autenticación de enlace. El valor predeterminado es cero.                                                                                                                                                                         |



 

En el ejemplo de código siguiente se muestra cómo se establecen las propiedades antes de crear el objeto de **comando** .


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



El segundo objeto de ADO es el objeto de **comando** . El ProgID del objeto **Command** es "ADODB. Command". Este objeto permite emitir instrucciones de consulta y otros comandos para ADSI mediante la conexión activa. El objeto **Command** utiliza su propiedad **ActiveConnection** para mantener una conexión activa. También mantiene la propiedad **CommandText** para contener instrucciones de consulta emitidas por un usuario. Las instrucciones de consulta se expresan en el dialecto [SQL](sql-dialect.md) o en el [dialecto LDAP](ldap-dialect.md).

En los siguientes ejemplos de código se muestra cómo crear un objeto de **comando** .


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



En el ejemplo de código siguiente, se incluye la biblioteca de tipos ADO (msadoXX.dll) como una de las referencias.


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



Las opciones de búsqueda para el objeto de **comando** se especifican estableciendo la propiedad **Properties** . En la tabla siguiente se enumeran las propiedades válidas con nombre para **las propiedades**.



| Propiedad con nombre      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Asincrónica      | Valor booleano que especifica si la búsqueda es sincrónica o asincrónica. El valor predeterminado es false (sincrónico). Una búsqueda sincrónica se bloquea hasta que el servidor devuelve el resultado completo, o para una búsqueda paginada, toda la página. Una búsqueda asincrónica se bloquea hasta que una fila de los resultados de la búsqueda está disponible, o hasta que transcurre el tiempo especificado por la propiedad "timeout".                           |
| "Resultados de caché"     | Valor booleano que especifica si el resultado se debe almacenar en caché en el lado del cliente. El valor predeterminado es **true**; ADSI almacena en caché el conjunto de resultados. Desactivar esta opción puede ser deseable para grandes conjuntos de resultados.                                                                                                                                                                                                    |
| "Referencias de seguimiento"   | Un valor de la [**\_ \_ \_ enumeración de referencias de seguimiento de ADS**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) que especifica cómo la búsqueda realiza las referencias. El valor predeterminado es **ADS \_ seguimiento de \_ referencias \_ nunca**. Para obtener más información sobre esta propiedad, vea [Referrals](/windows/desktop/AD/referrals).<br/>                                                                                                                                           |
| "Solo nombres de columna" | Un valor booleano que indica que la búsqueda debe recuperar solo el nombre de los atributos a los que se han asignado valores. El valor predeterminado es **false**.                                                                                                                                                                                                                                                       |
| "Subaliases de deref"     | Valor booleano que especifica si se resuelven los alias de objetos encontrados. El valor predeterminado es **false**.                                                                                                                                                                                                                                                                                                        |
| "Tamaño de página"         | Valor entero que activa la paginación y especifica el número máximo de objetos que se van a devolver en un conjunto de resultados. El valor predeterminado es sin tamaño de página. Para obtener más información, vea [recuperar grandes conjuntos de resultados](retrieving-large-results-sets.md).                                                                                                                                                                       |
| SearchScope       | Un valor de la enumeración [**ADS \_ SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) que especifica el ámbito de la búsqueda. El valor predeterminado **es \_ \_ subárbol del ámbito de ADS**.                                                                                                                                                                                                                                                                  |
| "Límite de tamaño"        | Valor entero que especifica el límite de tamaño de la búsqueda. Por Active Directory, el límite de tamaño especifica el número máximo de objetos devueltos. El servidor detiene la búsqueda cuando se alcanza el límite de tamaño y devuelve los resultados acumulados. El valor predeterminado es sin límite.                                                                                                                                  |
| "Ordenar por"           | Cadena que especifica una lista separada por comas de atributos que se van a utilizar como claves de ordenación. Esta propiedad solo funciona para los servidores de directorio que admiten el control LDAP para la ordenación del lado servidor. Active Directory admite el control de ordenación, pero puede afectar al rendimiento del servidor, especialmente si el conjunto de resultados es grande. Tenga en cuenta que Active Directory solo admite una única clave de ordenación. El valor predeterminado es ninguna ordenación. |
| "Límite de tiempo"        | Valor entero que especifica el límite de tiempo, en segundos, de la búsqueda. Cuando se alcanza el límite de tiempo, el servidor detiene la búsqueda y devuelve los resultados acumulados. El valor predeterminado es sin límite de tiempo.                                                                                                                                                                                                      |
| Super           | Valor entero que especifica el valor de tiempo de espera del lado cliente, en segundos. Este valor indica el tiempo que el cliente espera los resultados del servidor antes de detener la búsqueda. El valor predeterminado es sin tiempo de espera.                                                                                                                                                                                                  |



 

En el ejemplo de código siguiente se muestra cómo establecer las opciones de búsqueda.


```VB
Const ADS_SCOPE_ONELEVEL = 1
Const ADS_CHASE_REFERRALS_EXTERNAL = &H40

Dim Com As New Command
 
Com.Properties("Page Size") = 999
Com.Properties("Timeout") = 30     ' Seconds
Com.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Com.Properties("Chase referrals") = ADS_CHASE_REFERRALS_EXTERNAL
Com.Properties("Cache Results") = False     ' Do not cache the result set.
```



El tercer objeto ADO es **Recordset**. Este objeto se obtiene al invocar el método **Execute** en un objeto **Command** . La función principal del objeto de **conjunto de registros** es enumerar el conjunto de resultados y obtener los datos. El conjunto de resultados puede contener valores para los atributos que tienen valores únicos o múltiples. Obtener un atributo de un solo valor es sencillo, similar a obtener el valor de la columna en la base de datos relacional, por ejemplo:


```VB
Fields('name').Value
```



La obtención de un atributo con varios valores, sin embargo, es más desafiante. En este caso, el **campo. Value** es una matriz y debe comprobar el límite inferior y superior de la matriz, como se muestra en el ejemplo de código siguiente.


```VB
Set rs = Com.Execute
 
For i = 0 To rs.Fields.Count - 1
    Debug.Print rs.Fields(i).Name, rs.Fields(i).Type
Next i
 
'--------------------------
' Navigate the record set.
'--------------------------
rs.MoveFirst
lstResult.Clear      ' Clear the user interface.
While Not rs.EOF
For i = 0 To rs.Fields.Count - 1
    ' For Multi Value attribute
    If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
        Debug.Print rs.Fields(i).Name, " = "
        For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
            Debug.Print rs.Fields(i).Value(j), " # "
            lstResult.AddItem rs.Fields(i).Value(j)
        Next j
    Else
        ' For Single Value attribute.
         Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
         lstResult.AddItem rs.Fields(i).Value
    End If
Next i
rs.MoveNext
Wend
```



En el ejemplo de código siguiente se deshabilitan las cuentas de usuario en un servidor LDAP.


```VB
Dim X as IADs
Dim con As New Connection, rs As New Recordset
Dim MyUser As IADsUser
 
con.Provider = "ADsDSOObject"
con.Open "Active Directory Provider", "CN=Test,CN=Users,DC=Fabrikam,DC=COM,O=INTERNET", "Password"
Set rs = con.Execute("<LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com>;(objectClass=User);ADsPath;onelevel")
 
While Not rs.EOF
    ' Bind to the object to make changes 
    ' to it because ADO is currently read-only.
    MyUser = GetObject(rs.Fields(0).Value)
    MyUser.AccountDisabled = True
    MyUser.SetInfo
    rs.MoveNext
Wend
```



Para obtener más información sobre el modelo de objetos ADO, vea [Microsoft objetos de datos ActiveX](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).

 

