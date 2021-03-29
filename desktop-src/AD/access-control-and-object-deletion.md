---
title: Access Control y eliminación de objetos
description: Active Directory le permite eliminar un objeto si tiene acceso de eliminación al objeto o ADS \_ right \_ DS \_ Delete \_ Child Access al tipo de objeto en el contenedor principal.
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- AD de Access Control y eliminación de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bddcd2b563e144743689f2a26c17bd417db14ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789430"
---
# <a name="access-control-and-object-deletion"></a><span data-ttu-id="0c62a-104">Access Control y eliminación de objetos</span><span class="sxs-lookup"><span data-stu-id="0c62a-104">Access Control and Object Deletion</span></span>

<span data-ttu-id="0c62a-105">Active Directory Domain Services le permiten eliminar un objeto si tiene uno de los siguientes derechos de acceso:</span><span class="sxs-lookup"><span data-stu-id="0c62a-105">Active Directory Domain Services enable you to delete an object if you have one of the following access rights:</span></span>

-   <span data-ttu-id="0c62a-106">ELIMINAR el acceso al propio objeto</span><span class="sxs-lookup"><span data-stu-id="0c62a-106">DELETE access to the object itself</span></span>
-   <span data-ttu-id="0c62a-107">ADS \_ derecho \_ DS \_ eliminar \_ acceso secundario para ese tipo de objeto en el contenedor primario</span><span class="sxs-lookup"><span data-stu-id="0c62a-107">ADS\_RIGHT\_DS\_DELETE\_CHILD access for that object type on the parent container</span></span>

<span data-ttu-id="0c62a-108">Tenga en cuenta que el sistema comprueba el descriptor de seguridad para el objeto y su elemento primario antes de denegar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="0c62a-108">Be aware that the system verifies the security descriptor for both the object and its parent before denying the deletion.</span></span> <span data-ttu-id="0c62a-109">Esto significa que una ACE que deniegue explícitamente el acceso de eliminación a un usuario no tiene ningún efecto si el usuario tiene \_ acceso de eliminación secundario en el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="0c62a-109">This means that an ACE that explicitly denies DELETE access to a user has no effect if the user has DELETE\_CHILD access on the parent.</span></span> <span data-ttu-id="0c62a-110">Del mismo modo, se puede invalidar una ACE que deniegue \_ el acceso de eliminación secundario en el elemento primario si se permite el acceso de eliminación en el propio objeto.</span><span class="sxs-lookup"><span data-stu-id="0c62a-110">Similarly, an ACE that denies DELETE\_CHILD access on the parent can be overridden if DELETE access is allowed on the object itself.</span></span>

<span data-ttu-id="0c62a-111">Para realizar una operación de eliminación de árbol, por ejemplo, mediante el método [**IADsDeleteOps::D eleteobject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) , debe tener el \_ acceso de árbol derecho de \_ \_ eliminación DS \_ al objeto.</span><span class="sxs-lookup"><span data-stu-id="0c62a-111">To perform a tree-delete operation, for example using the [**IADsDeleteOps::DeleteObject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) method, you must have ADS\_RIGHT\_DS\_DELETE\_TREE access to the object.</span></span> <span data-ttu-id="0c62a-112">Si tiene este derecho de acceso, puede eliminar el objeto y todos los objetos secundarios, independientemente de las protecciones de los objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="0c62a-112">If you have this access right, you can delete the object and any child objects regardless of the protections on the child objects.</span></span> <span data-ttu-id="0c62a-113">Para eliminar un árbol si no tiene ADS \_ derecho \_ DS \_ eliminar \_ árbol, debe recorrer el árbol de forma recursiva y eliminar cada objeto individualmente.</span><span class="sxs-lookup"><span data-stu-id="0c62a-113">To delete a tree if you do not have ADS\_RIGHT\_DS\_DELETE\_TREE access, you must recursively traverse the tree, deleting each object individually.</span></span> <span data-ttu-id="0c62a-114">En este caso, debe tener el acceso secundario eliminar o eliminar \_ para cada objeto del árbol.</span><span class="sxs-lookup"><span data-stu-id="0c62a-114">In this case, you must have the necessary DELETE or DELETE\_CHILD access for each object in the tree.</span></span>

> [!WARNING]
> <span data-ttu-id="0c62a-115">Si los usuarios tienen \_ derechos \_ \_ \_ de acceso de árbol de eliminación DS correctos para un objeto, esto les da la posibilidad de eliminar un subárbol completo, incluidos todos los objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="0c62a-115">If users have ADS\_RIGHT\_DS\_DELETE\_TREE access for an object, this gives them the ability to delete a whole subtree, including all child objects.</span></span> <span data-ttu-id="0c62a-116">Por esta razón, puede considerar la posibilidad de revocar el permiso de acceso "eliminar subárbol" para todos los usuarios de un contenedor primario.</span><span class="sxs-lookup"><span data-stu-id="0c62a-116">For this reason, you may consider revoking "Delete Subtree" access permission for all users on a parent container.</span></span>

 

 

 