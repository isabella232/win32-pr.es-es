---
description: Un almacén de directivas de autorización contiene información sobre la Directiva de seguridad de una aplicación o grupo de aplicaciones.
ms.assetid: bce85da8-11de-4bc1-b097-d8efdbd28abf
title: Crear un objeto de almacén de directivas de autorización en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: feb02c80408210b663524e2aa914852a853e80ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908290"
---
# <a name="creating-an-authorization-policy-store-object-in-script"></a><span data-ttu-id="08664-103">Crear un objeto de almacén de directivas de autorización en el script</span><span class="sxs-lookup"><span data-stu-id="08664-103">Creating an Authorization Policy Store Object in Script</span></span>

<span data-ttu-id="08664-104">Un almacén de directivas de autorización contiene información sobre la Directiva de seguridad de una aplicación o grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="08664-104">An authorization policy store contains information about the security policy of an application or group of applications.</span></span> <span data-ttu-id="08664-105">La información incluye las aplicaciones, operaciones, tareas, usuarios y grupos de usuarios asociados a la tienda.</span><span class="sxs-lookup"><span data-stu-id="08664-105">The information includes the applications, operations, tasks, users, and groups of users associated with the store.</span></span> <span data-ttu-id="08664-106">Cuando una aplicación que usa administrador de autorización se inicializa, carga esta información desde el almacén.</span><span class="sxs-lookup"><span data-stu-id="08664-106">When an application that uses Authorization Manager initializes, it loads this information from the store.</span></span> <span data-ttu-id="08664-107">El almacén de directivas de autorización debe estar ubicado en un sistema de confianza porque los administradores de ese sistema tienen un alto grado de acceso al almacén.</span><span class="sxs-lookup"><span data-stu-id="08664-107">The authorization policy store must be located on a trusted system because administrators on that system have a high degree of access to the store.</span></span>

<span data-ttu-id="08664-108">Administrador de autorización admite el almacenamiento de la Directiva de autorización en el servicio de directorio de Active Directory o en un archivo XML, tal como se muestra en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="08664-108">Authorization Manager supports storing authorization policy either in the Active Directory directory service or in an XML file as shown in the following examples.</span></span> <span data-ttu-id="08664-109">En la API de administrador de autorización, un almacén de directivas de autorización se representa mediante un objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="08664-109">In the Authorization Manager API, an authorization policy store is represented by an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="08664-110">En los ejemplos se muestra cómo crear un objeto **AzAuthorizationStore** para un almacén de Active Directory y un almacén XML.</span><span class="sxs-lookup"><span data-stu-id="08664-110">The examples show how to create an **AzAuthorizationStore** object for an Active Directory store and an XML store.</span></span>

-   [<span data-ttu-id="08664-111">Creación de un almacén de Active Directory</span><span class="sxs-lookup"><span data-stu-id="08664-111">Creating an Active Directory Store</span></span>](#creating-an-active-directory-store)
-   [<span data-ttu-id="08664-112">Creación de un almacén de SQL Server</span><span class="sxs-lookup"><span data-stu-id="08664-112">Creating a SQL Server Store</span></span>](#creating-a-sql-server-store)
-   [<span data-ttu-id="08664-113">Crear un almacén XML</span><span class="sxs-lookup"><span data-stu-id="08664-113">Creating an XML Store</span></span>](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a><span data-ttu-id="08664-114">Creación de un almacén de Active Directory</span><span class="sxs-lookup"><span data-stu-id="08664-114">Creating an Active Directory Store</span></span>

<span data-ttu-id="08664-115">Para usar Active Directory para almacenar la Directiva de autorización, el dominio debe estar en el nivel funcional del dominio de **Windows Server 2003** .</span><span class="sxs-lookup"><span data-stu-id="08664-115">To use Active Directory to store the authorization policy, the domain must be in the **Windows Server 2003** domain functional level.</span></span> <span data-ttu-id="08664-116">No se encuentra el almacén de directivas de autorización en un **contexto de nomenclatura que no es de dominio** (también denominado partición de aplicación).</span><span class="sxs-lookup"><span data-stu-id="08664-116">The authorization policy store cannot be located in a **Non-Domain Naming Context** (also called an application partition).</span></span> <span data-ttu-id="08664-117">Se recomienda ubicar el almacén en el contenedor de **datos de programa** en una nueva unidad organizativa creada específicamente para el almacén de directivas de autorización.</span><span class="sxs-lookup"><span data-stu-id="08664-117">It is recommended that the store be located in the **Program Data** container under a new organizational unit created specifically for the authorization policy store.</span></span> <span data-ttu-id="08664-118">También se recomienda que el almacén se encuentre en la misma red de área local que los servidores de aplicaciones que ejecutan las aplicaciones que usan el almacén.</span><span class="sxs-lookup"><span data-stu-id="08664-118">It is also recommended that the store be located within the same local area network as application servers that run applications that use the store.</span></span>

<span data-ttu-id="08664-119">En el ejemplo siguiente se muestra cómo crear un objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="08664-119">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in Active Directory.</span></span> <span data-ttu-id="08664-120">En el ejemplo se supone que hay una unidad organizativa Active Directory denominada datos de programa en un dominio denominado authmanager.com.</span><span class="sxs-lookup"><span data-stu-id="08664-120">The example assumes that there is an existing Active Directory organizational unit named Program Data in a domain named authmanager.com.</span></span>


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _
    "msldap://CN=MyStore, CN=Program Data,DC=authmanager,DC=com"

'  Save the information to the store.
authStore.Submit
```



## <a name="creating-a-sql-server-store"></a><span data-ttu-id="08664-121">Creación de un almacén de SQL Server</span><span class="sxs-lookup"><span data-stu-id="08664-121">Creating a SQL Server Store</span></span>

<span data-ttu-id="08664-122">Administrador de autorización admite la creación de un almacén de directivas de autorización basado en Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="08664-122">Authorization Manager supports creating a Microsoft SQL Server–based authorization policy store.</span></span> <span data-ttu-id="08664-123">Para crear un almacén de autorización basado en SQL Server, use una dirección URL que comience con el prefijo **MSSQL://**.</span><span class="sxs-lookup"><span data-stu-id="08664-123">To create a SQL Server–based authorization store, use a URL that begins with the prefix **MSSQL://**.</span></span> <span data-ttu-id="08664-124">La dirección URL debe contener una cadena de conexión SQL válida, un nombre de base de datos y el nombre del almacén de directivas de autorización: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.</span><span class="sxs-lookup"><span data-stu-id="08664-124">The URL must contain a valid SQL connection string, a database name, and the name of the authorization policy store: **MSSQL://**_ConnectionString_*_/_*_DatabaseName_*_/_*_PolicyStoreName_.</span></span>

<span data-ttu-id="08664-125">Si la instancia de SQL Server no contiene la base de datos de administrador de autorización especificada, el administrador de autorización crea una nueva base de datos con ese nombre.</span><span class="sxs-lookup"><span data-stu-id="08664-125">If the instance of SQL Server does not contain the specified Authorization Manager database, Authorization Manager creates a new database with that name.</span></span>

> [!Note]  
> <span data-ttu-id="08664-126">Las conexiones a un almacén de SQL Server no se cifran a menos que se configure explícitamente el cifrado SQL para la conexión o se configure el cifrado del tráfico de red que usa el protocolo de seguridad de Internet (IPsec).</span><span class="sxs-lookup"><span data-stu-id="08664-126">Connections to a SQL Server store are not encrypted unless you explicitly set up SQL encryption for the connection or set up encryption of the network traffic that uses Internet Protocol Security (IPsec).</span></span>

 

<span data-ttu-id="08664-127">En el ejemplo siguiente se muestra cómo crear un objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en una base de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="08664-127">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in a SQL Server database.</span></span>


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _ 
  "MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore"

'  Save information to the store.
authStore.Submit
```



## <a name="creating-an-xml-store"></a><span data-ttu-id="08664-128">Crear un almacén XML</span><span class="sxs-lookup"><span data-stu-id="08664-128">Creating an XML Store</span></span>

<span data-ttu-id="08664-129">Administrador de autorización admite la creación de un almacén de directivas de autorización en formato XML.</span><span class="sxs-lookup"><span data-stu-id="08664-129">Authorization Manager supports creating an authorization policy store in XML format.</span></span> <span data-ttu-id="08664-130">El almacén XML puede ubicarse en el mismo equipo en el que se ejecuta la aplicación, o bien se puede almacenar de forma remota.</span><span class="sxs-lookup"><span data-stu-id="08664-130">The XML store can be located on the same computer where the application runs, or it can be stored remotely.</span></span> <span data-ttu-id="08664-131">No se admite la edición directa del archivo XML.</span><span class="sxs-lookup"><span data-stu-id="08664-131">Editing the XML file directly is not supported.</span></span> <span data-ttu-id="08664-132">Use el complemento MMC de administrador de autorización o la API de administrador de autorización para editar el almacén de directivas.</span><span class="sxs-lookup"><span data-stu-id="08664-132">Use the Authorization Manager MMC snap-in or the Authorization Manager API to edit the policy store.</span></span>

<span data-ttu-id="08664-133">Administrador de autorización no admite la delegación de la administración de un almacén de directivas XML.</span><span class="sxs-lookup"><span data-stu-id="08664-133">Authorization Manager does not support delegating administration of an XML policy store.</span></span> <span data-ttu-id="08664-134">Para obtener información acerca de la delegación, vea [delegar la definición de permisos en el script](delegating-the-defining-of-permissions-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="08664-134">For information about delegation, see [Delegating the Defining of Permissions in Script](delegating-the-defining-of-permissions-in-script.md).</span></span>

<span data-ttu-id="08664-135">En el ejemplo siguiente se muestra cómo crear un objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="08664-135">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in an XML file.</span></span>


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



