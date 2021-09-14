---
title: Dialecto LDAP
description: El dialecto LDAP es un formato para las instrucciones de consulta que usan la sintaxis de filtro de búsqueda LDAP.
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- LDAP Dialect ADSI
- dialectos ADSI, dialecto LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f7d1f65a41655596d0a14cf6e2a3595916c2cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172190"
---
# <a name="ldap-dialect"></a>Dialecto LDAP

El dialecto LDAP es un formato para las instrucciones de consulta que usan la sintaxis [de filtro de búsqueda LDAP](search-filter-syntax.md). Use una instrucción de consulta LDAP con las siguientes interfaces de búsqueda ADSI:

-   Las [ActiveX de objetos de datos (ADO),](searching-with-activex-data-objects-ado.md) que son interfaces de Automation que usan OLE DB.
-   [OLE DB](searching-with-ole-db.md), que es un conjunto de interfaces de C/C++ para consultar bases de datos.
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), que es la interfaz de C/C++ para Active Directory.

Una cadena de dialecto LDAP consta de cuatro partes separadas por punto y coma (;).

-   Nombre distintivo base. Por ejemplo:

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   Filtros de búsqueda LDAP. Para obtener más información sobre los filtros de búsqueda, vea [Sintaxis de filtro de búsqueda.](search-filter-syntax.md)
-   Nombre para mostrar LDAP de los atributos que se recuperarán. Varios atributos están separados por una coma.
-   Especifica el ámbito de la búsqueda. Los valores válidos son "base", "onelevel" y "subárbol". El ámbito especificado en una cadena de consulta LDAP invalida cualquier ámbito de búsqueda especificado con la propiedad "SearchScope" del objeto ADO Command.

A continuación se muestra un ejemplo de código del dialecto LDAP en ADSI que busca todos los objetos del subárbol.


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



No todas las opciones de búsqueda (tamaño de página de búsqueda, por ejemplo) se pueden expresar en el dialecto LDAP, por lo que debe establecer las opciones antes de que se inicie la ejecución real de la consulta.

## <a name="example-code-for-performing-an-ldap-query"></a>Código de ejemplo para realizar una consulta LDAP

En el ejemplo de código siguiente se muestra cómo usar una consulta LDAP


```VB
Dim con As New Connection, rs As New Recordset
Dim adVariant
Dim i 'Used for counter
Dim j 'Used for counter
Dim Com As New Command
Dim strDomain As String
Dim strPassword As String
 
' Open a Connection object.
con.Provider = "ADsDSOObject"
con.Properties("ADSI Flag") = 1
con.Properties("User ID") = strDomain + "\" + strUserID
con.Properties("Password") = strPassword

con.Open "Active Directory Provider"
 
' Create a command object on this connection.
Set Com.ActiveConnection = con
 
' Set the query string.
Com.CommandText = "<LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com>;
     (objectClass=*);ADsPath, objectclass;base"
 
' Set search preferences.
Com.Properties("Page Size") = 1000
Com.Properties("Timeout") = 30 'seconds
 
' Execute the query.
Set rs = Com.Execute
 
' Navigate the record set.
rs.MoveFirst
While Not rs.EOF
    For i = 0 To rs.Fields.Count - 1
        If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
            Debug.Print rs.Fields(i).Name, " = "
            For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
                Debug.Print rs.Fields(i).Value(j), " # "
            Next j
        Else
            Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
        End If
    Next i
    rs.MoveNext
Wend
 
rs.MoveLast
Debug.Print "No. of rows = ", rs.RecordCount
```



Para obtener más información sobre la sintaxis de consulta, vea [Sintaxis de filtro de búsqueda.](search-filter-syntax.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis de filtro de búsqueda](search-filter-syntax.md)
</dt> <dt>

[SQL dialecto](sql-dialect.md)
</dt> <dt>

[Búsqueda con la interfaz IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Buscar con objetos ActiveX datos](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Buscar con OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




