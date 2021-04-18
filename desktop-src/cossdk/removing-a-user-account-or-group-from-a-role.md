---
description: Si cambian los privilegios de los usuarios o si los roles se agregan a una aplicación, puede trasladar una cuenta de un rol a otro.
ms.assetid: 2d81a45a-9762-48b9-8395-3c3a4dcd5e8c
title: Quitar una cuenta de usuario o un grupo de un rol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176272aef16af0d0a65d90f6a1d7628a5af232fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714886"
---
# <a name="removing-a-user-account-or-group-from-a-role"></a><span data-ttu-id="251ba-103">Quitar una cuenta de usuario o un grupo de un rol</span><span class="sxs-lookup"><span data-stu-id="251ba-103">Removing a User Account or Group from a Role</span></span>

<span data-ttu-id="251ba-104">Si cambian los privilegios de un usuario o si los roles se agregan a una aplicación, puede trasladar una cuenta de un rol a otro.</span><span class="sxs-lookup"><span data-stu-id="251ba-104">If a user's privileges change or if roles are added to an application, you can move an account from one role to another role.</span></span> <span data-ttu-id="251ba-105">Para trasladar una cuenta de usuario o un grupo de usuarios de un rol a otro, debe quitar la cuenta de usuario o el grupo de su rol actual y, a continuación, asignarlo al nuevo rol.</span><span class="sxs-lookup"><span data-stu-id="251ba-105">To move a user account or group of users from one role to another, you must remove the user account or group from its current role and then assign it to the new role.</span></span>

<span data-ttu-id="251ba-106">**Para trasladar una cuenta de usuario o un grupo de un rol a otro**</span><span class="sxs-lookup"><span data-stu-id="251ba-106">**To move a user account or group from one role to another**</span></span>

1.  <span data-ttu-id="251ba-107">Quite la cuenta de usuario o el grupo del rol al que ya no debería pertenecer, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="251ba-107">Remove the user account or group from the role that it should no longer belong to, as follows:</span></span>

    1.  <span data-ttu-id="251ba-108">En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el rol que le interesa.</span><span class="sxs-lookup"><span data-stu-id="251ba-108">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="251ba-109">Expanda la vista en el árbol de consola hasta que los usuarios del rol sean visibles.</span><span class="sxs-lookup"><span data-stu-id="251ba-109">Expand the view in the console tree until the users for the role are visible.</span></span>

    2.  <span data-ttu-id="251ba-110">Haga clic con el botón secundario en la cuenta de usuario o el grupo que desea quitar y, a continuación, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="251ba-110">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

    3.  <span data-ttu-id="251ba-111">Cuando el cuadro de diálogo **Confirmar eliminación de elemento** se lo solicite, haga clic en **sí** para eliminar la cuenta de usuario o el grupo.</span><span class="sxs-lookup"><span data-stu-id="251ba-111">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

    <span data-ttu-id="251ba-112">La cuenta de usuario o el grupo que ha quitado del rol ya no aparece en la carpeta **usuarios** .</span><span class="sxs-lookup"><span data-stu-id="251ba-112">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span>

2.  <span data-ttu-id="251ba-113">Asigne la cuenta de usuario o el grupo que ha quitado a los roles a los que se debe asignar el usuario o grupo, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="251ba-113">Assign the user account or group you have removed to the roles that the user or group should be assigned to, as follows:</span></span>

    1.  <span data-ttu-id="251ba-114">En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el rol al que desea agregar la cuenta de usuario o el grupo.</span><span class="sxs-lookup"><span data-stu-id="251ba-114">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="251ba-115">Expanda la vista en el árbol de consola hasta que los roles de la aplicación sean visibles.</span><span class="sxs-lookup"><span data-stu-id="251ba-115">Expand the view in the console tree until the application's roles are visible.</span></span>

    2.  <span data-ttu-id="251ba-116">Busque el rol al que desea agregar la cuenta de usuario o el grupo.</span><span class="sxs-lookup"><span data-stu-id="251ba-116">Locate the role to which you want to add the user account or group.</span></span>

        > [!Note]  
        > <span data-ttu-id="251ba-117">Si el rol que está buscando no se encuentra en la carpeta **roles** , el rol no se ha agregado a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="251ba-117">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="251ba-118">El desarrollador debe agregarlo a la aplicación antes de poder asignar cuentas de usuario al rol.</span><span class="sxs-lookup"><span data-stu-id="251ba-118">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

         

    3.  <span data-ttu-id="251ba-119">Haga clic con el botón secundario en la carpeta **usuarios** del rol, elija **nuevo** y, a continuación, haga clic en **usuario**.</span><span class="sxs-lookup"><span data-stu-id="251ba-119">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

    4.  <span data-ttu-id="251ba-120">En la ventana **Seleccionar usuarios o grupos** , en el panel inferior, escriba el nombre completo del usuario o grupo que desea agregar.</span><span class="sxs-lookup"><span data-stu-id="251ba-120">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="251ba-121">Si no conoce el nombre, haga clic en el botón **Opciones avanzadas** y, a continuación, haga clic en **Buscar ahora** para ver una lista de usuarios y grupos del dominio seleccionado.</span><span class="sxs-lookup"><span data-stu-id="251ba-121">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="251ba-122">Seleccione un usuario o grupo en la lista **nombre (RDN)** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="251ba-122">Select a user or group from the **Name (RDN)** list and click **OK**.</span></span>

    5.  <span data-ttu-id="251ba-123">Cuando haya terminado de agregar la cuenta de usuario o el grupo al rol, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="251ba-123">When you have finished adding the user account or group to the role, click **OK**.</span></span>

    <span data-ttu-id="251ba-124">Para cada cuenta de usuario o grupo que haya asignado al rol, aparece un icono en la carpeta **usuarios** .</span><span class="sxs-lookup"><span data-stu-id="251ba-124">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span>

<span data-ttu-id="251ba-125">La pertenencia al rol modificada para la cuenta de usuario o el grupo surte efecto la próxima vez que se inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="251ba-125">The changed role membership for the user account or group takes effect the next time the application is started.</span></span>

 

 



