---
description: Puede quitar cuentas de usuario o grupos de un rol cuando los usuarios o los miembros de los grupos ya no deben tener acceso a los recursos de la aplicación a los que está asignado el rol.
ms.assetid: d2cfa5cb-a143-41de-9aa2-7af7fce10ed7
title: Mover una cuenta de usuario o un grupo a un rol diferente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2401d792066212269d4eaa4eb11eadfef6e2d73e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153390"
---
# <a name="moving-a-user-account-or-group-to-a-different-role"></a><span data-ttu-id="80b02-103">Mover una cuenta de usuario o un grupo a un rol diferente</span><span class="sxs-lookup"><span data-stu-id="80b02-103">Moving a User Account or Group to a Different Role</span></span>

<span data-ttu-id="80b02-104">Puede quitar cuentas de usuario o grupos de un rol cuando los usuarios o los miembros de los grupos ya no deben tener acceso a los recursos de la aplicación a los que está asignado el rol.</span><span class="sxs-lookup"><span data-stu-id="80b02-104">You can remove user accounts or groups from a role when the users or members of the groups should no longer be given access to the application resources to which the role is assigned.</span></span>

<span data-ttu-id="80b02-105">**Para quitar una cuenta de usuario o un grupo de un rol**</span><span class="sxs-lookup"><span data-stu-id="80b02-105">**To remove a user account or group from a role**</span></span>

1.  <span data-ttu-id="80b02-106">En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el rol que le interesa.</span><span class="sxs-lookup"><span data-stu-id="80b02-106">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="80b02-107">Expanda la vista en el árbol de consola hasta que los usuarios del rol sean visibles.</span><span class="sxs-lookup"><span data-stu-id="80b02-107">Expand the view in the console tree until the users for the role are visible.</span></span>

2.  <span data-ttu-id="80b02-108">Haga clic con el botón secundario en la cuenta de usuario o el grupo que desea quitar y, a continuación, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="80b02-108">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

3.  <span data-ttu-id="80b02-109">Cuando el cuadro de diálogo **Confirmar eliminación de elemento** se lo solicite, haga clic en **sí** para eliminar la cuenta de usuario o el grupo.</span><span class="sxs-lookup"><span data-stu-id="80b02-109">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

<span data-ttu-id="80b02-110">La cuenta de usuario o el grupo que ha quitado del rol ya no aparece en la carpeta **usuarios** .</span><span class="sxs-lookup"><span data-stu-id="80b02-110">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span> <span data-ttu-id="80b02-111">La nueva pertenencia al rol surtirá efecto la próxima vez que se inicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="80b02-111">The new role membership takes effect the next time the application is started.</span></span> <span data-ttu-id="80b02-112">Si ha realizado cambios en la **aplicación del sistema**, debe reiniciar el equipo para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="80b02-112">If you have made changes to the **System Application**, you must restart the computer for the changes to take effect.</span></span>

 

 



