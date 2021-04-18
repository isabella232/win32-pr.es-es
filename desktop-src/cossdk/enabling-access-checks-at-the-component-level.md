---
description: Habilitar comprobaciones de acceso en el nivel de componente
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Habilitar comprobaciones de acceso en el nivel de componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5da2de5f9d2f4f2d39f43330c8320c0bb0218bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705264"
---
# <a name="enabling-access-checks-at-the-component-level"></a><span data-ttu-id="0c79f-103">Habilitar comprobaciones de acceso en el nivel de componente</span><span class="sxs-lookup"><span data-stu-id="0c79f-103">Enabling Access Checks at the Component Level</span></span>

<span data-ttu-id="0c79f-104">Si la aplicación incluye un componente que no necesita comprobaciones de seguridad, puede decidir deshabilitar las comprobaciones de roles para ese componente con el fin de mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0c79f-104">If your application includes a component that does not need security checks, you might decide to disable role checks for that component to improve performance.</span></span> <span data-ttu-id="0c79f-105">O bien, al depurar, puede resultar útil deshabilitar la seguridad para que pueda concentrarse en otros aspectos de la funcionalidad del programa.</span><span class="sxs-lookup"><span data-stu-id="0c79f-105">Or when debugging, it might be helpful to disable security so that you can concentrate on other aspects of program functionality.</span></span>

<span data-ttu-id="0c79f-106">De forma predeterminada, cuando se instala un componente, se habilitan las comprobaciones de acceso de nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="0c79f-106">By default, when you install a component, component-level access checks are enabled.</span></span> <span data-ttu-id="0c79f-107">Sin embargo, esto solo surte efecto cuando se habilitan las [comprobaciones de acceso de nivel de aplicación](enabling-access-checks-for-an-application.md) y cuando el [nivel de seguridad](setting-a-security-level-for-access-checks.md) se establece para **realizar comprobaciones de acceso en el nivel de proceso y de componente**.</span><span class="sxs-lookup"><span data-stu-id="0c79f-107">However, this takes effect only when [application-level access checks](enabling-access-checks-for-an-application.md) are enabled and when the [security level](setting-a-security-level-for-access-checks.md) is set to **Perform access checks at the process and component level**.</span></span>

<span data-ttu-id="0c79f-108">**Para habilitar o deshabilitar las comprobaciones de acceso en el nivel de componente**</span><span class="sxs-lookup"><span data-stu-id="0c79f-108">**To enable or disable access checks at the component level**</span></span>

1.  <span data-ttu-id="0c79f-109">En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el componente para el que desea deshabilitar o habilitar las comprobaciones de rol.</span><span class="sxs-lookup"><span data-stu-id="0c79f-109">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the component for which you want to disable (or enable) role checks.</span></span> <span data-ttu-id="0c79f-110">Expanda la vista en el árbol para ver los componentes en la carpeta **componentes** .</span><span class="sxs-lookup"><span data-stu-id="0c79f-110">Expand the view in the tree to view the components in the **Components** folder.</span></span>

2.  <span data-ttu-id="0c79f-111">Haga clic con el botón secundario en el componente para el que desea habilitar las comprobaciones de roles y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="0c79f-111">Right-click the component for which you want to enable role checks, and then click **Properties**.</span></span>

3.  <span data-ttu-id="0c79f-112">En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **seguridad** .</span><span class="sxs-lookup"><span data-stu-id="0c79f-112">In the component properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="0c79f-113">Seleccione **aplicar comprobaciones de acceso de nivel de componente** para aplicar comprobaciones de nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="0c79f-113">Select **Enforce component level access checks** to enforce component-level checks.</span></span>

5.  <span data-ttu-id="0c79f-114">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c79f-114">Click **OK**.</span></span>

<span data-ttu-id="0c79f-115">La nueva configuración surtirá efecto la próxima vez que se inicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0c79f-115">The new setting will take effect the next time the application is started.</span></span>

> [!Note]  
> <span data-ttu-id="0c79f-116">A partir de Windows Server 2003, las comprobaciones de acceso de nivel de componente están deshabilitadas de forma predeterminada al crear una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="0c79f-116">As of Windows Server 2003, component-level access checks are disabled by default when creating a COM+ application.</span></span> <span data-ttu-id="0c79f-117">Las comprobaciones de acceso están habilitadas de forma predeterminada en el nivel de aplicación y deshabilitadas de forma predeterminada en el nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="0c79f-117">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="0c79f-118">Anteriormente, las comprobaciones de acceso estaban deshabilitadas de forma predeterminada en el nivel de aplicación y se habilitaban de forma predeterminada en el nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="0c79f-118">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0c79f-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0c79f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c79f-120">Asignar roles a componentes, interfaces o métodos</span><span class="sxs-lookup"><span data-stu-id="0c79f-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="0c79f-121">Configuración de la seguridad de Role-Based</span><span class="sxs-lookup"><span data-stu-id="0c79f-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="0c79f-122">Definición de roles para una aplicación</span><span class="sxs-lookup"><span data-stu-id="0c79f-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="0c79f-123">Habilitación de las comprobaciones de acceso para una aplicación</span><span class="sxs-lookup"><span data-stu-id="0c79f-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="0c79f-124">Establecimiento de un nivel de seguridad para las comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="0c79f-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



