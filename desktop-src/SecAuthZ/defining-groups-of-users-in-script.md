---
description: Un objeto IAzApplicationGroup representa un grupo de usuarios. Los roles se pueden asignar a este grupo de usuarios colectivamente. Un objeto IAzApplicationGroup también puede incluir otros objetos IAzApplicationGroup como miembros.
ms.assetid: 8b445419-7316-4034-b742-a05845af1862
title: Definir grupos de usuarios en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f0b652530167c71fbea7bc23d27434ae458f9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361386"
---
# <a name="defining-groups-of-users-in-script"></a><span data-ttu-id="5cc74-105">Definir grupos de usuarios en el script</span><span class="sxs-lookup"><span data-stu-id="5cc74-105">Defining Groups of Users in Script</span></span>

<span data-ttu-id="5cc74-106">En el administrador de autorización, un objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa un grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="5cc74-106">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="5cc74-107">Los roles se pueden asignar a este grupo de usuarios colectivamente.</span><span class="sxs-lookup"><span data-stu-id="5cc74-107">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="5cc74-108">Un objeto **IAzApplicationGroup** también puede incluir otros objetos **IAzApplicationGroup** como miembros.</span><span class="sxs-lookup"><span data-stu-id="5cc74-108">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> <span data-ttu-id="5cc74-109">Para obtener más información acerca de los grupos de aplicaciones, consulte [usuarios y grupos](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="5cc74-109">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

<span data-ttu-id="5cc74-110">Un grupo se puede definir mediante listas explícitas de miembros y no miembros, o bien mediante una consulta LDAP ( [*Protocolo ligero de acceso a directorios*](/windows/desktop/SecGloss/l-gly) ).</span><span class="sxs-lookup"><span data-stu-id="5cc74-110">A group can be defined either by explicit lists of members and nonmembers or by a [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP) query.</span></span> <span data-ttu-id="5cc74-111">En los siguientes ejemplos se muestra cómo crear cada tipo de grupo de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="5cc74-111">The following examples show how to create each type of application group:</span></span>

-   [<span data-ttu-id="5cc74-112">Creación de un grupo básico</span><span class="sxs-lookup"><span data-stu-id="5cc74-112">Creating a Basic Group</span></span>](#creating-a-basic-group)
-   [<span data-ttu-id="5cc74-113">Crear un grupo de consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="5cc74-113">Creating an LDAP Query Group</span></span>](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a><span data-ttu-id="5cc74-114">Creación de un grupo básico</span><span class="sxs-lookup"><span data-stu-id="5cc74-114">Creating a Basic Group</span></span>

<span data-ttu-id="5cc74-115">Los miembros incluidos en los [**miembros y las**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) propiedades que no son [**miembros**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) del objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) que representa el grupo definen un grupo de aplicación básico.</span><span class="sxs-lookup"><span data-stu-id="5cc74-115">A basic application group is defined by the members included in the [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) and [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) properties of the [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object that represents the group.</span></span> <span data-ttu-id="5cc74-116">Los usuarios y grupos que se enumeran en la propiedad **Members** se incluyen en el grupo de aplicaciones, y los usuarios y grupos que se enumeran en la propiedad **nonmembers** se excluyen del grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5cc74-116">Users and groups listed in the **Members** property are included in the application group, and users and groups listed in the **NonMembers** property are excluded from the application group.</span></span> <span data-ttu-id="5cc74-117">Que se enumeran en la propiedad los miembros no **miembros** se sustituyen en la propiedad **Members** .</span><span class="sxs-lookup"><span data-stu-id="5cc74-117">Being listed in the **NonMembers** property supersedes being listed in the **Members** property.</span></span>

<span data-ttu-id="5cc74-118">En el ejemplo siguiente se muestra cómo crear un grupo de aplicación básico y agregar todos los usuarios locales como miembros de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="5cc74-118">The following example shows how to create a basic application group and add all local users as members of that group.</span></span> <span data-ttu-id="5cc74-119">En el ejemplo se da por supuesto que hay un almacén de directivas XML con el nombre MyStore.xml en el directorio raíz de la unidad C.</span><span class="sxs-lookup"><span data-stu-id="5cc74-119">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Trusted Users")

'  Add a well-known SID for all local users to the group.
appGroup.AddMember("S-1-1-0")

'  Save the application group to the store.
appGroup.Submit
```



## <a name="creating-an-ldap-query-group"></a><span data-ttu-id="5cc74-120">Crear un grupo de consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="5cc74-120">Creating an LDAP Query Group</span></span>

<span data-ttu-id="5cc74-121">Un grupo de consulta LDAP tiene una pertenencia definida por la consulta contenida en el valor de su propiedad [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .</span><span class="sxs-lookup"><span data-stu-id="5cc74-121">An LDAP query group has a membership defined by the query contained in the value of its [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) property.</span></span>

<span data-ttu-id="5cc74-122">En el ejemplo siguiente se muestra cómo crear un grupo de aplicaciones de consulta LDAP y cómo agregar todos los usuarios como miembros de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="5cc74-122">The following example shows how to create an LDAP query application group and add all users as members of that group.</span></span> <span data-ttu-id="5cc74-123">En el ejemplo se da por supuesto que hay un almacén de directivas XML con el nombre MyStore.xml en el directorio raíz de la unidad C.</span><span class="sxs-lookup"><span data-stu-id="5cc74-123">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("LDAP Trusted Users")

'  Set the Type property of the group to two
'  (AZ_GROUPTYPE_LDAP_QUERY).
appGroup.Type = 2

'  Add LDAP query for all users.
appGroup.LdapQuery = ("&(objectCategory=person)(objectClass=user)")

'  Save the application group to the store.
appGroup.Submit

```



 

 
