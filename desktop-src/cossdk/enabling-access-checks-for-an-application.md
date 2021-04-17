---
description: Al realizar este paso, se habilitan las comprobaciones de acceso al proceso o la seguridad basada en roles completa, según el nivel de seguridad que seleccione y si habilita la comprobación de acceso para componentes individuales.
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: Habilitación de las comprobaciones de acceso para una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696104"
---
# <a name="enabling-access-checks-for-an-application"></a><span data-ttu-id="c08ed-103">Habilitación de las comprobaciones de acceso para una aplicación</span><span class="sxs-lookup"><span data-stu-id="c08ed-103">Enabling Access Checks for an Application</span></span>

<span data-ttu-id="c08ed-104">Al realizar este paso, se habilitan las comprobaciones de acceso al proceso o la seguridad basada en roles completa, según el nivel de seguridad que seleccione y si habilita la comprobación de acceso para componentes individuales.</span><span class="sxs-lookup"><span data-stu-id="c08ed-104">Performing this step enables either process access checks or full role-based security, depending on what security level you select and whether you enable access checking for individual components.</span></span>

<span data-ttu-id="c08ed-105">**Para habilitar las comprobaciones de acceso para una aplicación**</span><span class="sxs-lookup"><span data-stu-id="c08ed-105">**To enable access checks for an application**</span></span>

1.  <span data-ttu-id="c08ed-106">En el árbol de consola de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en la aplicación COM+ para la que desea habilitar las comprobaciones de acceso y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="c08ed-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="c08ed-107">En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .</span><span class="sxs-lookup"><span data-stu-id="c08ed-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="c08ed-108">Active la casilla **exigir comprobaciones de acceso para esta aplicación** .</span><span class="sxs-lookup"><span data-stu-id="c08ed-108">Select the **Enforce access checks for this application** check box.</span></span>

4.  <span data-ttu-id="c08ed-109">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="c08ed-109">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="c08ed-110">A partir de Windows Server 2003, las comprobaciones de acceso están habilitadas de forma predeterminada al crear una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="c08ed-110">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="c08ed-111">Las comprobaciones de acceso están habilitadas de forma predeterminada en el nivel de aplicación y deshabilitadas de forma predeterminada en el nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="c08ed-111">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="c08ed-112">Anteriormente, las comprobaciones de acceso estaban deshabilitadas de forma predeterminada en el nivel de aplicación y se habilitaban de forma predeterminada en el nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="c08ed-112">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

<span data-ttu-id="c08ed-113">Después de habilitar las comprobaciones de acceso, debe seleccionar el nivel de seguridad adecuado.</span><span class="sxs-lookup"><span data-stu-id="c08ed-113">After enabling access checks, you should select the appropriate security level.</span></span> <span data-ttu-id="c08ed-114">Consulte [configuración de un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="c08ed-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span> <span data-ttu-id="c08ed-115">Además, debe asegurarse de definir roles y agregarlos a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c08ed-115">Also, you must be sure to define roles and add them to the application.</span></span> <span data-ttu-id="c08ed-116">Si se habilitan las comprobaciones de acceso pero no se ha agregado ningún rol, se producirá un error en todas las llamadas a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c08ed-116">If access checks are enabled but no roles have been added, all calls to the application will fail.</span></span> <span data-ttu-id="c08ed-117">Consulte [definición de roles para una aplicación](defining-roles-for-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="c08ed-117">See [Defining Roles for an Application](defining-roles-for-an-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="c08ed-118">Al depurar la aplicación, puede resultar útil deshabilitar la seguridad para que pueda concentrarse en otros aspectos del diseño y el comportamiento de su programa.</span><span class="sxs-lookup"><span data-stu-id="c08ed-118">When debugging your application, it might be helpful to disable security so that you can concentrate on other aspects of your program's behavior and design.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c08ed-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c08ed-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c08ed-120">Asignar roles a componentes, interfaces o métodos</span><span class="sxs-lookup"><span data-stu-id="c08ed-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="c08ed-121">Configuración de la seguridad de Role-Based</span><span class="sxs-lookup"><span data-stu-id="c08ed-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="c08ed-122">Definición de roles para una aplicación</span><span class="sxs-lookup"><span data-stu-id="c08ed-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="c08ed-123">Habilitar comprobaciones de acceso en el nivel de componente</span><span class="sxs-lookup"><span data-stu-id="c08ed-123">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="c08ed-124">Establecimiento de un nivel de seguridad para las comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="c08ed-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



