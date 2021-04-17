---
title: Consulta distribuida
description: Como ADSI es un proveedor de OLE DB, puede participar en la consulta distribuida introducida en Microsoft SQL Server 7,0.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- consultas ADSI, consulta distribuida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8675f0a5ba9faa6ece78783eb4f61f17aafabc8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "105656309"
---
# <a name="distributed-query"></a><span data-ttu-id="e0c67-104">Consulta distribuida</span><span class="sxs-lookup"><span data-stu-id="e0c67-104">Distributed Query</span></span>

<span data-ttu-id="e0c67-105">Como ADSI es un proveedor de OLE DB, puede participar en la consulta distribuida introducida en Microsoft SQL Server 7,0.</span><span class="sxs-lookup"><span data-stu-id="e0c67-105">Because ADSI is an OLE DB Provider, it can participate in Distributed Query introduced in Microsoft SQL Server 7.0.</span></span> <span data-ttu-id="e0c67-106">Los escenarios posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e0c67-106">The following are possible scenarios:</span></span>

-   <span data-ttu-id="e0c67-107">Combinar objetos de Active Directory con datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e0c67-107">Joining Active Directory objects with SQL Server data.</span></span>
-   <span data-ttu-id="e0c67-108">Actualizar datos SQL desde objetos Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e0c67-108">Updating SQL data from Active Directory objects.</span></span>
-   <span data-ttu-id="e0c67-109">Crear combinaciones tridireccionales o bidireccionales con otros proveedores de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e0c67-109">Creating three-way or four-way joins with other OLE DB Providers.</span></span> <span data-ttu-id="e0c67-110">Por ejemplo, Index Server, SQL Server y Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e0c67-110">For example, Index Server, SQL Server, and Active Directory.</span></span>

<span data-ttu-id="e0c67-111">El proveedor de OLE DB admite dos dialectos de comandos, LDAP y SQL, para tener acceso al servicio de directorio y devolver los resultados en un formato tabular que se puede consultar con SQL Server consultas distribuidas.</span><span class="sxs-lookup"><span data-stu-id="e0c67-111">The OLE DB Provider supports two command dialects, LDAP and SQL, to access the directory service and return results in a tabular form that can be queried with SQL Server distributed queries.</span></span>

<span data-ttu-id="e0c67-112">**Para iniciar el analizador de consultas de SQL**</span><span class="sxs-lookup"><span data-stu-id="e0c67-112">**To start the SQL Query Analyzer**</span></span>

1.  <span data-ttu-id="e0c67-113">En primer lugar, abra el [analizador de consultas de SQL](https://msdn.microsoft.com/library/Aa216983.aspx) en el SQL Server que está vinculado al servicio de directorio (consulte Creación de un servidor vinculado).</span><span class="sxs-lookup"><span data-stu-id="e0c67-113">First, open the [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) on the SQL Server that is linked to the directory service (see Creating a Linked Server).</span></span>
2.  <span data-ttu-id="e0c67-114">Ejecutar el **analizador de consultas de SQL** (iniciar \| programas \| Microsoft SQL Server 7,0)</span><span class="sxs-lookup"><span data-stu-id="e0c67-114">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
3.  <span data-ttu-id="e0c67-115">Inicie sesión en el equipo SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e0c67-115">Log on to the SQL Server computer.</span></span>
4.  <span data-ttu-id="e0c67-116">Escriba la consulta SQL en el panel del editor de la ventana de consulta.</span><span class="sxs-lookup"><span data-stu-id="e0c67-116">Enter the SQL Query into the Editor pane of the query window.</span></span>
5.  <span data-ttu-id="e0c67-117">Ejecute la consulta presionando F5.</span><span class="sxs-lookup"><span data-stu-id="e0c67-117">Execute the query by pressing F5.</span></span>

<span data-ttu-id="e0c67-118">En las secciones siguientes se proporcionan más detalles:</span><span class="sxs-lookup"><span data-stu-id="e0c67-118">The following sections provide more detail:</span></span>

-   [<span data-ttu-id="e0c67-119">Creación de un servidor vinculado</span><span class="sxs-lookup"><span data-stu-id="e0c67-119">Creating a Linked Server</span></span>](#creating-a-linked-server)
-   [<span data-ttu-id="e0c67-120">Creación de un inicio de sesión autenticado de SQL Server</span><span class="sxs-lookup"><span data-stu-id="e0c67-120">Creating a SQL Server Authenticated Login</span></span>](#creating-a-sql-server-authenticated-login)
-   [<span data-ttu-id="e0c67-121">Consultar el servicio de directorio</span><span class="sxs-lookup"><span data-stu-id="e0c67-121">Querying the Directory Service</span></span>](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a><span data-ttu-id="e0c67-122">Creación de un servidor vinculado</span><span class="sxs-lookup"><span data-stu-id="e0c67-122">Creating a Linked Server</span></span>

<span data-ttu-id="e0c67-123">Para configurar una combinación distribuida en un servicio de directorio de Windows 2000 Server, cree un servidor vinculado.</span><span class="sxs-lookup"><span data-stu-id="e0c67-123">To set up a distributed join on a Windows 2000 Server directory service, create a linked server.</span></span> <span data-ttu-id="e0c67-124">Para ello, configure la asignación ADSI mediante el procedimiento almacenado del sistema [ \_ addlinkedserver de SP](https://msdn.microsoft.com/library/Aa259589.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e0c67-124">To do this, set up ADSI mapping by using the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure.</span></span> <span data-ttu-id="e0c67-125">Este procedimiento vincula un nombre a un nombre de proveedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e0c67-125">This procedure links a name to an OLE DB Provider name.</span></span>

<span data-ttu-id="e0c67-126">En el ejemplo siguiente, tenga en cuenta que hay varios argumentos que se usan con el procedimiento almacenado del sistema [Sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) :</span><span class="sxs-lookup"><span data-stu-id="e0c67-126">In the following example, note that there are several arguments used with the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="e0c67-127">"ADSI" es el argumento **Server** y será el nombre de este servidor vinculado.</span><span class="sxs-lookup"><span data-stu-id="e0c67-127">"ADSI" is the **server** argument and will be the name of this linked server.</span></span>
-   <span data-ttu-id="e0c67-128">"Active Directory Services 2,5" es el argumento **srvproduct** , que es el nombre del origen de datos OLE DB que se va a agregar como servidor vinculado.</span><span class="sxs-lookup"><span data-stu-id="e0c67-128">"Active Directory Services 2.5" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
-   <span data-ttu-id="e0c67-129">"ADSDSOObject" es el argumento de **\_ nombre del proveedor** .</span><span class="sxs-lookup"><span data-stu-id="e0c67-129">"ADSDSOObject" is the **provider\_name** argument.</span></span>
-   <span data-ttu-id="e0c67-130">"adsdatasource" es el argumento de **\_ origen de datos** , que es el nombre del origen de datos tal como lo interpreta el proveedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e0c67-130">"adsdatasource" is the **data\_source** argument, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

<span data-ttu-id="e0c67-131">El comando [exec](https://msdn.microsoft.com/library/Aa258848.aspx) se usa para ejecutar procedimientos almacenados del sistema.</span><span class="sxs-lookup"><span data-stu-id="e0c67-131">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



<span data-ttu-id="e0c67-132">En el caso de los inicios de sesión autenticados por Windows, la asignación automática es suficiente para tener acceso al directorio con SQL Server la delegación de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e0c67-132">For Windows-authenticated logins, the self-mapping is sufficient to access the directory with SQL Server Security Delegation.</span></span> <span data-ttu-id="e0c67-133">Dado que la asignación automática se crea de forma predeterminada para los servidores vinculados creados a través de [Sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), no es necesario ninguna otra asignación de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e0c67-133">Because the self-mapping is created by default for linked servers created through [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), no other login mapping is necessary.</span></span>

<span data-ttu-id="e0c67-134">En el caso de los inicios de sesión autenticados de SQL Server, puede configurar inicios de sesión y contraseñas adecuados para conectarse al servicio de directorio mediante el procedimiento almacenado del sistema [ \_ addlinkedsrvlogin de SP](https://msdn.microsoft.com/library/Aa259581.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e0c67-134">For SQL Server–authenticated logins, you can configure suitable logins and passwords for connecting to the directory service by using the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

> [!Note]  
> <span data-ttu-id="e0c67-135">Siempre que sea posible, utilice la autenticación de Windows.</span><span class="sxs-lookup"><span data-stu-id="e0c67-135">When possible, use Windows Authentication.</span></span>

 

## <a name="creating-a-sql-server-authenticated-login"></a><span data-ttu-id="e0c67-136">Creación de un inicio de sesión autenticado de SQL Server</span><span class="sxs-lookup"><span data-stu-id="e0c67-136">Creating a SQL Server Authenticated Login</span></span>

<span data-ttu-id="e0c67-137">Si prefiere usar un inicio de sesión autenticado SQL Server en lugar de la autenticación de Windows, agregue un inicio de sesión al servidor vinculado (vea la sección anterior).</span><span class="sxs-lookup"><span data-stu-id="e0c67-137">If you prefer to use a SQL Server–authenticated login rather than Windows Authentication, add a login to the linked server (see the previous section).</span></span> <span data-ttu-id="e0c67-138">Para ello, use el procedimiento almacenado del sistema [Sp \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e0c67-138">To do this, use the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

<span data-ttu-id="e0c67-139">En el ejemplo siguiente, hay varios argumentos que se usan con el procedimiento almacenado del sistema [Sp \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) :</span><span class="sxs-lookup"><span data-stu-id="e0c67-139">In the following example, there are several arguments that are used with the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="e0c67-140">"ADSI" es el argumento **rmtsvrname** , que es el nombre del servidor vinculado creado en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="e0c67-140">"ADSI" is the **rmtsvrname** argument, which is the name of the linked server created in the previous example.</span></span>
-   <span data-ttu-id="e0c67-141">" \\ Administrador de Fabrikam" es el argumento **locallogin** , que es el inicio de sesión en el servidor local y puede ser el inicio de sesión de SQL Server o un usuario de Windows NT.</span><span class="sxs-lookup"><span data-stu-id="e0c67-141">"Fabrikam\\Administrator" is the **locallogin** argument, which is the login on the local server and can be the SQL Server login or a Windows NT user.</span></span>
-   <span data-ttu-id="e0c67-142">"CN = Administrator, OU = sales, DC = activeds, DC = Fabrikam, DC = com" es el argumento **rmtuser** , que es el nombre de usuario que se usa para conectarse porque **useself** es **false**.</span><span class="sxs-lookup"><span data-stu-id="e0c67-142">"CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com" is the **rmtuser** argument, which is the user name that you use to connect because **useself** is **false**.</span></span>
-   <span data-ttu-id="e0c67-143">"Secret \* \* 2000" es el **rmtpassword**, que es la contraseña asociada a **rmtuser**</span><span class="sxs-lookup"><span data-stu-id="e0c67-143">"secret\*\*2000" is the **rmtpassword**, which is the password associated to **rmtuser**</span></span>

<span data-ttu-id="e0c67-144">El comando [exec](https://msdn.microsoft.com/library/Aa258848.aspx) se usa para ejecutar procedimientos almacenados del sistema.</span><span class="sxs-lookup"><span data-stu-id="e0c67-144">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a><span data-ttu-id="e0c67-145">Consultar el servicio de directorio</span><span class="sxs-lookup"><span data-stu-id="e0c67-145">Querying the Directory Service</span></span>

<span data-ttu-id="e0c67-146">Después de crear un servidor vinculado, utilice una instrucción [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) para enviar una consulta al servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="e0c67-146">After you have created a linked server, use an [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement to send a query to the Directory Service.</span></span> <span data-ttu-id="e0c67-147">La siguiente consulta SQL crea una tabla virtual para almacenar los resultados de la consulta mediante la instrucción [Create View](https://msdn.microsoft.com/library/Aa258253.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e0c67-147">The following SQL query creates a virtual table to hold your query results by using the [CREATE VIEW](https://msdn.microsoft.com/library/Aa258253.aspx) statement.</span></span> <span data-ttu-id="e0c67-148">La vista que se crea se denomina "viewADContacts".</span><span class="sxs-lookup"><span data-stu-id="e0c67-148">The view that is created is named "viewADContacts".</span></span>

<span data-ttu-id="e0c67-149">La primera instrucción [Select](https://msdn.microsoft.com/library/Aa259187.aspx) define la información que se consulta desde el servicio de directorio y la asigna a una columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e0c67-149">The first [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement defines the information that is being queried from the directory service and maps it to a column in the table.</span></span> <span data-ttu-id="e0c67-150">La información entre corchetes indica los datos que se colocan en la tabla virtual.</span><span class="sxs-lookup"><span data-stu-id="e0c67-150">Information surrounded by brackets indicates the data that is put into the virtual table.</span></span> <span data-ttu-id="e0c67-151">La información que no está entre corchetes indica los datos que se recuperan del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="e0c67-151">The information that is not in brackets indicates the data that is retrieved from the directory service.</span></span> <span data-ttu-id="e0c67-152">Tenga en cuenta que se debe hacer referencia a la información que se recupera del servicio de directorio mediante su nombre para mostrar LDAP.</span><span class="sxs-lookup"><span data-stu-id="e0c67-152">Notice that the information that is being retrieved from the directory service must be referenced by its LDAP display name.</span></span>

<span data-ttu-id="e0c67-153">La siguiente instrucción es la instrucción [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e0c67-153">The next statement is the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="e0c67-154">Esta instrucción tiene dos argumentos: ADSI, que es el nombre del servidor vinculado que ha creado y una instrucción de consulta.</span><span class="sxs-lookup"><span data-stu-id="e0c67-154">This statement has two arguments: ADSI, which is the name of the linked server that you created, and a query statement.</span></span> <span data-ttu-id="e0c67-155">La instrucción de consulta contiene los elementos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e0c67-155">The query statement contains the following items:</span></span>

-   <span data-ttu-id="e0c67-156">La instrucción [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contiene la lista de datos que se obtendrán del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="e0c67-156">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="e0c67-157">Tendrá que usar el nombre para mostrar LDAP para indicar qué datos está buscando.</span><span class="sxs-lookup"><span data-stu-id="e0c67-157">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
-   <span data-ttu-id="e0c67-158">La instrucción [from](https://msdn.microsoft.com/library/Aa258869.aspx) contiene el nombre del servidor de directorio vinculado del que se obtendrá esta información.</span><span class="sxs-lookup"><span data-stu-id="e0c67-158">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
-   <span data-ttu-id="e0c67-159">La instrucción [Where](https://msdn.microsoft.com/library/Aa260674.aspx) proporciona las condiciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e0c67-159">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="e0c67-160">En este ejemplo, busca contactos.</span><span class="sxs-lookup"><span data-stu-id="e0c67-160">In this example, it is searching for contacts.</span></span>

<span data-ttu-id="e0c67-161">La instrucción [Select](https://msdn.microsoft.com/library/Aa259187.aspx) final se usa para recopilar los resultados de la vista que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="e0c67-161">The final [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement is used to pick up results from the view to display.</span></span>


```sql
CREATE VIEW viewADContacts
AS
SELECT  [Name], sn [Last Name], street [Street], l [City], st [State]
FROM OPENQUERY( ADSI, 
     'SELECT name, sn, street, l, st
      FROM 'LDAP:// OU=Sales,DC=activeds,DC=Fabrikam,DC=Com'
      WHERE objectCategory='Person' AND 
      objectClass = 'contact'')
GO
SELECT * FROM viewADContacts
```



 

 




