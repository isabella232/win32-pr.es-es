---
description: Ejemplo introductorio con el catálogo de administración de COM+
ms.assetid: e9ce25aa-4fb1-4357-9f4e-5bf649e29447
title: Ejemplo introductorio con el catálogo de administración de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db24f3985538b7189534c9fef3ef279ed240e3a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677239"
---
# <a name="introductory-example-using-the-com-administration-catalog"></a><span data-ttu-id="7a23c-103">Ejemplo introductorio con el catálogo de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="7a23c-103">Introductory Example Using the COM+ Administration Catalog</span></span>

<span data-ttu-id="7a23c-104">Al utilizar mediante programación el catálogo de administración de COM+, normalmente se realizan los siguientes pasos generales (no se proporcionan en un orden estricto aquí):</span><span class="sxs-lookup"><span data-stu-id="7a23c-104">When programmatically using the COM+ Administration catalog, you typically carry out the following general steps (not given in a strict order here):</span></span>

-   <span data-ttu-id="7a23c-105">Abra una sesión de con el catálogo de COM+ en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="7a23c-105">Open a session with the COM+ catalog on the local machine.</span></span> <span data-ttu-id="7a23c-106">Opcionalmente, conéctese al catálogo de COM+ en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="7a23c-106">Optionally, connect to the COM+ catalog on a remote machine.</span></span>
-   <span data-ttu-id="7a23c-107">Realizar acciones como iniciar o detener servicios: acciones que no pertenecen a una aplicación COM+ concreta.</span><span class="sxs-lookup"><span data-stu-id="7a23c-107">Perform actions such as starting or stopping services—actions that don't pertain to a particular COM+ application.</span></span>
-   <span data-ttu-id="7a23c-108">Realizar acciones como la instalación o exportación de aplicaciones COM+, o la instalación de componentes en aplicaciones, acciones que se aplican a la lectura o escritura en archivos.</span><span class="sxs-lookup"><span data-stu-id="7a23c-108">Perform actions such as installing or exporting COM+ applications, or installing components into applications—actions that pertain to reading from or writing to files.</span></span>
-   <span data-ttu-id="7a23c-109">Agregar nuevos elementos a las recopilaciones, como crear una nueva aplicación COM+ agregando un nuevo elemento a la colección "aplicaciones".</span><span class="sxs-lookup"><span data-stu-id="7a23c-109">Add new items to collections, such as creating a new COM+ application by adding a new item to the "Applications" collection.</span></span>
-   <span data-ttu-id="7a23c-110">Establecer u obtener propiedades en un elemento de una colección.</span><span class="sxs-lookup"><span data-stu-id="7a23c-110">Set or get properties on an item in a collection.</span></span>
-   <span data-ttu-id="7a23c-111">Guardar o descartar los cambios pendientes en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="7a23c-111">Save or discard pending changes to the catalog.</span></span>
-   <span data-ttu-id="7a23c-112">Controle los errores que puedan producirse.</span><span class="sxs-lookup"><span data-stu-id="7a23c-112">Handle any errors that might occur.</span></span>

<span data-ttu-id="7a23c-113">Para mostrar el aspecto de estos pasos cuando se usan los objetos COMAdmin, se proporciona un ejemplo de Microsoft Visual Basic a continuación.</span><span class="sxs-lookup"><span data-stu-id="7a23c-113">To show what these steps look like when you use the COMAdmin objects, a Microsoft Visual Basic example is provided below.</span></span> <span data-ttu-id="7a23c-114">Ilustra brevemente algunos de los pasos típicos descritos anteriormente, como la ubicación de colecciones, la enumeración a través de una colección para recuperar un elemento y el establecimiento de propiedades en ese elemento.</span><span class="sxs-lookup"><span data-stu-id="7a23c-114">It briefly illustrates some of the typical steps described above, such as locating collections, enumerating through a collection to retrieve an item, and setting properties on that item.</span></span>

<span data-ttu-id="7a23c-115">En el ejemplo siguiente, realizará las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="7a23c-115">In the example below you will perform the following actions:</span></span>

1.  <span data-ttu-id="7a23c-116">Cree una nueva aplicación COM+, "MyHomeZoo".</span><span class="sxs-lookup"><span data-stu-id="7a23c-116">Create a new COM+ application, "MyHomeZoo".</span></span>
2.  <span data-ttu-id="7a23c-117">Instale algunos componentes, CAT y Dog, en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a23c-117">Install some components, Cat and Dog, into the application.</span></span> <span data-ttu-id="7a23c-118">Ambos componentes se encuentran en un único archivo DLL que ya debe existir: MyZoo.dll.</span><span class="sxs-lookup"><span data-stu-id="7a23c-118">Both components are contained in a single DLL that must already exist: MyZoo.dll.</span></span>
3.  <span data-ttu-id="7a23c-119">Configure la seguridad basada en roles para la aplicación definiendo dos roles: ZooKeeper y AllergicToCats.</span><span class="sxs-lookup"><span data-stu-id="7a23c-119">Configure role-based security for the application by defining two roles: ZooKeeper and AllergicToCats.</span></span>
4.  <span data-ttu-id="7a23c-120">Asigne el rol ZooKeeper a toda la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a23c-120">Assign the ZooKeeper role access to the entire application.</span></span>
5.  <span data-ttu-id="7a23c-121">Asigne el rol AllergicToCats al componente Dog.</span><span class="sxs-lookup"><span data-stu-id="7a23c-121">Assign the AllergicToCats role access to only the Dog component.</span></span>
6.  <span data-ttu-id="7a23c-122">Active las propiedades de seguridad para que se aplique la comprobación de roles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a23c-122">Turn on security properties so that role checking will be enforced for the application.</span></span>
7.  <span data-ttu-id="7a23c-123">Exporte la aplicación MyHomeZoo a un archivo para que se pueda instalar en otros equipos.</span><span class="sxs-lookup"><span data-stu-id="7a23c-123">Export the MyHomeZoo application to a file so that it can be installed on other computers.</span></span>

<span data-ttu-id="7a23c-124">Para usar este ejemplo desde Visual Basic, agregue una referencia a la biblioteca de tipos de administración de COM+.</span><span class="sxs-lookup"><span data-stu-id="7a23c-124">To use this example from Visual Basic, add a reference to the COM+ Admin Type Library.</span></span>


```VB
Function SetupMyZoo() As Boolean  ' Return False if any errors occur.

    '  Initialize error handling for this function.
    SetupMyZoo = False 
    On Error GoTo My_Error_Handler

    '  Open a session with the catalog.
    '  Instantiate a COMAdminCatalog object. 
    Dim objCatalog As COMAdminCatalog
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")

    '  Create a new COM+ application.
    '  First get the "Applications" collection from the catalog.
    Dim objApplicationsColl As COMAdminCatalogCollection
    Set objApplicationsColl = objCatalog.GetCollection("Applications")

    '  Add a new item to this collection. 
    Dim objZooApp As COMAdminCatalogObject
    Set objZooApp = objApplicationsColl.Add

    '  The "Applications" collection determines the available properties.
    '  Set the "Name" property of the new application item. 
    objZooApp.Value("Name") = "MyHomeZoo"

    '  Set the "Description" property of the new application item. 
    objZooApp.Value("Description") = "My pets at home"

    '  Save changes made to the "Applications" collection. 
    objApplicationsColl.SaveChanges

    '  Install components into the application.
    '  Use the InstallComponent method on COMAdminCatalog. 
    '  In this case, the last two parameters are passed as empty strings.
    objCatalog.InstallComponent "MyHomeZoo","MyZoo.DLL","","" 

    '  Define the roles ZooKeeper and AllergicToCats 
    '  by adding them to the "Roles" collection related to MyHomeZoo. 
    '  First get the "Roles" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Roles", 
    '  and the Key property value of objZooApp.   
    '  The Key property uniquely identifies the object, serving
    '  here to distinguish the "Roles" collection related 
    '  to MyHomeZoo from that of any other application. 
    Dim objRolesColl As COMAdminCatalogCollection
    Set objRolesColl = objApplicationsColl.GetCollection("Roles", objZooApp.Key)

    '  Add new items to this "Roles" collection. 
    Dim objZooKeeperRole As COMAdminCatalogObject
    Dim objAllergicToCatsRole As COMAdminCatalogObject
    Set objZooKeeperRole = objRolesColl.Add
    Set objAllergicToCatsRole = objRolesColl.Add

    '  Set the "Name" for the new items.
    objZooKeeperRole.Value("Name") = "ZooKeeper" 
    objAllergicToCatsRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to any items in this "Roles" collection. 
    objRolesColl.SaveChanges

    '  Assign the AllergicToCats role to the Dog component to 
    '  restrict its scope of access. (The ZooKeeper role, if assigned
    '  only at the application level, can access the whole application.)
    '  First get the "Components" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Components", and
    '  the Key property value of objZooApp. 
    Dim objZooComponentsColl As COMAdminCatalogCollection
    Set objZooComponentsColl = objApplicationsColl.GetCollection("Components", objZooApp.Key) 

    '  Find the Dog component item in this "Components" collection.
    '  First Populate the collection to read in data for all its items. 
    objZooComponentsColl.Populate

    '  Enumerate through the "Components" collection 
    '  until the Dog component item is located. 
    Dim objDog As COMAdminCatalogObject 
    For Each objDog in objZooComponentsColl
        If objDog.Name = "Dog" Then 
            Exit For
        End If
    Next 
    '  Set the role checking property at the component level for Dog.
        objDog.Value("ComponentAccessChecksEnabled") = True 

    '  Save these changes.
        objZooComponentsColl.SaveChanges
    '  Get the "RolesForComponent" collection related to the 
    '  Dog component, using the Key property of objDog. 
    Dim objRolesForDogColl As COMAdminCatalogCollection 
    Set objRolesForDogColl = objZooComponentsColl.GetCollection("RolesForComponent", objDog.Key) 

    '  Add a new item to this "RolesForComponent" collection. 
    Dim objCatSneezerRole As COMAdminCatalogObject
    Set objCatSneezerRole = objRolesForDogColl.Add

    '  Set the "Name" of the new item to be "AllergicToCats". 
    objCatSneezerRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to this "RolesForComponent" collection. 
    objRolesForDogColl.SaveChanges

    '  Now set properties to enforce role-based security. 
    '  First set role-based security at the application level.
    objZooApp.Value("ApplicationAccessChecksEnabled") = True 
    objZooApp.Value("AccessChecksLevel") = COMAdminAccessChecksApplicationComponentLevel 

    '  Save these changes.
    objApplicationsColl.SaveChanges

    '  Finally, export the new configured MyHomeZoo application to an 
    '  MSI file, used to install the application on other machines.
    '  Use the ExportApplication method on COMAdminCatalogObject.
    objCatalog.ExportApplication "MyHomeZoo", "c:\Program Files\COM applications\MyHomeZoo.MSI", 4

    '  Exit the function gracefully.
    SetupMyZoo = True

My_Error_Handler:
    If Not SetupMyZoo Then
        MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) & ")" & vbNewLine & Err.Description
    End If
    objCatSneezerRole = Nothing
    objRolesForDogColl = Nothing
    objDog = Nothing
    objZooComponentsColl = Nothing
    objAllergicToCatsRole = Nothing
    objZooKeeperRole = Nothing
    objRolesColl = Nothing
    objZooApp = Nothing
    objApplicationsColl = Nothing
    objCatalog = Nothing
Exit Function
```



## <a name="related-topics"></a><span data-ttu-id="7a23c-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a23c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a23c-126">Operaciones de administración de COM+ en transacciones</span><span class="sxs-lookup"><span data-stu-id="7a23c-126">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="7a23c-127">Control de errores de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="7a23c-127">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="7a23c-128">Información general de los objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="7a23c-128">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="7a23c-129">Recuperar recopilaciones en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="7a23c-129">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="7a23c-130">Establecer propiedades y guardar cambios en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="7a23c-130">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



