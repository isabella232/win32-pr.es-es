---
description: Una vez que haya habilitado las comprobaciones de acceso, para la aplicación COM+, debe seleccionar el nivel en el que desea que se realicen las comprobaciones de acceso.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Establecimiento de un nivel de seguridad para las comprobaciones de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646a49a4966bff7c593f12cb7481f4a4aad8859e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153385"
---
# <a name="setting-a-security-level-for-access-checks"></a><span data-ttu-id="057b5-103">Establecimiento de un nivel de seguridad para las comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="057b5-103">Setting a Security Level for Access Checks</span></span>

<span data-ttu-id="057b5-104">Una vez que haya habilitado las [comprobaciones de acceso](enabling-access-checks-for-an-application.md), para la aplicación com+, debe seleccionar el nivel en el que desea que se realicen las comprobaciones de acceso.</span><span class="sxs-lookup"><span data-stu-id="057b5-104">After you have enabled [access checks](enabling-access-checks-for-an-application.md), for your COM+ application, you must select the level at which you wish to have access checks performed.</span></span>

<span data-ttu-id="057b5-105">**Para seleccionar un nivel de seguridad**</span><span class="sxs-lookup"><span data-stu-id="057b5-105">**To select a security level**</span></span>

1.  <span data-ttu-id="057b5-106">En el árbol de consola de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en la aplicación COM+ para la que desea habilitar las comprobaciones de acceso y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="057b5-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="057b5-107">En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .</span><span class="sxs-lookup"><span data-stu-id="057b5-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="057b5-108">En **nivel de seguridad**, seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="057b5-108">Under **Security level**, select one of the following:</span></span>

    -   <span data-ttu-id="057b5-109">**Realizar comprobaciones de acceso solo en el nivel de proceso**: este valor indica que los usuarios de roles asignados a la aplicación se agregarán al descriptor de seguridad del proceso.</span><span class="sxs-lookup"><span data-stu-id="057b5-109">**Perform access checks only at the process level**— This setting indicates that users in roles that are assigned to the application will be added to the process security descriptor.</span></span> <span data-ttu-id="057b5-110">Esto tiene los siguientes efectos e implicaciones:</span><span class="sxs-lookup"><span data-stu-id="057b5-110">This has the following effects and implications:</span></span>

        <span data-ttu-id="057b5-111">La comprobación de roles específica se desactiva en los niveles de componente, método y interfaz.</span><span class="sxs-lookup"><span data-stu-id="057b5-111">Fine-grained role checking is turned off at the component, method, and interface levels.</span></span> <span data-ttu-id="057b5-112">Las comprobaciones de seguridad solo se realizan en el nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="057b5-112">Security checks are performed only at the application level.</span></span>

        <span data-ttu-id="057b5-113">La propiedad Security no se incluye en el contexto de los objetos que se ejecutan dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="057b5-113">The security property is not included on the context for any objects running within the application.</span></span> <span data-ttu-id="057b5-114">Esto puede afectar al modo en que se activan los objetos.</span><span class="sxs-lookup"><span data-stu-id="057b5-114">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="057b5-115">Vea [propiedad de contexto de seguridad](security-context-property.md).</span><span class="sxs-lookup"><span data-stu-id="057b5-115">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="057b5-116">El contexto de la llamada de seguridad no estará disponible.</span><span class="sxs-lookup"><span data-stu-id="057b5-116">The security call context will not be made available.</span></span> <span data-ttu-id="057b5-117">La seguridad mediante programación que se basa en la información de contexto de llamada de seguridad no funcionará.</span><span class="sxs-lookup"><span data-stu-id="057b5-117">Programmatic security that relies on security call context information will not function.</span></span> <span data-ttu-id="057b5-118">Vea [información sobre el contexto de llamada de seguridad](security-call-context-information.md).</span><span class="sxs-lookup"><span data-stu-id="057b5-118">See [Security Call Context Information](security-call-context-information.md).</span></span>

    -   <span data-ttu-id="057b5-119">**Realizar comprobaciones de acceso en el nivel de proceso y de componente**: este valor indica que se realizarán comprobaciones de descriptores de seguridad de nivel de proceso y comprobaciones completas de seguridad basadas en roles.</span><span class="sxs-lookup"><span data-stu-id="057b5-119">**Perform access checks at the process and component level**—This setting indicates that process-level security descriptor checks and full role-based security checks will be performed.</span></span> <span data-ttu-id="057b5-120">Esto tiene los siguientes efectos e implicaciones:</span><span class="sxs-lookup"><span data-stu-id="057b5-120">This has the following effects and implications:</span></span>

        <span data-ttu-id="057b5-121">Para habilitar la comprobación de roles para componentes concretos, debe [habilitar las comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md).</span><span class="sxs-lookup"><span data-stu-id="057b5-121">To enable role checking for particular components, you must [enable access checks at the component level](enabling-access-checks-at-the-component-level.md).</span></span>

        <span data-ttu-id="057b5-122">La propiedad de seguridad se incluye en el contexto de los objetos que se ejecutan dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="057b5-122">The security property is included on the context for any objects running within the application.</span></span> <span data-ttu-id="057b5-123">Esto puede afectar al modo en que se activan los objetos.</span><span class="sxs-lookup"><span data-stu-id="057b5-123">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="057b5-124">Vea [propiedad de contexto de seguridad](security-context-property.md).</span><span class="sxs-lookup"><span data-stu-id="057b5-124">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="057b5-125">El contexto de la llamada de seguridad está disponible.</span><span class="sxs-lookup"><span data-stu-id="057b5-125">The security call context is available.</span></span> <span data-ttu-id="057b5-126">La seguridad basada en roles de programación está habilitada.</span><span class="sxs-lookup"><span data-stu-id="057b5-126">Programmatic role-based security is enabled.</span></span> <span data-ttu-id="057b5-127">Vea [información sobre el contexto de llamada de seguridad](security-call-context-information.md).</span><span class="sxs-lookup"><span data-stu-id="057b5-127">See [Security Call Context Information](security-call-context-information.md).</span></span>

        > [!Note]  
        > <span data-ttu-id="057b5-128">En el caso de las aplicaciones de biblioteca COM+, debe elegir entre los niveles de componente en proceso y en los componentes para que funcionen todas las comprobaciones de acceso significativas.</span><span class="sxs-lookup"><span data-stu-id="057b5-128">For COM+ library applications, you must choose to check both at process and at component levels for any meaningful access checking to work.</span></span> <span data-ttu-id="057b5-129">Las aplicaciones de biblioteca se basan en el proceso de host para la seguridad de nivel de proceso.</span><span class="sxs-lookup"><span data-stu-id="057b5-129">Library applications rely on the host process for process-level security.</span></span> <span data-ttu-id="057b5-130">Puede determinar cómo interactúa la aplicación de biblioteca con la autenticación realizada por el proceso de host mediante la configuración de la [autenticación](enabling-authentication-for-a-library-application.md).</span><span class="sxs-lookup"><span data-stu-id="057b5-130">You can determine how the library application interacts with authentication performed by the host process by [setting authentication](enabling-authentication-for-a-library-application.md).</span></span> <span data-ttu-id="057b5-131">Para obtener más información, vea [seguridad de aplicaciones de biblioteca](library-application-security.md).</span><span class="sxs-lookup"><span data-stu-id="057b5-131">For more information, see [Library Application Security](library-application-security.md).</span></span>

         

4.  <span data-ttu-id="057b5-132">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="057b5-132">Click **OK**.</span></span>

<span data-ttu-id="057b5-133">La próxima vez que se inicie la aplicación, la seguridad se comprobará automáticamente en el nivel especificado.</span><span class="sxs-lookup"><span data-stu-id="057b5-133">The next time the application is started, security will automatically be checked at the specified level.</span></span> <span data-ttu-id="057b5-134">Solo se concederá acceso a la aplicación a los usuarios asignados a los roles asignados a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="057b5-134">Only users assigned to roles assigned to the application will be given access to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="057b5-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="057b5-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="057b5-136">Asignar roles a componentes, interfaces o métodos</span><span class="sxs-lookup"><span data-stu-id="057b5-136">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="057b5-137">Configuración de la seguridad de Role-Based</span><span class="sxs-lookup"><span data-stu-id="057b5-137">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="057b5-138">Definición de roles para una aplicación</span><span class="sxs-lookup"><span data-stu-id="057b5-138">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="057b5-139">Habilitación de las comprobaciones de acceso para una aplicación</span><span class="sxs-lookup"><span data-stu-id="057b5-139">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="057b5-140">Habilitar comprobaciones de acceso en el nivel de componente</span><span class="sxs-lookup"><span data-stu-id="057b5-140">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



