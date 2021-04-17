---
description: Crear una nueva aplicación COM+
ms.assetid: eec4e871-36c2-4e60-9808-1400efcfc60c
title: Crear una nueva aplicación COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09eb296ad0a5f2326b5d931f59a5075d001d89f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705376"
---
# <a name="creating-a-new-com-application"></a><span data-ttu-id="924b0-103">Crear una nueva aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="924b0-103">Creating a New COM+ Application</span></span>

<span data-ttu-id="924b0-104">La creación de una nueva aplicación COM+ requiere dos pasos básicos, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="924b0-104">Creating a new COM+ application requires two basic steps, as follows:</span></span>

-   <span data-ttu-id="924b0-105">Crear una aplicación COM+ vacía (descrita a continuación).</span><span class="sxs-lookup"><span data-stu-id="924b0-105">Creating an empty COM+ application (described below).</span></span>
-   <span data-ttu-id="924b0-106">Agregar componentes a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="924b0-106">Adding components to the application.</span></span> <span data-ttu-id="924b0-107">(Consulte [instalación de nuevos componentes](installing-new-components.md) e [importación de componentes](importing-components.md)).</span><span class="sxs-lookup"><span data-stu-id="924b0-107">(See [Installing New Components](installing-new-components.md) and [Importing Components](importing-components.md).)</span></span>

<span data-ttu-id="924b0-108">**Para crear una aplicación COM+ vacía**</span><span class="sxs-lookup"><span data-stu-id="924b0-108">**To create an empty COM+ application**</span></span>

1.  <span data-ttu-id="924b0-109">En el árbol de consola de la herramienta administrativa Servicios de componentes, seleccione el equipo en el que desea crear una aplicación.</span><span class="sxs-lookup"><span data-stu-id="924b0-109">In the console tree of the Component Services administrative tool, select the computer on which you want to create an application.</span></span>

2.  <span data-ttu-id="924b0-110">Seleccione la carpeta **aplicaciones com+** para ese equipo.</span><span class="sxs-lookup"><span data-stu-id="924b0-110">Select the **COM+ Applications** folder for that computer.</span></span>

3.  <span data-ttu-id="924b0-111">En el menú **acción** , seleccione **nuevo** y, a continuación, haga clic en **aplicación**.</span><span class="sxs-lookup"><span data-stu-id="924b0-111">On the **Action** menu, point to **New**, and then click **Application**.</span></span> <span data-ttu-id="924b0-112">También puede hacer clic con el botón secundario en la carpeta **aplicaciones com+** , seleccionar **nuevo** y, a continuación, hacer clic en **aplicación**.</span><span class="sxs-lookup"><span data-stu-id="924b0-112">You can also right-click the **COM+ Applications** folder, point to **New**, and then click **Application**.</span></span>

4.  <span data-ttu-id="924b0-113">En la página **principal** del Asistente para instalación de aplicaciones com+, haga clic en **siguiente** y, en el cuadro de diálogo **instalar o crear una nueva aplicación** , haga clic en **crear una aplicación vacía**.</span><span class="sxs-lookup"><span data-stu-id="924b0-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Install or Create a New Application** dialog box, click **Create an empty application**.</span></span>

5.  <span data-ttu-id="924b0-114">En el cuadro proporcionado, escriba un nombre para la nueva aplicación.</span><span class="sxs-lookup"><span data-stu-id="924b0-114">In the box provided, type a name for the new application.</span></span> <span data-ttu-id="924b0-115">(Tenga en cuenta que los siguientes caracteres especiales no se pueden usar en un nombre de aplicación: \\ ,/, ~,!, @, \# ,%, ^, &, \* , (,), \| ,}, {, \] , \[ , ', ", >, <,.,?,:, y;.) En **tipo de activación**, haga clic en **aplicación de biblioteca** o **aplicación de servidor**.</span><span class="sxs-lookup"><span data-stu-id="924b0-115">(Note that the following special characters cannot be used in an application name: \\, /, ~, !, @, \#, %, ^, &, \*, (, ), \|, }, {, \], \[, ', ", >, <, ., ?, :, and ;.) Under **Activation type**, click **Library application** or **Server application**.</span></span> <span data-ttu-id="924b0-116">Haga clic en **Next**.</span><span class="sxs-lookup"><span data-stu-id="924b0-116">Click **Next**.</span></span>

    > [!Note]  
    > <span data-ttu-id="924b0-117">Una aplicación de servidor se ejecuta en su propio proceso.</span><span class="sxs-lookup"><span data-stu-id="924b0-117">A server application runs in its own process.</span></span> <span data-ttu-id="924b0-118">Las aplicaciones de servidor pueden admitir todos los servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="924b0-118">Server applications can support all COM+ services.</span></span> <span data-ttu-id="924b0-119">Una aplicación de biblioteca se ejecuta en el proceso del cliente que la crea.</span><span class="sxs-lookup"><span data-stu-id="924b0-119">A library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="924b0-120">Las aplicaciones de biblioteca pueden utilizar la seguridad basada en roles pero no admiten el acceso remoto o los componentes en cola.</span><span class="sxs-lookup"><span data-stu-id="924b0-120">Library applications can use role-based security but do not support remote access or queued components.</span></span>

     

6.  <span data-ttu-id="924b0-121">En el cuadro de diálogo **establecer identidad** de la aplicación, elija una identidad en la que se ejecutará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="924b0-121">In the **Set Application Identity** dialog box, choose an identity under which the application will run.</span></span> <span data-ttu-id="924b0-122">Si selecciona **este usuario**, escriba el nombre de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="924b0-122">If you select **This user**, type the user name and password.</span></span> <span data-ttu-id="924b0-123">También debe escribir la contraseña en el cuadro **Confirmar contraseña** .</span><span class="sxs-lookup"><span data-stu-id="924b0-123">You must also retype the password in the **Confirm password** box.</span></span> <span data-ttu-id="924b0-124">Haga clic en **Next**.</span><span class="sxs-lookup"><span data-stu-id="924b0-124">Click **Next**.</span></span> <span data-ttu-id="924b0-125">(La selección predeterminada de identidad de aplicación es **usuario interactivo**.</span><span class="sxs-lookup"><span data-stu-id="924b0-125">(The default selection for application identity is **Interactive User**.</span></span> <span data-ttu-id="924b0-126">El usuario interactivo es el usuario que ha iniciado sesión en el equipo servidor en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="924b0-126">The interactive user is the user logged on to the server computer at any given time.</span></span> <span data-ttu-id="924b0-127">Puede seleccionar un usuario diferente si selecciona **este usuario** y especifica un usuario o grupo específico).</span><span class="sxs-lookup"><span data-stu-id="924b0-127">You can select a different user by selecting **This user** and entering a specific user or group.)</span></span>

    > [!Note]  
    > <span data-ttu-id="924b0-128">El cuadro de diálogo **establecer identidad de aplicación** solo aparece si ha seleccionado **aplicación de servidor** para el tipo de activación de la nueva aplicación en el cuadro de diálogo anterior del Asistente para instalación de aplicaciones com.</span><span class="sxs-lookup"><span data-stu-id="924b0-128">The **Set Application Identity** dialog box appears only if you selected **Server application** for the new application's activation type in the COM Application Install Wizard's preceding dialog box.</span></span> <span data-ttu-id="924b0-129">La propiedad Identity no se utiliza para las aplicaciones de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="924b0-129">The identity property is not used for library applications.</span></span>

     

7.  <span data-ttu-id="924b0-130">En el cuadro de diálogo **Agregar roles de aplicación** , agregue los roles que desee asociar a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="924b0-130">In the **Add Application Roles** dialog box, add any roles you want to associate with the application.</span></span> <span data-ttu-id="924b0-131">De forma predeterminada, solo se define el rol **CreatorOwner** .</span><span class="sxs-lookup"><span data-stu-id="924b0-131">By default, only the **CreatorOwner** role is defined.</span></span> <span data-ttu-id="924b0-132">Para obtener información sobre los roles, consulte [Administración de la seguridad basada en roles](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="924b0-132">For information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

8.  <span data-ttu-id="924b0-133">En el cuadro de diálogo **Agregar usuarios a roles** , rellene cada rol que creó en el último paso con los usuarios, grupos o entidades de seguridad integradas a los que desea conceder los privilegios asociados a ese rol.</span><span class="sxs-lookup"><span data-stu-id="924b0-133">In the **Add Users to Roles** dialog box, populate each role you created in the last step with the users, groups, or built-in security principals to which you want to grant the privileges associated with that role.</span></span> <span data-ttu-id="924b0-134">De forma predeterminada, el usuario interactivo se coloca en el rol **CreatorOwner** .</span><span class="sxs-lookup"><span data-stu-id="924b0-134">By default, the interactive user is placed in the **CreatorOwner** role.</span></span>

9.  <span data-ttu-id="924b0-135">Haga clic en **Finalizar**</span><span class="sxs-lookup"><span data-stu-id="924b0-135">Click **Finish**.</span></span>

<span data-ttu-id="924b0-136">La nueva aplicación se mostrará en la carpeta **aplicaciones com+** en el árbol de consola de la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="924b0-136">The new application will now be displayed under the **COM+ Applications** folder in the console tree of the Component Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="924b0-137">A partir de Windows Server 2003, las comprobaciones de acceso están habilitadas de forma predeterminada al crear una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="924b0-137">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="924b0-138">En versiones anteriores, las comprobaciones de acceso estaban deshabilitadas de forma predeterminada en el nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="924b0-138">In previous versions, access checks were disabled by default at the application level.</span></span> <span data-ttu-id="924b0-139">El resultado es que, de forma predeterminada, el acceso a una aplicación COM+ solo se permite a los usuarios que están en los roles asociados con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="924b0-139">The result is that by default, access to a COM+ application is allowed only to users that are in the roles associated with the application.</span></span> <span data-ttu-id="924b0-140">(Consulte [Administración de la seguridad basada en roles](role-based-security-administration.md)). Como alternativa, puede permitir el acceso a todos los usuarios deshabilitando las comprobaciones de acceso en una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="924b0-140">(See [Role-Based Security Administration](role-based-security-administration.md).) Alternatively, you can allow access to all users by disabling access checks on a COM+ application.</span></span> <span data-ttu-id="924b0-141">(Consulte [habilitación de comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md)).</span><span class="sxs-lookup"><span data-stu-id="924b0-141">(See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md).)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="924b0-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="924b0-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="924b0-143">Copiar componentes</span><span class="sxs-lookup"><span data-stu-id="924b0-143">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="924b0-144">Eliminar una aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="924b0-144">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="924b0-145">Importar componentes</span><span class="sxs-lookup"><span data-stu-id="924b0-145">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="924b0-146">Instalación de nuevos componentes</span><span class="sxs-lookup"><span data-stu-id="924b0-146">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="924b0-147">Mover componentes</span><span class="sxs-lookup"><span data-stu-id="924b0-147">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="924b0-148">Quitar un componente de una aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="924b0-148">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



