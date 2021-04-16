---
description: Seguridad de aplicaciones de niveles múltiples
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Seguridad de aplicaciones de niveles múltiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150f7894c7d11e832786e31ab028f9dbac35f6e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677219"
---
# <a name="multi-tier-application-security"></a><span data-ttu-id="bdfd2-103">Seguridad de aplicaciones de niveles múltiples</span><span class="sxs-lookup"><span data-stu-id="bdfd2-103">Multi-Tier Application Security</span></span>

<span data-ttu-id="bdfd2-104">Puede encontrar opciones difíciles para decidir exactamente dónde aplicar la seguridad en una aplicación de varios niveles basada en componentes: en la base de datos de.</span><span class="sxs-lookup"><span data-stu-id="bdfd2-104">You can face difficult choices in deciding precisely where to enforce security in a multi-tier, component-based application: At the database?</span></span> <span data-ttu-id="bdfd2-105">¿En el nivel intermedio?</span><span class="sxs-lookup"><span data-stu-id="bdfd2-105">At the middle tier?</span></span> <span data-ttu-id="bdfd2-106">¿En los componentes?</span><span class="sxs-lookup"><span data-stu-id="bdfd2-106">In the components?</span></span> <span data-ttu-id="bdfd2-107">¿Alguna otra parte?</span><span class="sxs-lookup"><span data-stu-id="bdfd2-107">Somewhere else?</span></span> <span data-ttu-id="bdfd2-108">Todas?</span><span class="sxs-lookup"><span data-stu-id="bdfd2-108">Everywhere?</span></span> <span data-ttu-id="bdfd2-109">A medida que los mecanismos de seguridad aumentan en número y complejidad, el rendimiento disminuye y el comportamiento de la aplicación es menos predecible.</span><span class="sxs-lookup"><span data-stu-id="bdfd2-109">As security mechanisms increase in number and complexity, performance declines and application behavior becomes less predictable.</span></span> <span data-ttu-id="bdfd2-110">No obstante, debe asegurarse de que se protegen los datos, se siguen las reglas de negocios y se registra la actividad significativa, y la aplicación sigue funcionando para los clientes según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="bdfd2-110">Nevertheless, you must ensure that data is protected, business rules are followed, and significant activity is logged, and still have your application work for clients as intended.</span></span> <span data-ttu-id="bdfd2-111">Debe asegurarse de que todas las rutas de acceso de cliente a través de la aplicación son correctas y que los puntos de control de seguridad que tiene en su lugar serán suficientes.</span><span class="sxs-lookup"><span data-stu-id="bdfd2-111">You must be certain that every client path through your application is correct and that the security checkpoints you have in place will suffice.</span></span>

<span data-ttu-id="bdfd2-112">La decisión más difícil es a menudo si se aplica la seguridad en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="bdfd2-112">The hardest decision is often whether to enforce security at the database.</span></span> <span data-ttu-id="bdfd2-113">Históricamente, aquí es donde la seguridad es la más estricta porque se percibe como el único reino que debe ser realmente seguro, y los administradores de bases de datos son muy reticentes a confiar en otros para que apliquen seguridad para ellos.</span><span class="sxs-lookup"><span data-stu-id="bdfd2-113">Historically, this is where security is tightest because it is perceived as the one kingdom that needs to be truly secure, and database administrators are very reluctant to trust someone else to enforce security for them.</span></span> <span data-ttu-id="bdfd2-114">Pero la exigencia de seguridad en la base de datos puede resultar bastante costosa y difícil de escalar, lo que es precisamente el punto de escribir aplicaciones de varios niveles en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="bdfd2-114">But enforcing security at the database can be quite expensive and difficult to scale, which is precisely the point of writing multi-tier applications in the first place.</span></span>

<span data-ttu-id="bdfd2-115">La regla general que debe seguir con las aplicaciones escalables de varios niveles mediante COM+ es que, siempre que sea posible, debe exigir una seguridad detallada en la aplicación COM+ en el nivel intermedio.</span><span class="sxs-lookup"><span data-stu-id="bdfd2-115">The general rule to follow with scalable multi-tier applications using COM+ is that, whenever possible, you should enforce detailed security in the COM+ application at the middle tier.</span></span> <span data-ttu-id="bdfd2-116">De este modo, podrá aprovechar al máximo los servicios escalables que proporciona COM+.</span><span class="sxs-lookup"><span data-stu-id="bdfd2-116">Doing so enables you to fully leverage the scalable services provided by COM+.</span></span> <span data-ttu-id="bdfd2-117">Autentique en la base de datos solo cuando sea absolutamente necesario y evalúe completamente las implicaciones de rendimiento de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="bdfd2-117">Authenticate at the database only when you absolutely need to, and fully weigh the performance implications of doing so.</span></span>

<span data-ttu-id="bdfd2-118">Para obtener una explicación de los problemas que se deben tener en cuenta a la hora de decidir dónde realizar las comprobaciones de seguridad, consulte [decidir dónde aplicar la seguridad](deciding-where-to-enforce-security.md).</span><span class="sxs-lookup"><span data-stu-id="bdfd2-118">For a discussion of issues to consider in deciding where to perform security checks, see [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

<span data-ttu-id="bdfd2-119">Para obtener una descripción de algunos escenarios básicos de la protección de aplicaciones de niveles múltiples, vea [escenarios básicos para proteger datos en aplicaciones de varios niveles](basic-scenarios-for-securing-data-in-multi-tier-applications.md).</span><span class="sxs-lookup"><span data-stu-id="bdfd2-119">For a discussion of some basic scenarios in securing multi-tier applications, see [Basic Scenarios for Securing Data in Multi-Tier Applications](basic-scenarios-for-securing-data-in-multi-tier-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdfd2-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bdfd2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdfd2-121">Autenticación de cliente</span><span class="sxs-lookup"><span data-stu-id="bdfd2-121">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="bdfd2-122">Suplantación y delegación de cliente</span><span class="sxs-lookup"><span data-stu-id="bdfd2-122">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="bdfd2-123">Seguridad de aplicaciones de biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdfd2-123">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="bdfd2-124">Seguridad de componentes mediante programación</span><span class="sxs-lookup"><span data-stu-id="bdfd2-124">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="bdfd2-125">Administración de la seguridad basada en roles</span><span class="sxs-lookup"><span data-stu-id="bdfd2-125">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="bdfd2-126">Usar la Directiva de restricción de software en COM+</span><span class="sxs-lookup"><span data-stu-id="bdfd2-126">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



