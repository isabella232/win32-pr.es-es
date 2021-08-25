---
title: Buscar con ActiveX objetos de datos (ADO)
description: El ActiveX de objetos de datos (ADO) consta de objetos enumerados en la tabla siguiente.
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- ActiveX Objetos de datos ADSI , Buscar con ADO
- Búsqueda con ActiveX ADSI de objetos de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52eba3dd5bc9013500aa4def7a31104d1408d4818b78a35ff75f09f2454f4d21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770455"
---
# <a name="searching-with-activex-data-objects-ado"></a>Buscar con ActiveX objetos de datos (ADO)

El ActiveX de objetos de datos (ADO) consta de objetos enumerados en la tabla siguiente.



| Object         | Descripción                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| **Connection** | Una conexión abierta a un OLE DB de datos como ADSI.                                                                          |
| **Comando**    | Define un comando específico que se ejecutará en el origen de datos.                                                                         |
| **Parámetro**  | Colección opcional para cualquier parámetro que se proporcione al objeto de comando.                                                        |
| **Recordset**  | Un conjunto de registros de una tabla, un objeto de comando o SQL sintaxis. Se puede crear un conjunto de registros sin ningún objeto de conexión subyacente. |
| **Campo**      | Una sola columna de datos en un conjunto de registros.                                                                                            |
| **Propiedad**   | Colección de valores proporcionados por el proveedor para ADO.                                                                           |
| **Error**      | Contiene datos sobre errores de acceso a datos. Se actualiza cuando se produce un error en una sola operación.                                      |



 

Para que ADO se comunique con ADSI, debe haber, al menos, dos objetos ADO: **Connection** y **RecordSet.** Estos objetos ADO sirven para autenticar a los usuarios y enumerar los resultados, respectivamente. Normalmente, también usará un objeto **Command** para mantener una conexión activa, especificar parámetros de consulta, como el tamaño de página y el ámbito de búsqueda, y realizar una consulta. Para obtener más información sobre la sintaxis de filtro de búsqueda, vea [Sintaxis de filtro de búsqueda.](search-filter-syntax.md)

El **objeto Connection** carga el OLE DB y valida las credenciales de usuario. En Visual Basic, llame a la **función CreateObject** con "ADODB. Connection" para crear una instancia de un objeto **Connection** y, a continuación, establezca la propiedad **Provider** del objeto **Connection** en "ADsDSOObject". "ADODB. Connection" es el ProgID del objeto **Connection** y "ADsDSOObject" es el nombre del proveedor OLE DB en ADSI. Si no se especifica ninguna credencial, se usan las credenciales del usuario que ha iniciado sesión actualmente.

En el ejemplo de código siguiente se muestra cómo crear una instancia de un **objeto Connection.**


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



En el ejemplo de código siguiente se muestra cómo crear una instancia de un **objeto Connection.**


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



En el ejemplo de código siguiente se muestra cómo crear una instancia de un **objeto Connection.** Tenga en cuenta que debe incluir la biblioteca de tipos de ADO (msadoXX.dll) como una de las referencias del proyecto Visual Basic.


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



Especifique los datos de autenticación de usuario estableciendo las propiedades del **objeto Connection.** En la tabla siguiente se enumeran las propiedades de autenticación de usuario compatibles con ADSI.



| Propiedad           | Descripción                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Id. de usuario"          | Cadena que identifica al usuario cuyo contexto de seguridad se usa al realizar la búsqueda. Para obtener más información sobre el formato de la cadena de nombre de usuario, vea [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). Si no se especifica, el valor predeterminado es el usuario que ha iniciado sesión o el usuario suplantado por el proceso de llamada. |
| "Password"         | Cadena que especifica la contraseña del usuario identificado por "Id. de usuario".                                                                                                                                                                                                                                                                      |
| "Cifrar contraseña" | Valor booleano que especifica si la contraseña está cifrada. El valor predeterminado es **false**.                                                                                                                                                                                                                                                    |
| "Marca ADSI"        | Conjunto de marcas de la enumeración [**ADS \_ AUTHENTICATION \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) que especifican las opciones de autenticación de enlace. El valor predeterminado es cero.                                                                                                                                                                         |



 

En el ejemplo de código siguiente se muestra cómo se establecen las propiedades antes de crear el **objeto Command.**


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



El segundo objeto ADO es el **objeto Command.** El ProgID del **objeto Command** es "ADODB.Command". Este objeto permite emitir instrucciones de consulta y otros comandos a ADSI mediante la conexión activa. El **objeto Command** usa su propiedad **ActiveConnection** para mantener una conexión activa. También mantiene la propiedad **CommandText** para contener las instrucciones de consulta emitidas por un usuario. Las instrucciones de consulta se expresan en el [dialecto SQL o](sql-dialect.md) [en el dialecto LDAP.](ldap-dialect.md)

En los ejemplos de código siguientes se muestra cómo crear un **objeto Command.**


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



En el ejemplo de código siguiente, incluya la biblioteca de tipos ADO (msadoXX.dll) como una de las referencias.


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



Las opciones de búsqueda **para el objeto Command** se especifican estableciendo la propiedad **Properties.** En la tabla siguiente se enumeran las propiedades con nombre aceptables para **Propiedades**.



| Propiedad con nombre      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Asincrónico"      | Valor booleano que especifica si la búsqueda es sincrónica o asincrónica. El valor predeterminado es False (sincrónico). Una búsqueda sincrónica se bloquea hasta que el servidor devuelve el resultado completo o, para una búsqueda paginada, toda la página. Una búsqueda asincrónica se bloquea hasta que hay disponible una fila de los resultados de la búsqueda o hasta que transcurre el tiempo especificado por la propiedad "Timeout".                           |
| "Resultados de caché"     | Valor booleano que especifica si el resultado debe almacenarse en caché en el lado cliente. El valor predeterminado es **true**; ADSI almacena en caché el conjunto de resultados. Desactivar esta opción puede ser conveniente para conjuntos de resultados grandes.                                                                                                                                                                                                    |
| "Referencias de búsqueda"   | Valor de la [**enumeración \_ ADS REFERRAL \_ REFERRALS \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) que especifica cómo la búsqueda busca referencias. El valor predeterminado es **ADS \_ CHASE \_ REFERRALS \_ NEVER**. Para obtener más información sobre esta propiedad, vea [Referencias](/windows/desktop/AD/referrals).<br/>                                                                                                                                           |
| "Solo nombres de columna" | Valor booleano que indica que la búsqueda debe recuperar solo el nombre de los atributos a los que se han asignado valores. El valor predeterminado es **false**.                                                                                                                                                                                                                                                       |
| "Deref Aliases"     | Valor booleano que especifica si se resuelven los alias de los objetos encontrados. El valor predeterminado es **false**.                                                                                                                                                                                                                                                                                                        |
| "Tamaño de página"         | Valor entero que activa la paginación y especifica el número máximo de objetos que se devuelven en un conjunto de resultados. El valor predeterminado no es ningún tamaño de página. Para obtener más información, vea [Recuperación de conjuntos de resultados grandes](retrieving-large-results-sets.md).                                                                                                                                                                       |
| "SearchScope"       | Valor de la [**enumeración \_ ADS SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) que especifica el ámbito de búsqueda. El valor predeterminado es **ADS \_ SCOPE \_ SUBTREE.**                                                                                                                                                                                                                                                                  |
| "Límite de tamaño"        | Valor entero que especifica el límite de tamaño de la búsqueda. Por Active Directory, el límite de tamaño especifica el número máximo de objetos devueltos. El servidor deja de buscar cuando se alcanza el límite de tamaño y devuelve los resultados acumulados. El valor predeterminado no es ningún límite.                                                                                                                                  |
| "Ordenar"           | Cadena que especifica una lista separada por comas de atributos que se usarán como claves de ordenación. Esta propiedad solo funciona para servidores de directorio que admiten el control LDAP para la ordenación del lado servidor. Active Directory admite el control de ordenación, pero puede afectar al rendimiento del servidor, especialmente si el conjunto de resultados es grande. Tenga en cuenta que Active Directory solo admite una única clave de ordenación. El valor predeterminado no es ninguna ordenación. |
| "Límite de tiempo"        | Valor entero que especifica el límite de tiempo, en segundos, para la búsqueda. Cuando se alcanza el límite de tiempo, el servidor deja de buscar y devuelve los resultados acumulados. El valor predeterminado no es ningún límite de tiempo.                                                                                                                                                                                                      |
| "Tiempo de espera"           | Valor entero que especifica el valor de tiempo de espera del lado cliente, en segundos. Este valor indica el tiempo que el cliente espera los resultados del servidor antes de detener la búsqueda. El valor predeterminado no es tiempo de espera.                                                                                                                                                                                                  |



 

En el ejemplo de código siguiente se muestra cómo establecer opciones de búsqueda.


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



El tercer objeto ADO es **RecordSet.** Este objeto se obtiene al invocar el **método Execute** en un **objeto Command.** La función principal del **objeto RecordSet** es enumerar el conjunto de resultados y obtener los datos. El conjunto de resultados puede contener valores para los atributos que tienen uno o varios valores. Obtener un atributo con un solo valor es sencillo, similar a obtener el valor de columna en la base de datos relacional, por ejemplo:


```VB
Fields('name').Value
```



Sin embargo, obtener un atributo con varios valores es más complicado. En este caso, **Field.Value** es una matriz y debe comprobar el límite inferior y superior de la matriz, como se muestra en el ejemplo de código siguiente.


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



Para obtener más información sobre el modelo de objetos ADO, vea [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).

 

