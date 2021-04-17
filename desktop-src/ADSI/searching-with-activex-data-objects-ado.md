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
# <a name="searching-with-activex-data-objects-ado"></a><span data-ttu-id="ab4ed-105">Buscar con Objetos de datos ActiveX (ADO)</span><span class="sxs-lookup"><span data-stu-id="ab4ed-105">Searching with ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="ab4ed-106">El modelo de objetos de datos ActiveX (ADO) consta de los objetos que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-106">The ActiveX Data Object (ADO) model consists of objects listed in the following table.</span></span>



| <span data-ttu-id="ab4ed-107">Object</span><span class="sxs-lookup"><span data-stu-id="ab4ed-107">Object</span></span>         | <span data-ttu-id="ab4ed-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab4ed-108">Description</span></span>                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab4ed-109">**Connection**</span><span class="sxs-lookup"><span data-stu-id="ab4ed-109">**Connection**</span></span> | <span data-ttu-id="ab4ed-110">Conexión abierta a un origen de datos de OLE DB, como ADSI.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-110">An open connection to an OLE DB data source such as ADSI.</span></span>                                                                          |
| <span data-ttu-id="ab4ed-111">**Comando**</span><span class="sxs-lookup"><span data-stu-id="ab4ed-111">**Command**</span></span>    | <span data-ttu-id="ab4ed-112">Define un comando específico que se ejecutará en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-112">Defines a specific command to run against the data source.</span></span>                                                                         |
| <span data-ttu-id="ab4ed-113">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="ab4ed-113">**Parameter**</span></span>  | <span data-ttu-id="ab4ed-114">Colección opcional para los parámetros que se van a proporcionar al objeto de comando.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-114">An optional collection for any parameters to provide to the command object.</span></span>                                                        |
| <span data-ttu-id="ab4ed-115">**DataRecordsets**</span><span class="sxs-lookup"><span data-stu-id="ab4ed-115">**RecordSet**</span></span>  | <span data-ttu-id="ab4ed-116">Un conjunto de registros de una tabla, un objeto de comando o una sintaxis SQL.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-116">A set of records from a table, command object, or SQL syntax.</span></span> <span data-ttu-id="ab4ed-117">Se puede crear un conjunto de registros sin ningún objeto de conexión subyacente.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-117">A recordset can be created without any underlying connection object.</span></span> |
| <span data-ttu-id="ab4ed-118">**Campo**</span><span class="sxs-lookup"><span data-stu-id="ab4ed-118">**Field**</span></span>      | <span data-ttu-id="ab4ed-119">Una única columna de datos en un conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-119">A single column of data in a recordset.</span></span>                                                                                            |
| <span data-ttu-id="ab4ed-120">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="ab4ed-120">**Property**</span></span>   | <span data-ttu-id="ab4ed-121">Colección de valores proporcionados por el proveedor para ADO.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-121">A collection of values supplied by the provider for ADO.</span></span>                                                                           |
| <span data-ttu-id="ab4ed-122">**Error**</span><span class="sxs-lookup"><span data-stu-id="ab4ed-122">**Error**</span></span>      | <span data-ttu-id="ab4ed-123">Contiene datos sobre errores de acceso a datos.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-123">Contains data about data access errors.</span></span> <span data-ttu-id="ab4ed-124">Se actualiza cuando se produce un error en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-124">Refreshed when an error occurs in a single operation.</span></span>                                      |



 

<span data-ttu-id="ab4ed-125">Para que ADO se comunique con ADSI, debe haber, como mínimo, dos objetos ADO: **Connection** y **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-125">For ADO to communicate with ADSI, there must be, at least, two ADO objects: **Connection** and **RecordSet**.</span></span> <span data-ttu-id="ab4ed-126">Estos objetos ADO sirven para autenticar a los usuarios y enumerar los resultados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-126">These ADO objects serve to authenticate users and enumerate results, respectively.</span></span> <span data-ttu-id="ab4ed-127">Normalmente, también usará un objeto de **comando** para mantener una conexión activa, especificar parámetros de consulta, como el tamaño de página y el ámbito de búsqueda, y realizar una consulta.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-127">Typically, you will also use a **Command** object to maintain an active connection, specify query parameters, such as page size and search scope, and perform a query.</span></span> <span data-ttu-id="ab4ed-128">Para obtener más información sobre la sintaxis del filtro de búsqueda, consulte [Sintaxis de filtro de búsqueda](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="ab4ed-128">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="ab4ed-129">El objeto de **conexión** carga el proveedor de OLE DB y valida las credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-129">The **Connection** object loads the OLE DB provider, and validates user credentials.</span></span> <span data-ttu-id="ab4ed-130">En Visual Basic, llame a la función **CreateObject** con "ADODB. Conexión "para crear una instancia de un objeto de **conexión** y, a continuación, establezca la propiedad **Provider** del objeto de **conexión** en" ADsDSOObject ".</span><span class="sxs-lookup"><span data-stu-id="ab4ed-130">In Visual Basic, call the **CreateObject** function with "ADODB.Connection" to create an instance of a **Connection** object, and then set the **Provider** property of the **Connection** object to "ADsDSOObject".</span></span> <span data-ttu-id="ab4ed-131">ADODB. Connection "es el ProgID del objeto de **conexión** y" ADsDSOObject "es el nombre del proveedor de OLE DB en ADSI.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-131">"ADODB.Connection" is the ProgID of the **Connection** object and "ADsDSOObject" is the name of the OLE DB provider in ADSI.</span></span> <span data-ttu-id="ab4ed-132">Si no se especifica ninguna credencial, se usan las credenciales del usuario que ha iniciado sesión actualmente.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-132">If no credentials are specified, the credentials of the currently logged on user are used.</span></span>

<span data-ttu-id="ab4ed-133">En el ejemplo de código siguiente se muestra cómo crear una instancia de un objeto de **conexión** .</span><span class="sxs-lookup"><span data-stu-id="ab4ed-133">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="ab4ed-134">En el ejemplo de código siguiente se muestra cómo crear una instancia de un objeto de **conexión** .</span><span class="sxs-lookup"><span data-stu-id="ab4ed-134">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



<span data-ttu-id="ab4ed-135">En el ejemplo de código siguiente se muestra cómo crear una instancia de un objeto de **conexión** .</span><span class="sxs-lookup"><span data-stu-id="ab4ed-135">The following code example shows how to create an instance of a **Connection** object.</span></span> <span data-ttu-id="ab4ed-136">Tenga en cuenta que debe incluir la biblioteca de tipos de ADO (msadoXX.dll) como una de las referencias del proyecto Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-136">Be aware that you must include the ADO type library (msadoXX.dll) as one of the references in the Visual Basic project.</span></span>


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="ab4ed-137">Especifique los datos de autenticación del usuario estableciendo las propiedades del objeto de **conexión** .</span><span class="sxs-lookup"><span data-stu-id="ab4ed-137">Specify user authentication data by setting the properties of the **Connection** object.</span></span> <span data-ttu-id="ab4ed-138">En la tabla siguiente se enumeran las propiedades de autenticación de usuario compatibles con ADSI.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-138">The following table lists ADSI-supported user-authentication properties.</span></span>



| <span data-ttu-id="ab4ed-139">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab4ed-139">Property</span></span>           | <span data-ttu-id="ab4ed-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab4ed-140">Description</span></span>                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab4ed-141">"ID. de usuario"</span><span class="sxs-lookup"><span data-stu-id="ab4ed-141">"User ID"</span></span>          | <span data-ttu-id="ab4ed-142">Cadena que identifica al usuario cuyo contexto de seguridad se utiliza al realizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-142">A string that identifies the user whose security context is used when performing the search.</span></span> <span data-ttu-id="ab4ed-143">Para obtener más información sobre el formato de la cadena de nombre de usuario, vea [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject).</span><span class="sxs-lookup"><span data-stu-id="ab4ed-143">For more information about the format of the user name string, see [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject).</span></span> <span data-ttu-id="ab4ed-144">Si no se especifica, el valor predeterminado es el usuario que ha iniciado sesión o el usuario suplantado por el proceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-144">If not specified, the default is the logged on user, or the user impersonated by the calling process.</span></span> |
| <span data-ttu-id="ab4ed-145">"Password"</span><span class="sxs-lookup"><span data-stu-id="ab4ed-145">"Password"</span></span>         | <span data-ttu-id="ab4ed-146">Una cadena que especifica la contraseña del usuario identificado por "ID. de usuario".</span><span class="sxs-lookup"><span data-stu-id="ab4ed-146">A string that specifies the password of the user identified by "User ID".</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ab4ed-147">"Cifrar contraseña"</span><span class="sxs-lookup"><span data-stu-id="ab4ed-147">"Encrypt Password"</span></span> | <span data-ttu-id="ab4ed-148">Valor booleano que especifica si la contraseña está cifrada.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-148">A Boolean value that specifies whether the password is encrypted.</span></span> <span data-ttu-id="ab4ed-149">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-149">The default is **false**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ab4ed-150">"Marca ADSI"</span><span class="sxs-lookup"><span data-stu-id="ab4ed-150">"ADSI Flag"</span></span>        | <span data-ttu-id="ab4ed-151">Un conjunto de marcas de la enumeración de la enumeración de [**\_ \_ autenticación ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) que especifican las opciones de autenticación de enlace.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-151">A set of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration that specify the binding authentication options.</span></span> <span data-ttu-id="ab4ed-152">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-152">The default is zero.</span></span>                                                                                                                                                                         |



 

<span data-ttu-id="ab4ed-153">En el ejemplo de código siguiente se muestra cómo se establecen las propiedades antes de crear el objeto de **comando** .</span><span class="sxs-lookup"><span data-stu-id="ab4ed-153">The following code example shows how the properties are set before creating the **Command** object.</span></span>


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



<span data-ttu-id="ab4ed-154">El segundo objeto de ADO es el objeto de **comando** .</span><span class="sxs-lookup"><span data-stu-id="ab4ed-154">The second ADO object is the **Command** object.</span></span> <span data-ttu-id="ab4ed-155">El ProgID del objeto **Command** es "ADODB. Command".</span><span class="sxs-lookup"><span data-stu-id="ab4ed-155">The ProgID of the **Command** object is "ADODB.Command".</span></span> <span data-ttu-id="ab4ed-156">Este objeto permite emitir instrucciones de consulta y otros comandos para ADSI mediante la conexión activa.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-156">This object enables you to issue query statements and other commands to ADSI using the active connection.</span></span> <span data-ttu-id="ab4ed-157">El objeto **Command** utiliza su propiedad **ActiveConnection** para mantener una conexión activa.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-157">The **Command** object uses its **ActiveConnection** property to maintain an active connection.</span></span> <span data-ttu-id="ab4ed-158">También mantiene la propiedad **CommandText** para contener instrucciones de consulta emitidas por un usuario.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-158">It also maintains the **CommandText** property to hold query statements issued by a user.</span></span> <span data-ttu-id="ab4ed-159">Las instrucciones de consulta se expresan en el dialecto [SQL](sql-dialect.md) o en el [dialecto LDAP](ldap-dialect.md).</span><span class="sxs-lookup"><span data-stu-id="ab4ed-159">The query statements are expressed in either the [SQL dialect](sql-dialect.md) or the [LDAP dialect](ldap-dialect.md).</span></span>

<span data-ttu-id="ab4ed-160">En los siguientes ejemplos de código se muestra cómo crear un objeto de **comando** .</span><span class="sxs-lookup"><span data-stu-id="ab4ed-160">The following code examples show how to create a **Command** object.</span></span>


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



<span data-ttu-id="ab4ed-161">En el ejemplo de código siguiente, se incluye la biblioteca de tipos ADO (msadoXX.dll) como una de las referencias.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-161">In the following code example, include ADO type library (msadoXX.dll) as one of the references.</span></span>


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



<span data-ttu-id="ab4ed-162">Las opciones de búsqueda para el objeto de **comando** se especifican estableciendo la propiedad **Properties** .</span><span class="sxs-lookup"><span data-stu-id="ab4ed-162">Search options for the **Command** object are specified by setting the **Properties** property.</span></span> <span data-ttu-id="ab4ed-163">En la tabla siguiente se enumeran las propiedades válidas con nombre para **las propiedades**.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-163">The following table lists acceptable named properties for **Properties**.</span></span>



| <span data-ttu-id="ab4ed-164">Propiedad con nombre</span><span class="sxs-lookup"><span data-stu-id="ab4ed-164">Named property</span></span>      | <span data-ttu-id="ab4ed-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab4ed-165">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab4ed-166">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="ab4ed-166">"Asynchronous"</span></span>      | <span data-ttu-id="ab4ed-167">Valor booleano que especifica si la búsqueda es sincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-167">A Boolean value that specifies whether the search is synchronous or asynchronous.</span></span> <span data-ttu-id="ab4ed-168">El valor predeterminado es false (sincrónico).</span><span class="sxs-lookup"><span data-stu-id="ab4ed-168">The default is False (synchronous).</span></span> <span data-ttu-id="ab4ed-169">Una búsqueda sincrónica se bloquea hasta que el servidor devuelve el resultado completo, o para una búsqueda paginada, toda la página.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-169">A synchronous search blocks until the server returns the entire result, or for a paged search, the entire page.</span></span> <span data-ttu-id="ab4ed-170">Una búsqueda asincrónica se bloquea hasta que una fila de los resultados de la búsqueda está disponible, o hasta que transcurre el tiempo especificado por la propiedad "timeout".</span><span class="sxs-lookup"><span data-stu-id="ab4ed-170">An asynchronous search blocks until one row of the search results is available, or until the time specified by the "Timeout" property elapses.</span></span>                           |
| <span data-ttu-id="ab4ed-171">"Resultados de caché"</span><span class="sxs-lookup"><span data-stu-id="ab4ed-171">"Cache results"</span></span>     | <span data-ttu-id="ab4ed-172">Valor booleano que especifica si el resultado se debe almacenar en caché en el lado del cliente.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-172">A Boolean value that specifies whether the result should be cached on the client side.</span></span> <span data-ttu-id="ab4ed-173">El valor predeterminado es **true**; ADSI almacena en caché el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-173">The default is **true**; ADSI caches the result set.</span></span> <span data-ttu-id="ab4ed-174">Desactivar esta opción puede ser deseable para grandes conjuntos de resultados.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-174">Turning off this option may be desirable for large result sets.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="ab4ed-175">"Referencias de seguimiento"</span><span class="sxs-lookup"><span data-stu-id="ab4ed-175">"Chase referrals"</span></span>   | <span data-ttu-id="ab4ed-176">Un valor de la [**\_ \_ \_ enumeración de referencias de seguimiento de ADS**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) que especifica cómo la búsqueda realiza las referencias.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-176">A value from the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) that specifies how the search chases referrals.</span></span> <span data-ttu-id="ab4ed-177">El valor predeterminado es **ADS \_ seguimiento de \_ referencias \_ nunca**. Para obtener más información sobre esta propiedad, vea [Referrals](/windows/desktop/AD/referrals).</span><span class="sxs-lookup"><span data-stu-id="ab4ed-177">The default is **ADS\_CHASE\_REFERRALS\_NEVER**.For more information about this property, see [Referrals](/windows/desktop/AD/referrals).</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="ab4ed-178">"Solo nombres de columna"</span><span class="sxs-lookup"><span data-stu-id="ab4ed-178">"Column Names Only"</span></span> | <span data-ttu-id="ab4ed-179">Un valor booleano que indica que la búsqueda debe recuperar solo el nombre de los atributos a los que se han asignado valores.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-179">A Boolean value that indicates that the search should retrieve only the name of attributes to which values have been assigned.</span></span> <span data-ttu-id="ab4ed-180">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-180">The default is **false**.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ab4ed-181">"Subaliases de deref"</span><span class="sxs-lookup"><span data-stu-id="ab4ed-181">"Deref Aliases"</span></span>     | <span data-ttu-id="ab4ed-182">Valor booleano que especifica si se resuelven los alias de objetos encontrados.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-182">A Boolean value that specifies whether aliases of found objects are resolved.</span></span> <span data-ttu-id="ab4ed-183">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-183">The default is **false**.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="ab4ed-184">"Tamaño de página"</span><span class="sxs-lookup"><span data-stu-id="ab4ed-184">"Page size"</span></span>         | <span data-ttu-id="ab4ed-185">Valor entero que activa la paginación y especifica el número máximo de objetos que se van a devolver en un conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-185">An integer value that turns on paging and specifies the maximum number of objects to return in a results set.</span></span> <span data-ttu-id="ab4ed-186">El valor predeterminado es sin tamaño de página.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-186">The default is no page size.</span></span> <span data-ttu-id="ab4ed-187">Para obtener más información, vea [recuperar grandes conjuntos de resultados](retrieving-large-results-sets.md).</span><span class="sxs-lookup"><span data-stu-id="ab4ed-187">For more information, see [Retrieving Large Results Sets](retrieving-large-results-sets.md).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="ab4ed-188">SearchScope</span><span class="sxs-lookup"><span data-stu-id="ab4ed-188">"SearchScope"</span></span>       | <span data-ttu-id="ab4ed-189">Un valor de la enumeración [**ADS \_ SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) que especifica el ámbito de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-189">A value from the [**ADS\_SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) enumeration that specifies the search scope.</span></span> <span data-ttu-id="ab4ed-190">El valor predeterminado **es \_ \_ subárbol del ámbito de ADS**.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-190">The default is **ADS\_SCOPE\_SUBTREE**.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ab4ed-191">"Límite de tamaño"</span><span class="sxs-lookup"><span data-stu-id="ab4ed-191">"Size Limit"</span></span>        | <span data-ttu-id="ab4ed-192">Valor entero que especifica el límite de tamaño de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-192">An integer value that specifies the size limit for the search.</span></span> <span data-ttu-id="ab4ed-193">Por Active Directory, el límite de tamaño especifica el número máximo de objetos devueltos.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-193">For Active Directory, the size limit specifies the maximum number of returned objects.</span></span> <span data-ttu-id="ab4ed-194">El servidor detiene la búsqueda cuando se alcanza el límite de tamaño y devuelve los resultados acumulados.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-194">The server stops searching when the size limit is reached and returns the results accumulated.</span></span> <span data-ttu-id="ab4ed-195">El valor predeterminado es sin límite.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-195">The default is no limit.</span></span>                                                                                                                                  |
| <span data-ttu-id="ab4ed-196">"Ordenar por"</span><span class="sxs-lookup"><span data-stu-id="ab4ed-196">"Sort on"</span></span>           | <span data-ttu-id="ab4ed-197">Cadena que especifica una lista separada por comas de atributos que se van a utilizar como claves de ordenación.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-197">A string that specifies a comma-separated list of attributes to use as sort keys.</span></span> <span data-ttu-id="ab4ed-198">Esta propiedad solo funciona para los servidores de directorio que admiten el control LDAP para la ordenación del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-198">This property works only for directory servers that support the LDAP control for server-side sorting.</span></span> <span data-ttu-id="ab4ed-199">Active Directory admite el control de ordenación, pero puede afectar al rendimiento del servidor, especialmente si el conjunto de resultados es grande.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-199">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="ab4ed-200">Tenga en cuenta que Active Directory solo admite una única clave de ordenación.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-200">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="ab4ed-201">El valor predeterminado es ninguna ordenación.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-201">The default is no sorting.</span></span> |
| <span data-ttu-id="ab4ed-202">"Límite de tiempo"</span><span class="sxs-lookup"><span data-stu-id="ab4ed-202">"Time Limit"</span></span>        | <span data-ttu-id="ab4ed-203">Valor entero que especifica el límite de tiempo, en segundos, de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-203">An integer value that specifies the time limit, in seconds, for the search.</span></span> <span data-ttu-id="ab4ed-204">Cuando se alcanza el límite de tiempo, el servidor detiene la búsqueda y devuelve los resultados acumulados.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-204">When the time limit is reached, the server stops searching and returns the results accumulated.</span></span> <span data-ttu-id="ab4ed-205">El valor predeterminado es sin límite de tiempo.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-205">The default is no time limit.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="ab4ed-206">Super</span><span class="sxs-lookup"><span data-stu-id="ab4ed-206">"Timeout"</span></span>           | <span data-ttu-id="ab4ed-207">Valor entero que especifica el valor de tiempo de espera del lado cliente, en segundos.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-207">An integer value that specifies the client-side timeout value, in seconds.</span></span> <span data-ttu-id="ab4ed-208">Este valor indica el tiempo que el cliente espera los resultados del servidor antes de detener la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-208">This value indicates the time the client waits for results from the server before stopping the search.</span></span> <span data-ttu-id="ab4ed-209">El valor predeterminado es sin tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-209">The default is no time-out.</span></span>                                                                                                                                                                                                  |



 

<span data-ttu-id="ab4ed-210">En el ejemplo de código siguiente se muestra cómo establecer las opciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-210">The following code example shows how to set search options.</span></span>


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



<span data-ttu-id="ab4ed-211">El tercer objeto ADO es **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-211">The third ADO object is **RecordSet**.</span></span> <span data-ttu-id="ab4ed-212">Este objeto se obtiene al invocar el método **Execute** en un objeto **Command** .</span><span class="sxs-lookup"><span data-stu-id="ab4ed-212">You obtain this object when you invoke the **Execute** method on a **Command** object.</span></span> <span data-ttu-id="ab4ed-213">La función principal del objeto de **conjunto de registros** es enumerar el conjunto de resultados y obtener los datos.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-213">The primary function of the **RecordSet** object is to enumerate the result set and obtain the data.</span></span> <span data-ttu-id="ab4ed-214">El conjunto de resultados puede contener valores para los atributos que tienen valores únicos o múltiples.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-214">The result set can contain values for attributes that have both single or multiple values.</span></span> <span data-ttu-id="ab4ed-215">Obtener un atributo de un solo valor es sencillo, similar a obtener el valor de la columna en la base de datos relacional, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ab4ed-215">Getting a single-valued attribute is simple, similar to getting the column value in the relational database, for example:</span></span>


```VB
Fields('name').Value
```



<span data-ttu-id="ab4ed-216">La obtención de un atributo con varios valores, sin embargo, es más desafiante.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-216">Getting an attribute with multiple values, however, is more challenging.</span></span> <span data-ttu-id="ab4ed-217">En este caso, el **campo. Value** es una matriz y debe comprobar el límite inferior y superior de la matriz, como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-217">In this case, the **Field.Value** is an array and you must check the lower and upper bound of the array, as shown in the following code example.</span></span>


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



<span data-ttu-id="ab4ed-218">En el ejemplo de código siguiente se deshabilitan las cuentas de usuario en un servidor LDAP.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-218">The following code example disables the user accounts on an LDAP server.</span></span>


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



<span data-ttu-id="ab4ed-219">Para obtener más información sobre el modelo de objetos ADO, vea [Microsoft objetos de datos ActiveX](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).</span><span class="sxs-lookup"><span data-stu-id="ab4ed-219">For more information about the ADO object model, see [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).</span></span>

 

