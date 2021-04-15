---
description: Hay varias maneras de usar Windows Search para consultar el índice. En este tema se describen los enfoques basados en la sintaxis de consulta avanzada (AQS) y Lenguaje de consulta estructurado (SQL).
ms.assetid: 544f03b3-cdf8-4550-a6da-e4a3bfc44744
title: Uso de enfoques de SQL y AQS para consultar el índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641bea0e6109182b5896aa1f0f981695fd91b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696253"
---
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a>Uso de enfoques de SQL y AQS para consultar el índice

Hay varias maneras de usar Windows Search para consultar el índice. En este tema se describen los enfoques basados en la sintaxis de consulta avanzada (AQS) y Lenguaje de consulta estructurado (SQL).

Este tema se organiza de la siguiente manera:

- [Consultas basadas en SQL](#sql-based-queries)
  - [Usar OLE DB](#using-ole-db)
  - [Usar ADO y ADO.NET](#using-ado-and-adonet)
  - [Usar SQL en consultas locales y remotas](#using-sql-in-local-and-remote-queries)
- [Consultas basadas en AQS](#aqs-based-queries)
  - [Usar ISearchQueryHelper](#using-isearchqueryhelper)
  - [Uso del protocolo Search-MS](#using-the-search-ms-protocol)
- [Temas relacionados](#related-topics)

## <a name="sql-based-queries"></a>Consultas basadas en SQL

SQL es un lenguaje de texto que define las consultas. SQL es común en muchas tecnologías de base de datos diferentes. Windows Search usa SQL, implementa un subconjunto del mismo y lo amplía agregando elementos al lenguaje. El SQL de búsqueda de Windows que usa Windows Search extiende partes de la sintaxis de consulta de base de datos SQL-92 y SQL-99 para mejorar su utilidad con las búsquedas basadas en texto. Todas las características de Windows Search SQL son compatibles con Windows Search en Windows XP y Windows Server 2003 y versiones posteriores.

Para obtener más información acerca del uso de la sintaxis SQL de Windows Search, vea [consultar el índice con la sintaxis SQL](-search-sql-windowssearch-entry.md) de Windows Search e [información general sobre la sintaxis SQL de Windows Search](-search-sql-ovwofsearchquery.md).

Los siguientes enfoques para consultar el índice se basan en SQL.

### <a name="using-ole-db"></a>Usar OLE DB

La base de datos de vinculación e incrustación de objetos (OLE DB) es una API del modelo de objetos componentes (COM) que permite tener acceso a diferentes tipos de almacenes de datos de manera uniforme, incluidas bases de datos no relacionales, como hojas de cálculo. OLE DB separa el almacén de datos de la aplicación que obtiene acceso a él a través de un conjunto de abstracciones que incluyen el origen de datos del shell, la sesión, el comando y los conjuntos de filas. Un proveedor de OLE DB es un componente de software que implementa la interfaz de OLE DB para proporcionar datos a las aplicaciones de un almacén de datos determinado.

Puede tener acceso al proveedor de OLE DB de Windows Search mediante programación usando los objetos OleDbConnection y OleDbSession en C \# y utilizando la compatibilidad de OLE DB integrada en Active Template Library (ATL) en C++ (a través de atlclidb. h). La única propiedad que se debe establecer es la cadena del proveedor.

Puede usar la siguiente cadena:

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

Como alternativa, puede obtener la cadena de conexión mediante una llamada a [**ISearchQueryHelper:: get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring). Vea uso de [ISearchQueryHelper](#using-isearchqueryhelper) para obtener un ejemplo.

> [!Note]  
> El proveedor de OLE DB de Windows Search es de solo lectura y admite instrucciones SELECT y GROUP ON. No se admiten las instrucciones INSERT y DELETE.

```cpp
#include <atldbcli.h>
CDataSource cDataSource;
hr = cDataSource.OpenFromInitializationString(L"provider=Search.CollatorDSO.1;EXTENDED PROPERTIES=\"Application=Windows\"");

if (SUCCEEDED(hr))
{
    CSession cSession;
    hr = cSession.Open(cDataSource);

    if (SUCCEEDED(hr))
    {
        CCommand<CDynamicAccessor, CRowset> cCommand;
        hr = cCommand.Open(cSession, pszSQL);

        if (SUCCEEDED(hr))
        {
            for (hr = cCommand.MoveFirst(); S_OK == hr; hr = cCommand.MoveNext())
            {
                for (DBORDINAL i = 1; i <= cCommand.GetColumnCount(); i++)
                {
                    PCWSTR pszName = cCommand.GetColumnName(i);
                    // do something with the column here
                }
            }
            cCommand.Close();
        }
    }
}
```

Para obtener más información sobre OLE DB, consulte [información general](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx)sobre la programación de OLE DB. Para obtener información sobre el proveedor de datos de .NET Framework para OLE DB, consulte la documentación del [espacio de nombres System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .

### <a name="using-ado-and-adonet"></a>Usar ADO y ADO.NET

Microsoft Objetos de datos ActiveX (ADO) y ADO.NET le permiten escribir aplicaciones cliente para tener acceso a los datos de un servidor de base de datos y manipularlos a través de un proveedor. Windows Search es una tecnología de solo lectura: puede recuperar datos mediante la búsqueda en el escritorio, pero no puede cambiar los datos mediante la búsqueda de Windows. Sin embargo, puede pasar los resultados de una búsqueda a una tecnología que pueda cambiar los datos.

En los siguientes ejemplos de código se muestra cómo abrir una conexión al origen de datos, crear y abrir un conjunto de registros con una instrucción SQL SELECT de [Windows Search](-search-sql-ovwofsearchquery.md) y obtener las direcciones URL de los cinco archivos más grandes del índice.

> [!Note]  
> Para obtener información sobre cómo obtener la cadena de conexión, vea [consultar el índice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)y [ISearchQueryHelper:: get \_ Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).

#### <a name="ado-and-vbscript"></a>ADO y VBScript

```VB
'To run this snippet, save it to a file and run it using cscript.exe from a command line.
'Running the .vbs file with Windows Script Host may cause dialog boxes to open for each item returned from the index.

On Error Resume Next

Set objConnection = CreateObject("ADODB.Connection")
Set objRecordSet = CreateObject("ADODB.Recordset")

objConnection.Open "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"

objRecordSet.Open "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC", objConnection

objRecordSet.MoveFirst
Do Until objRecordset.EOF
    Wscript.Echo objRecordset.Fields.Item("System.ItemPathDisplay")
    objRecordset.MoveNext
Loop
```

#### <a name="ado-and-c"></a>ADO y C++

```cpp
#import "msado15.dll" rename_namespace("ADO") rename("EOF", "EndOfFile") implementation_only

ADO::_ConnectionPtr connection = NULL;
HRESULT hr = connection.CreateInstance(__uuidof(ADO::Connection));
if (SUCCEEDED(hr))
{
    ADO::_RecordsetPtr recordset = NULL;
    hr = recordset.CreateInstance(__uuidof(ADO::Recordset));
    if (SUCCEEDED(hr))
    {
        connection->CursorLocation = ADO::adUseClient;
        hr = connection->Open(L"Provider=Search.CollatorDSO;Extended Properties='Application=Windows';",
            L"", L"", ADO::adConnectUnspecified);
        if (SUCCEEDED(hr))
        {
            hr = recordset->Open("SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC",
            connection.GetInterfacePtr(), ADO::adOpenForwardOnly, ADO::adLockReadOnly, ADO::adCmdText);
            if (SUCCEEDED(hr))
            {
                while (!recordset->EndOfFile)
                {
                    _variant_t var;
                    var = recordset->Fields->GetItem(L"System.ItemPathDisplay")->GetValue();
                    std::cout << static_cast<char *>(_bstr_t(var.bstrVal)) << std::endl;
                    recordset->MoveNext();
                };
                recordset->Close();
            }
            connection->Close();
        }
    }
}

```

#### <a name="ado-and-visualbasic"></a>ADO y VisualBasic

Agregue primero una referencia a ADODB en el proyecto

```VB
Dim con As ADODB.Connection
Dim rst As ADODB.Recordset

con = New ADODB.Connection
rst = New ADODB.Recordset

Dim sConString As String
Dim sSQLString As String

sConString = "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"
con.Open(sConString)

sSQLString = "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC"

rst = con.Execute(sSQLString)

Do Until (rst.EOF)
    Print(1, rst("System.ItemPathDisplay").Value)
    rst.MoveNext
Loop

rst.Close
rst = Nothing

con.Close
con = Nothing
```

#### <a name="adonet-and-c"></a>ADO.NET y C\#

```csharp
string query = @"SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC";

using (OleDbConnection objConnection =
    new OleDbConnection
    ("Provider=Search.CollatorDSO.1;Extended?Properties='Application=Windows';"))
{
    objConnection.Open();
    OleDbCommand cmd = new OleDbCommand(query, objConnection);
    using (OleDbDataReader rdr = cmd.ExecuteReader())
    {
        for (int i = 0; i < rdr.FieldCount; i++)
        {
            Console.Write(rdr.GetName(i));
            Console.Write('\t');
        }
        while (rdr.Read())
        {
            Console.WriteLine();
            for (int i = 0; i < rdr.FieldCount; i++)
            {
                Console.Write(rdr[i]);
                Console.Write('\t');
            }
        }
        Console.ReadKey();
    }
}
```

### <a name="using-sql-in-local-and-remote-queries"></a>Usar SQL en consultas locales y remotas

Puede ejecutar las consultas de forma local o remota. En el ejemplo siguiente se muestra una consulta local con la [cláusula FROM](-search-sql-from.md) . Una consulta local solo consulta el catálogo SystemIndex local.

```sql
FROM SystemIndex
```

En el ejemplo siguiente se muestra una consulta remota con la [cláusula FROM](-search-sql-from.md) . Al agregar ComputerName, se transforma el ejemplo anterior en una consulta remota.

```sql
FROM [<ComputerName>.]SystemIndex
```

De forma predeterminada, Windows XP y Windows Server 2003 no tienen instalado Windows Search. Solo Windows Search 4 (WS4) proporciona compatibilidad con consultas remotas. Las versiones anteriores de la búsqueda de escritorio de Windows (WDS), como 3,01 y versiones anteriores, no admiten las consultas remotas. Con el explorador de Windows puede consultar el índice local de un equipo remoto para los elementos del sistema de archivos (elementos administrados por el protocolo "File:").

Para recuperar un elemento mediante una consulta remota, el elemento debe cumplir los siguientes requisitos:

- Ser accesible a través de la ruta de acceso UNC (Convención de nomenclatura universal).
- Existe en el equipo remoto al que el cliente tiene acceso.
- Tenga su seguridad establecida para permitir que el cliente tenga acceso de lectura.

El explorador de Windows tiene características para compartir elementos, incluido un recurso compartido "público" ( \\ \\ equipo \\ público \\ ...) en el **centro de redes y recursos compartidos**, y un recurso compartido de "usuarios" ( \\ \\ \\ usuarios \\ de la máquina...) para elementos compartidos mediante el Asistente para compartir. Después de compartir las carpetas, puede consultar el índice local especificando el nombre del equipo del equipo remoto en la cláusula FROM y una ruta de acceso UNC en el equipo remoto en la cláusula SCOPE, tal como se muestra en el ejemplo siguiente:

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a>Consultas basadas en AQS

AQS es la sintaxis de consulta predeterminada que usa Windows Search para consultar el índice y para refinar y restringir los parámetros de búsqueda. Aunque AQS está dirigido principalmente a los usuarios, los desarrolladores pueden usarlos para crear consultas mediante programación. En Windows 7, se presentó una AQS canónica y se debe usar en Windows 7 y versiones posteriores, para generar consultas AQS mediante programación. Para obtener información detallada sobre AQS, consulte [usar la sintaxis de consulta avanzada mediante programación](-search-3x-advancedquerysyntax.md).

Los siguientes enfoques para consultar el índice se basan en AQS.

### <a name="using-isearchqueryhelper"></a>Usar ISearchQueryHelper

Puede desarrollar un componente o una clase auxiliar para consultar el índice mediante la interfaz [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , que le permite aprovechar algunas características del sistema y simplificar el uso de Windows Search. Esta interfaz le ayuda a:

- Obtenga una cadena de conexión OLE DB para conectarse a la base de datos de Windows Search.
- Convierta las consultas de usuario de AQS a SQL de búsqueda de Windows.

Esta interfaz se implementa como una clase auxiliar en [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) y se obtiene llamando a [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), como se muestra en el siguiente ejemplo de C++.

```cpp
HRESULT GetQueryHelper(ISearchQueryHelper **ppQueryHelper)
{
    *ppQueryHelper = NULL;

    // Create an instance of the search manager

    ISearchManager *pSearchManager;
    HRESULT hr = CoCreateInstance(__uuidof(CSearchManager), NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));
    if (SUCCEEDED(hr))
    {
        // Get the catalog manager from the search manager
        ISearchCatalogManager *pSearchCatalogManager;
        hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
        if (SUCCEEDED(hr))
        {
            // Get the query helper from the catalog manager
            hr = pSearchCatalogManager->GetQueryHelper(ppQueryHelper);
            pSearchCatalogManager->Release();
        }
        pSearchManager->Release();
    }

    return hr;
}
```

Para implementar la interfaz [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , consulte [uso de la interfaz ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md) y el tema de referencia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .

> [!Note]  
> Compatibilidad con la versión de Microsoft Windows Desktop Search (WDS) 2x heredada: en los equipos que ejecutan Windows XP y Windows Server 2003 y versiones posteriores, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) está en desuso. En su lugar, los desarrolladores deben usar [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para obtener una cadena de conexión, analizar la consulta del usuario en SQL y, a continuación, consultar OLE DB.

### <a name="using-the-search-ms-protocol"></a>Uso del protocolo Search-MS

**Search-MS** [Application Protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) es una Convención para iniciar una aplicación, como el explorador de Windows, para consultar el índice de Windows Search. Permite que las consultas se compilen con argumentos de valor de parámetro, incluidos los argumentos de propiedad, las búsquedas guardadas anteriormente, la sintaxis de consulta avanzada (AQS), la sintaxis de consulta natural (NQS) y los identificadores de código de idioma (LCID) del indexador y la propia consulta.

Para obtener información detallada sobre la sintaxis del protocolo Search-MS, consulte [consultar el índice con el protocolo Search-MS](-search-3x-wds-qryidx-searchms.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consulta del índice mediante programación](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Consultar el índice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Consultar el índice con el protocolo Search-MS](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Consultar el índice con la sintaxis SQL de Windows Search](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Usar la sintaxis de consulta avanzada mediante programación](-search-3x-advancedquerysyntax.md)
</dt> </dl>
