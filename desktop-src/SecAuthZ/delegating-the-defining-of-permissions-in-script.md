---
description: Puede delegar la administración de los almacenes de directivas de autorización que se almacenan en Active Directory.
ms.assetid: a7b43dfe-f03e-4795-bbd3-746eb3449fd0
title: Delegación de la definición de permisos en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a9569f82271642a610919db8246cc6389daba309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360910"
---
# <a name="delegating-the-defining-of-permissions-in-script"></a><span data-ttu-id="46d9a-103">Delegación de la definición de permisos en el script</span><span class="sxs-lookup"><span data-stu-id="46d9a-103">Delegating the Defining of Permissions in Script</span></span>

<span data-ttu-id="46d9a-104">Puede delegar la administración de almacenes de directivas de autorización que se almacenan en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="46d9a-104">You can delegate the administration of authorization policy stores that are stored in Active Directory.</span></span> <span data-ttu-id="46d9a-105">La administración se puede delegar a usuarios y grupos en el nivel de almacén, aplicación o ámbito.</span><span class="sxs-lookup"><span data-stu-id="46d9a-105">Administration can be delegated to users and groups at the store, application, or scope level.</span></span>

<span data-ttu-id="46d9a-106">En cada nivel, hay una lista de administradores y lectores.</span><span class="sxs-lookup"><span data-stu-id="46d9a-106">At each level, there is a list of administrators and readers.</span></span> <span data-ttu-id="46d9a-107">Los administradores de un almacén, aplicación o ámbito pueden leer y modificar el almacén de directivas en el nivel delegado.</span><span class="sxs-lookup"><span data-stu-id="46d9a-107">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="46d9a-108">Los lectores pueden leer el almacén de directivas en el nivel delegado, pero no pueden modificar el almacén.</span><span class="sxs-lookup"><span data-stu-id="46d9a-108">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

<span data-ttu-id="46d9a-109">También se debe agregar un usuario o grupo que sea administrador o lector de una aplicación como usuario delegado del almacén de directivas que contiene esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="46d9a-109">A user or group that is either an administrator or a reader of an application must also be added as a delegated user of the policy store that contains that application.</span></span> <span data-ttu-id="46d9a-110">De forma similar, un usuario o grupo que sea administrador o lector de un ámbito debe agregarse como un usuario delegado de la aplicación que contiene ese ámbito.</span><span class="sxs-lookup"><span data-stu-id="46d9a-110">Similarly, a user or group that is an administrator or a reader of a scope must be added as a delegated user of the application that contains that scope.</span></span>

<span data-ttu-id="46d9a-111">**Para delegar la administración de un ámbito**</span><span class="sxs-lookup"><span data-stu-id="46d9a-111">**To delegate administration of a scope**</span></span>

1.  <span data-ttu-id="46d9a-112">Agregue el usuario o el grupo a la lista de usuarios delegados del almacén que contiene el ámbito mediante una llamada al método [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) del objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que contiene el ámbito.</span><span class="sxs-lookup"><span data-stu-id="46d9a-112">Add the user or group to the list of delegated users of the store that contains the scope by calling the [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) method of the [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that contains the scope.</span></span>
2.  <span data-ttu-id="46d9a-113">Agregue el usuario o el grupo a la lista de usuarios delegados de la aplicación que contiene el ámbito mediante una llamada al método [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) del objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) que contiene el ámbito.</span><span class="sxs-lookup"><span data-stu-id="46d9a-113">Add the user or group to the list of delegated users of the application that contains the scope by calling the [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) method of the [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object that contains the scope.</span></span>
3.  <span data-ttu-id="46d9a-114">Agregue el usuario o el grupo a la lista de administradores del ámbito llamando al método [**AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) del objeto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .</span><span class="sxs-lookup"><span data-stu-id="46d9a-114">Add the user or group to the list of administrators of the scope by calling the [**AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) method of the [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

> [!Note]  
> <span data-ttu-id="46d9a-115">Los almacenes de directivas basados en XML no admiten la delegación en cualquier nivel.</span><span class="sxs-lookup"><span data-stu-id="46d9a-115">XML-based policy stores do not support delegation at any level.</span></span>

 

<span data-ttu-id="46d9a-116">Si un ámbito dentro de un almacén de autorización almacenado en Active Directory contiene definiciones de tareas que incluyen reglas de autorización o definiciones de roles que incluyen reglas de autorización, el ámbito no se puede delegar.</span><span class="sxs-lookup"><span data-stu-id="46d9a-116">If a scope within an authorization store that is stored in Active Directory contains task definitions that include authorization rules or role definitions that include authorization rules, the scope cannot be delegated.</span></span>

<span data-ttu-id="46d9a-117">En el ejemplo siguiente se muestra cómo delegar la administración de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="46d9a-117">The following example shows how to delegate administration of an application.</span></span> <span data-ttu-id="46d9a-118">En el ejemplo se supone que existe un almacén de directivas de autorización de Active Directory en la ubicación especificada, que este almacén de directivas contiene una aplicación denominada///Expense y que esta aplicación no contiene tareas con scripts de reglas de negocios.</span><span class="sxs-lookup"><span data-stu-id="46d9a-118">The example assumes that there is an existing Active Directory authorization policy store at the specified location, that this policy store contains an application named Expense, and that this application contains no tasks with business rule scripts.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, _
    "msldap://CN=MyStore,CN=Program Data,DC=authmanager,DC=com"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Add a delegated policy user to the store.
AzManStore.AddDelegatedPolicyUserName("ExampleDomain\\UserName")

'  Add the user as an administrator of the application.
expenseApp.AddPolicyAdministratorName("ExampleDomain\\UserName")

'  Save changes to the store.
AzManStore.Submit
```



 

 



