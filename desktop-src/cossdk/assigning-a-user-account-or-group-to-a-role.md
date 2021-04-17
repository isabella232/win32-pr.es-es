---
description: Puede usar la herramienta administrativa Servicios de componentes para rellenar un rol con cuentas de usuario o grupos.
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: Asignación de una cuenta de usuario o un grupo a un rol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53b37c9f0265e02c7abdf74eeaf81bd0b12e3d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714857"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a><span data-ttu-id="9b4f5-103">Asignación de una cuenta de usuario o un grupo a un rol</span><span class="sxs-lookup"><span data-stu-id="9b4f5-103">Assigning a User Account or Group to a Role</span></span>

<span data-ttu-id="9b4f5-104">Puede usar la herramienta administrativa Servicios de componentes para rellenar un rol con cuentas de usuario o grupos.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-104">You can use the Component Services administrative tool to populate a role with user accounts or groups.</span></span> <span data-ttu-id="9b4f5-105">La mejor manera de asignar una cuenta de usuario a un rol es asignar la cuenta de usuario a un grupo y, a continuación, asignar el grupo al rol.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-105">The preferred way to assign a user account to a role is to assign the user account to a group and then assign the group to the role.</span></span> <span data-ttu-id="9b4f5-106">El uso de grupos para rellenar roles facilita la administración de un gran número de usuarios.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-106">Using groups to populate roles makes it easier for you to manage large numbers of users.</span></span> <span data-ttu-id="9b4f5-107">En la ayuda en pantalla de la herramienta administrativa administración de equipos, vea el tema "usuarios y grupos locales" para obtener más información acerca de la creación de grupos o la asignación de una cuenta de usuario a un grupo.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-107">In the online help for the Computer Management administrative tool, see the topic "Local Users and Groups" for more information about creating groups or assigning a user account to a group.</span></span>

> [!Note]  
> <span data-ttu-id="9b4f5-108">Para permitir que los usuarios de red sin autenticar ejecuten una aplicación COM+, los roles de aplicación deben incluir el usuario anónimo.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-108">To allow unauthenticated network users to run a COM+ application, the application roles must include the Anonymous user.</span></span> <span data-ttu-id="9b4f5-109">A partir de Windows Server 2003, de forma predeterminada, el usuario anónimo no se incluye en el grupo todos.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-109">Starting with Windows Server 2003, by default, the Anonymous user is not included in the Everyone group.</span></span>

 

<span data-ttu-id="9b4f5-110">Después de asignar la cuenta de usuario al grupo de Windows adecuado, siga estos pasos para asignar el grupo de Windows al rol.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-110">After you have assigned the user account to the appropriate Windows group, follow these steps to assign the Windows group to the role.</span></span>

<span data-ttu-id="9b4f5-111">**Para asignar un grupo de Windows a un rol de seguridad**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-111">**To assign a Windows group to a security role**</span></span>

1.  <span data-ttu-id="9b4f5-112">En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el rol al que desea agregar la cuenta de usuario o el grupo.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-112">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="9b4f5-113">Expanda la vista en el árbol de consola hasta que los roles de la aplicación sean visibles.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-113">Expand the view in the console tree until the application's roles are visible.</span></span>

2.  <span data-ttu-id="9b4f5-114">Busque el rol al que desea agregar la cuenta de usuario o el grupo.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-114">Locate the role to which you want to add the user account or group.</span></span>

    > [!Note]  
    > <span data-ttu-id="9b4f5-115">Si el rol que está buscando no se encuentra en la carpeta **roles** , el rol no se ha agregado a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-115">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="9b4f5-116">El desarrollador debe agregarlo a la aplicación antes de poder asignar cuentas de usuario al rol.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-116">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

     

3.  <span data-ttu-id="9b4f5-117">Haga clic con el botón secundario en la carpeta **usuarios** del rol, elija **nuevo** y, a continuación, haga clic en **usuario**.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-117">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

4.  <span data-ttu-id="9b4f5-118">En la ventana **Seleccionar usuarios o grupos** , en el panel inferior, escriba el nombre completo del usuario o grupo que desea agregar.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-118">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="9b4f5-119">Si no conoce el nombre, haga clic en el botón **Opciones avanzadas** y, a continuación, haga clic en **Buscar ahora** para ver una lista de usuarios y grupos del dominio seleccionado.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-119">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="9b4f5-120">Seleccione un usuario o grupo en la lista **nombre (RDN)** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-120">Select a user or group from the **Name (RDN)** list, and click **OK**.</span></span>

5.  <span data-ttu-id="9b4f5-121">Para agregar más cuentas de usuario o grupos, repita el paso 4.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-121">To add more user accounts or groups, repeat step 4.</span></span>

6.  <span data-ttu-id="9b4f5-122">Cuando haya terminado de agregar cuentas de usuario y grupos al rol, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-122">When you have finished adding user accounts and groups to the role, click **OK**.</span></span>

<span data-ttu-id="9b4f5-123">Para cada cuenta de usuario o grupo que haya asignado al rol, aparece un icono en la carpeta **usuarios** .</span><span class="sxs-lookup"><span data-stu-id="9b4f5-123">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span> <span data-ttu-id="9b4f5-124">La nueva pertenencia al rol surtirá efecto la próxima vez que se inicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9b4f5-124">The new role membership takes effect the next time the application is started.</span></span>

 

 



