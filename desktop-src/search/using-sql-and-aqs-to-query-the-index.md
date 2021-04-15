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
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a><span data-ttu-id="3c9c3-104">Uso de enfoques de SQL y AQS para consultar el índice</span><span class="sxs-lookup"><span data-stu-id="3c9c3-104">Using SQL and AQS Approaches to Query the Index</span></span>

<span data-ttu-id="3c9c3-105">Hay varias maneras de usar Windows Search para consultar el índice.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-105">There are several ways to use Windows Search to query the index.</span></span> <span data-ttu-id="3c9c3-106">En este tema se describen los enfoques basados en la sintaxis de consulta avanzada (AQS) y Lenguaje de consulta estructurado (SQL).</span><span class="sxs-lookup"><span data-stu-id="3c9c3-106">This topic outlines Advanced Query Syntax (AQS) and Structured Query Language (SQL) based approaches.</span></span>

<span data-ttu-id="3c9c3-107">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="3c9c3-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="3c9c3-108">Consultas basadas en SQL</span><span class="sxs-lookup"><span data-stu-id="3c9c3-108">SQL Based Queries</span></span>](#sql-based-queries)
  - [<span data-ttu-id="3c9c3-109">Usar OLE DB</span><span class="sxs-lookup"><span data-stu-id="3c9c3-109">Using OLE DB</span></span>](#using-ole-db)
  - [<span data-ttu-id="3c9c3-110">Usar ADO y ADO.NET</span><span class="sxs-lookup"><span data-stu-id="3c9c3-110">Using ADO and ADO.NET</span></span>](#using-ado-and-adonet)
  - [<span data-ttu-id="3c9c3-111">Usar SQL en consultas locales y remotas</span><span class="sxs-lookup"><span data-stu-id="3c9c3-111">Using SQL in Local and Remote Queries</span></span>](#using-sql-in-local-and-remote-queries)
- [<span data-ttu-id="3c9c3-112">Consultas basadas en AQS</span><span class="sxs-lookup"><span data-stu-id="3c9c3-112">AQS Based Queries</span></span>](#aqs-based-queries)
  - [<span data-ttu-id="3c9c3-113">Usar ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="3c9c3-113">Using ISearchQueryHelper</span></span>](#using-isearchqueryhelper)
  - [<span data-ttu-id="3c9c3-114">Uso del protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="3c9c3-114">Using the search-ms Protocol</span></span>](#using-the-search-ms-protocol)
- [<span data-ttu-id="3c9c3-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c9c3-115">Related topics</span></span>](#related-topics)

## <a name="sql-based-queries"></a><span data-ttu-id="3c9c3-116">Consultas basadas en SQL</span><span class="sxs-lookup"><span data-stu-id="3c9c3-116">SQL Based Queries</span></span>

<span data-ttu-id="3c9c3-117">SQL es un lenguaje de texto que define las consultas.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-117">SQL is a text language that defines queries.</span></span> <span data-ttu-id="3c9c3-118">SQL es común en muchas tecnologías de base de datos diferentes.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-118">SQL is common across many different database technologies.</span></span> <span data-ttu-id="3c9c3-119">Windows Search usa SQL, implementa un subconjunto del mismo y lo amplía agregando elementos al lenguaje.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-119">Windows Search uses SQL, implements a subset of it, and extends it by adding elements to the language.</span></span> <span data-ttu-id="3c9c3-120">El SQL de búsqueda de Windows que usa Windows Search extiende partes de la sintaxis de consulta de base de datos SQL-92 y SQL-99 para mejorar su utilidad con las búsquedas basadas en texto.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-120">The Windows Search SQL used by Windows Search extends portions of the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span> <span data-ttu-id="3c9c3-121">Todas las características de Windows Search SQL son compatibles con Windows Search en Windows XP y Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-121">All features of Windows Search SQL are compatible with Windows Search on Windows XP and Windows Server 2003, and later.</span></span>

<span data-ttu-id="3c9c3-122">Para obtener más información acerca del uso de la sintaxis SQL de Windows Search, vea [consultar el índice con la sintaxis SQL](-search-sql-windowssearch-entry.md) de Windows Search e [información general sobre la sintaxis SQL de Windows Search](-search-sql-ovwofsearchquery.md).</span><span class="sxs-lookup"><span data-stu-id="3c9c3-122">For more information about using Windows Search SQL syntax, see [Querying the Index with Windows Search SQL Syntax](-search-sql-windowssearch-entry.md) and [Overview of Windows Search SQL Syntax](-search-sql-ovwofsearchquery.md).</span></span>

<span data-ttu-id="3c9c3-123">Los siguientes enfoques para consultar el índice se basan en SQL.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-123">The following approaches for querying the index are SQL based.</span></span>

### <a name="using-ole-db"></a><span data-ttu-id="3c9c3-124">Usar OLE DB</span><span class="sxs-lookup"><span data-stu-id="3c9c3-124">Using OLE DB</span></span>

<span data-ttu-id="3c9c3-125">La base de datos de vinculación e incrustación de objetos (OLE DB) es una API del modelo de objetos componentes (COM) que permite tener acceso a diferentes tipos de almacenes de datos de manera uniforme, incluidas bases de datos no relacionales, como hojas de cálculo.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-125">The Object Linking and Embedding Database (OLE DB) is a Component Object Model (COM) API that enables you to access different types of data stores uniformly, including non-relational databases like spreadsheets.</span></span> <span data-ttu-id="3c9c3-126">OLE DB separa el almacén de datos de la aplicación que obtiene acceso a él a través de un conjunto de abstracciones que incluyen el origen de datos del shell, la sesión, el comando y los conjuntos de filas.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-126">OLE DB separates the data store from the application accessing it through a set of abstractions that include the Shell data source, session, command, and rowsets.</span></span> <span data-ttu-id="3c9c3-127">Un proveedor de OLE DB es un componente de software que implementa la interfaz de OLE DB para proporcionar datos a las aplicaciones de un almacén de datos determinado.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-127">An OLE DB provider is a software component that implements the OLE DB interface to provide data to applications from a particular data store.</span></span>

<span data-ttu-id="3c9c3-128">Puede tener acceso al proveedor de OLE DB de Windows Search mediante programación usando los objetos OleDbConnection y OleDbSession en C \# y utilizando la compatibilidad de OLE DB integrada en Active Template Library (ATL) en C++ (a través de atlclidb. h).</span><span class="sxs-lookup"><span data-stu-id="3c9c3-128">You can access the Windows Search OLE DB provider programmatically by using the OleDbConnection and OleDbSession objects in C\# and by using the OLE DB support built into Active Template Library (ATL) in C++ (via atlclidb.h).</span></span> <span data-ttu-id="3c9c3-129">La única propiedad que se debe establecer es la cadena del proveedor.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-129">The only property that has to be set is the provider string.</span></span>

<span data-ttu-id="3c9c3-130">Puede usar la siguiente cadena:</span><span class="sxs-lookup"><span data-stu-id="3c9c3-130">You can use the following string:</span></span>

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

<span data-ttu-id="3c9c3-131">Como alternativa, puede obtener la cadena de conexión mediante una llamada a [**ISearchQueryHelper:: get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span><span class="sxs-lookup"><span data-stu-id="3c9c3-131">Alternatively, you can get the connection string by calling [**ISearchQueryHelper::get\_ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span> <span data-ttu-id="3c9c3-132">Vea uso de [ISearchQueryHelper](#using-isearchqueryhelper) para obtener un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-132">See Using [ISearchQueryHelper](#using-isearchqueryhelper) for an example.</span></span>

> [!Note]  
> <span data-ttu-id="3c9c3-133">El proveedor de OLE DB de Windows Search es de solo lectura y admite instrucciones SELECT y GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-133">The Windows Search OLE DB provider is read-only, and support SELECT and GROUP ON statements.</span></span> <span data-ttu-id="3c9c3-134">No se admiten las instrucciones INSERT y DELETE.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-134">INSERT and DELETE statements are not supported.</span></span>

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

<span data-ttu-id="3c9c3-135">Para obtener más información sobre OLE DB, consulte [información general](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx)sobre la programación de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-135">For more information on OLE DB, see [OLE DB Programming Overview](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx).</span></span> <span data-ttu-id="3c9c3-136">Para obtener información sobre el proveedor de datos de .NET Framework para OLE DB, consulte la documentación del [espacio de nombres System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .</span><span class="sxs-lookup"><span data-stu-id="3c9c3-136">For information on the .NET Framework Data Provider for OLE DB, see the [System.Data.OleDb Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) documentation.</span></span>

### <a name="using-ado-and-adonet"></a><span data-ttu-id="3c9c3-137">Usar ADO y ADO.NET</span><span class="sxs-lookup"><span data-stu-id="3c9c3-137">Using ADO and ADO.NET</span></span>

<span data-ttu-id="3c9c3-138">Microsoft Objetos de datos ActiveX (ADO) y ADO.NET le permiten escribir aplicaciones cliente para tener acceso a los datos de un servidor de base de datos y manipularlos a través de un proveedor.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-138">Microsoft ActiveX Data Objects (ADO) and ADO.NET enable you to write client applications to access and manipulate data in a database server through a provider.</span></span> <span data-ttu-id="3c9c3-139">Windows Search es una tecnología de solo lectura: puede recuperar datos mediante la búsqueda en el escritorio, pero no puede cambiar los datos mediante la búsqueda de Windows.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-139">Windows Search is a read-only technology: you can retrieve data using Desktop Search but you can't change data using Windows Search.</span></span> <span data-ttu-id="3c9c3-140">Sin embargo, puede pasar los resultados de una búsqueda a una tecnología que pueda cambiar los datos.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-140">You can, however, pass the results of a search over to a technology that can change data.</span></span>

<span data-ttu-id="3c9c3-141">En los siguientes ejemplos de código se muestra cómo abrir una conexión al origen de datos, crear y abrir un conjunto de registros con una instrucción SQL SELECT de [Windows Search](-search-sql-ovwofsearchquery.md) y obtener las direcciones URL de los cinco archivos más grandes del índice.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-141">The following code examples demonstrate how to open a connection to the data source, create and open a RecordSet with a [Windows Search SQL](-search-sql-ovwofsearchquery.md) SELECT statement, and get the URLs of the five largest files from the index.</span></span>

> [!Note]  
> <span data-ttu-id="3c9c3-142">Para obtener información sobre cómo obtener la cadena de conexión, vea [consultar el índice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)y [ISearchQueryHelper:: get \_ Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span><span class="sxs-lookup"><span data-stu-id="3c9c3-142">For information on how to obtain the connection string, see [Querying the Index with ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md), and [ISearchQueryHelper::get\_Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span>

#### <a name="ado-and-vbscript"></a><span data-ttu-id="3c9c3-143">ADO y VBScript</span><span class="sxs-lookup"><span data-stu-id="3c9c3-143">ADO and VBScript</span></span>

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

#### <a name="ado-and-c"></a><span data-ttu-id="3c9c3-144">ADO y C++</span><span class="sxs-lookup"><span data-stu-id="3c9c3-144">ADO and C++</span></span>

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

#### <a name="ado-and-visualbasic"></a><span data-ttu-id="3c9c3-145">ADO y VisualBasic</span><span class="sxs-lookup"><span data-stu-id="3c9c3-145">ADO and VisualBasic</span></span>

<span data-ttu-id="3c9c3-146">Agregue primero una referencia a ADODB en el proyecto</span><span class="sxs-lookup"><span data-stu-id="3c9c3-146">First add a reference to ADODB in your project</span></span>

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

#### <a name="adonet-and-c"></a><span data-ttu-id="3c9c3-147">ADO.NET y C\#</span><span class="sxs-lookup"><span data-stu-id="3c9c3-147">ADO.NET and C\#</span></span>

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

### <a name="using-sql-in-local-and-remote-queries"></a><span data-ttu-id="3c9c3-148">Usar SQL en consultas locales y remotas</span><span class="sxs-lookup"><span data-stu-id="3c9c3-148">Using SQL in Local and Remote Queries</span></span>

<span data-ttu-id="3c9c3-149">Puede ejecutar las consultas de forma local o remota.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-149">You can execute your queries either locally or remotely.</span></span> <span data-ttu-id="3c9c3-150">En el ejemplo siguiente se muestra una consulta local con la [cláusula FROM](-search-sql-from.md) .</span><span class="sxs-lookup"><span data-stu-id="3c9c3-150">A local query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="3c9c3-151">Una consulta local solo consulta el catálogo SystemIndex local.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-151">A local query queries the local SystemIndex catalog only.</span></span>

```sql
FROM SystemIndex
```

<span data-ttu-id="3c9c3-152">En el ejemplo siguiente se muestra una consulta remota con la [cláusula FROM](-search-sql-from.md) .</span><span class="sxs-lookup"><span data-stu-id="3c9c3-152">A remote query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="3c9c3-153">Al agregar ComputerName, se transforma el ejemplo anterior en una consulta remota.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-153">Adding ComputerName transforms the previous example into a remote query.</span></span>

```sql
FROM [<ComputerName>.]SystemIndex
```

<span data-ttu-id="3c9c3-154">De forma predeterminada, Windows XP y Windows Server 2003 no tienen instalado Windows Search.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-154">By default, Windows XP and Windows Server 2003 do not have Windows Search installed.</span></span> <span data-ttu-id="3c9c3-155">Solo Windows Search 4 (WS4) proporciona compatibilidad con consultas remotas.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-155">Only Windows Search 4 (WS4) provides remote query support.</span></span> <span data-ttu-id="3c9c3-156">Las versiones anteriores de la búsqueda de escritorio de Windows (WDS), como 3,01 y versiones anteriores, no admiten las consultas remotas.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-156">Previous versions of Windows Desktop Search (WDS), such as 3.01 and earlier, do not support remote querying.</span></span> <span data-ttu-id="3c9c3-157">Con el explorador de Windows puede consultar el índice local de un equipo remoto para los elementos del sistema de archivos (elementos administrados por el protocolo "File:").</span><span class="sxs-lookup"><span data-stu-id="3c9c3-157">With Windows Explorer you can query the local index of a remote computer for file system items (items handled by the "file:" protocol).</span></span>

<span data-ttu-id="3c9c3-158">Para recuperar un elemento mediante una consulta remota, el elemento debe cumplir los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="3c9c3-158">To retrieve an item by remote query, the item must meet the following requirements:</span></span>

- <span data-ttu-id="3c9c3-159">Ser accesible a través de la ruta de acceso UNC (Convención de nomenclatura universal).</span><span class="sxs-lookup"><span data-stu-id="3c9c3-159">Be accessible via Universal Naming Convention (UNC) path.</span></span>
- <span data-ttu-id="3c9c3-160">Existe en el equipo remoto al que el cliente tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-160">Exist on the remote computer to which the client has access.</span></span>
- <span data-ttu-id="3c9c3-161">Tenga su seguridad establecida para permitir que el cliente tenga acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-161">Have its security set to allow the client to have Read access.</span></span>

<span data-ttu-id="3c9c3-162">El explorador de Windows tiene características para compartir elementos, incluido un recurso compartido "público" ( \\ \\ equipo \\ público \\ ...) en el **centro de redes y recursos compartidos**, y un recurso compartido de "usuarios" ( \\ \\ \\ usuarios \\ de la máquina...) para elementos compartidos mediante el Asistente para compartir.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-162">Windows Explorer has features for sharing items including a "Public" share (\\\\Machine\\Public\\...) in the **Network and Sharing Center**, and a "Users" share (\\\\Machine\\Users\\...) for items shared through the Sharing Wizard.</span></span> <span data-ttu-id="3c9c3-163">Después de compartir las carpetas, puede consultar el índice local especificando el nombre del equipo del equipo remoto en la cláusula FROM y una ruta de acceso UNC en el equipo remoto en la cláusula SCOPE, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3c9c3-163">After you share the folder(s), you can query the local index by specifying the remote computer's machine name in the FROM clause, and a UNC path on the remote machine in the SCOPE clause, as shown in the following example:</span></span>

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a><span data-ttu-id="3c9c3-164">Consultas basadas en AQS</span><span class="sxs-lookup"><span data-stu-id="3c9c3-164">AQS Based Queries</span></span>

<span data-ttu-id="3c9c3-165">AQS es la sintaxis de consulta predeterminada que usa Windows Search para consultar el índice y para refinar y restringir los parámetros de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-165">AQS is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="3c9c3-166">Aunque AQS está dirigido principalmente a los usuarios, los desarrolladores pueden usarlos para crear consultas mediante programación.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-166">While AQS is primarily user facing, it can be used by developers to build queries programmatically.</span></span> <span data-ttu-id="3c9c3-167">En Windows 7, se presentó una AQS canónica y se debe usar en Windows 7 y versiones posteriores, para generar consultas AQS mediante programación.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-167">In Windows 7 canonical AQS was introduced, and must be used in Windows 7 and later, to programmatically generate AQS queries.</span></span> <span data-ttu-id="3c9c3-168">Para obtener información detallada sobre AQS, consulte [usar la sintaxis de consulta avanzada mediante programación](-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="3c9c3-168">For detailed information on AQS, see [Using Advanced Query Syntax Programmatically](-search-3x-advancedquerysyntax.md).</span></span>

<span data-ttu-id="3c9c3-169">Los siguientes enfoques para consultar el índice se basan en AQS.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-169">The following approaches for querying the index are AQS based.</span></span>

### <a name="using-isearchqueryhelper"></a><span data-ttu-id="3c9c3-170">Usar ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="3c9c3-170">Using ISearchQueryHelper</span></span>

<span data-ttu-id="3c9c3-171">Puede desarrollar un componente o una clase auxiliar para consultar el índice mediante la interfaz [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , que le permite aprovechar algunas características del sistema y simplificar el uso de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-171">You can develop a component or helper class to query the index by using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, which enables you to take advantage of some features of the system and simplify your use of Windows Search.</span></span> <span data-ttu-id="3c9c3-172">Esta interfaz le ayuda a:</span><span class="sxs-lookup"><span data-stu-id="3c9c3-172">This interface helps you:</span></span>

- <span data-ttu-id="3c9c3-173">Obtenga una cadena de conexión OLE DB para conectarse a la base de datos de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-173">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
- <span data-ttu-id="3c9c3-174">Convierta las consultas de usuario de AQS a SQL de búsqueda de Windows.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-174">Convert user queries from AQS to Windows Search SQL.</span></span>

<span data-ttu-id="3c9c3-175">Esta interfaz se implementa como una clase auxiliar en [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) y se obtiene llamando a [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), como se muestra en el siguiente ejemplo de C++.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-175">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), as shown in the following C++ example.</span></span>

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

<span data-ttu-id="3c9c3-176">Para implementar la interfaz [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , consulte [uso de la interfaz ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md) y el tema de referencia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="3c9c3-176">To implement the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, see [Using the ISearchQueryHelper Interface](-search-3x-wds-qryidx-searchqueryhelper.md) and the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) reference topic.</span></span>

> [!Note]  
> <span data-ttu-id="3c9c3-177">Compatibilidad con la versión de Microsoft Windows Desktop Search (WDS) 2x heredada: en los equipos que ejecutan Windows XP y Windows Server 2003 y versiones posteriores, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) está en desuso.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-177">Legacy Microsoft Windows Desktop Search (WDS) 2x compatibility: On computers running Windows XP and Windows Server 2003 and later, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) is deprecated.</span></span> <span data-ttu-id="3c9c3-178">En su lugar, los desarrolladores deben usar [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para obtener una cadena de conexión, analizar la consulta del usuario en SQL y, a continuación, consultar OLE DB.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-178">Instead, developers should use [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) to get a connection string, parse the user's query into SQL, and then query through OLE DB.</span></span>

### <a name="using-the-search-ms-protocol"></a><span data-ttu-id="3c9c3-179">Uso del protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="3c9c3-179">Using the search-ms Protocol</span></span>

<span data-ttu-id="3c9c3-180">**Search-MS** [Application Protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) es una Convención para iniciar una aplicación, como el explorador de Windows, para consultar el índice de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-180">The **search-ms** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is a convention for starting an application, like Windows Explorer, to query the Windows Search index.</span></span> <span data-ttu-id="3c9c3-181">Permite que las consultas se compilen con argumentos de valor de parámetro, incluidos los argumentos de propiedad, las búsquedas guardadas anteriormente, la sintaxis de consulta avanzada (AQS), la sintaxis de consulta natural (NQS) y los identificadores de código de idioma (LCID) del indexador y la propia consulta.</span><span class="sxs-lookup"><span data-stu-id="3c9c3-181">It enables queries to be built with parameter-value arguments, including property arguments, previously saved searches, Advanced Query Syntax (AQS), Natural Query Syntax (NQS), and language code identifiers (LCIDs) for both the indexer and the query itself.</span></span>

<span data-ttu-id="3c9c3-182">Para obtener información detallada sobre la sintaxis del protocolo Search-MS, consulte [consultar el índice con el protocolo Search-MS](-search-3x-wds-qryidx-searchms.md).</span><span class="sxs-lookup"><span data-stu-id="3c9c3-182">For detailed information on the search-ms protocol syntax, see [Querying the Index with the search-ms Protocol](-search-3x-wds-qryidx-searchms.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c9c3-183">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c9c3-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c9c3-184">Consulta del índice mediante programación</span><span class="sxs-lookup"><span data-stu-id="3c9c3-184">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="3c9c3-185">Consultar el índice con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="3c9c3-185">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="3c9c3-186">Consultar el índice con el protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="3c9c3-186">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="3c9c3-187">Consultar el índice con la sintaxis SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="3c9c3-187">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="3c9c3-188">Usar la sintaxis de consulta avanzada mediante programación</span><span class="sxs-lookup"><span data-stu-id="3c9c3-188">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>
