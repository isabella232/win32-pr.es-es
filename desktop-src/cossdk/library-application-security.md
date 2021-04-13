---
description: Dado que otro proceso hospeda una aplicación de biblioteca COM+, que puede tener su propia configuración de seguridad, la seguridad de las aplicaciones de biblioteca requiere una consideración especial.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Seguridad de aplicaciones de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2885173f3798d33ed26a5b447fde4429b9bf96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538716"
---
# <a name="library-application-security"></a><span data-ttu-id="0051a-103">Seguridad de aplicaciones de biblioteca</span><span class="sxs-lookup"><span data-stu-id="0051a-103">Library Application Security</span></span>

<span data-ttu-id="0051a-104">Dado que otro proceso hospeda una aplicación de biblioteca COM+, que puede tener su propia configuración de seguridad, la seguridad de las aplicaciones de biblioteca requiere una consideración especial.</span><span class="sxs-lookup"><span data-stu-id="0051a-104">Because a COM+ library application is hosted by another process, which may have its own security settings, security for library applications requires special consideration.</span></span>

<span data-ttu-id="0051a-105">Las siguientes restricciones se aplican a la seguridad de la aplicación de biblioteca:</span><span class="sxs-lookup"><span data-stu-id="0051a-105">The following constraints apply to library application security:</span></span>

-   <span data-ttu-id="0051a-106">Las aplicaciones de biblioteca se ejecutan en el token de seguridad del proceso de cliente en lugar de en su propia identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="0051a-106">Library applications run under the client process security token rather than under their own user identity.</span></span> <span data-ttu-id="0051a-107">Solo tienen los privilegios que tiene el cliente.</span><span class="sxs-lookup"><span data-stu-id="0051a-107">They have only as much privilege as the client has.</span></span>
-   <span data-ttu-id="0051a-108">Las aplicaciones de biblioteca no controlan la seguridad de nivel de proceso.</span><span class="sxs-lookup"><span data-stu-id="0051a-108">Library applications do not control process-level security.</span></span> <span data-ttu-id="0051a-109">No se agregarán usuarios en roles al descriptor de seguridad para el proceso.</span><span class="sxs-lookup"><span data-stu-id="0051a-109">No users in roles will be added to the security descriptor for the process.</span></span> <span data-ttu-id="0051a-110">La única manera de que una aplicación de biblioteca realice sus propias comprobaciones de acceso es usar la seguridad de nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="0051a-110">The only way for a library application to perform its own access checks is to use component-level security.</span></span> <span data-ttu-id="0051a-111">(Vea [límites de seguridad](security-boundaries.md)).</span><span class="sxs-lookup"><span data-stu-id="0051a-111">(See [Security Boundaries](security-boundaries.md).)</span></span>
-   <span data-ttu-id="0051a-112">Las aplicaciones de biblioteca se pueden configurar para participar o no en la autenticación del proceso de host, habilitando o deshabilitando la autenticación.</span><span class="sxs-lookup"><span data-stu-id="0051a-112">Library applications can be configured to either participate or not participate in host process authentication, by enabling or disabling authentication.</span></span> <span data-ttu-id="0051a-113">(Consulte [habilitación de la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md)).</span><span class="sxs-lookup"><span data-stu-id="0051a-113">(See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).)</span></span>
-   <span data-ttu-id="0051a-114">Las aplicaciones de biblioteca no pueden establecer un nivel de suplantación; usan el del proceso de host.</span><span class="sxs-lookup"><span data-stu-id="0051a-114">Library applications cannot set an impersonation level; they use that of the host process.</span></span>

## <a name="using-library-applications-to-limit-application-privilege"></a><span data-ttu-id="0051a-115">Usar aplicaciones de biblioteca para limitar el privilegio de aplicación</span><span class="sxs-lookup"><span data-stu-id="0051a-115">Using Library Applications to Limit Application Privilege</span></span>

<span data-ttu-id="0051a-116">En algunos casos, puede que desee configurar una aplicación específicamente como una aplicación de biblioteca para que se ejecute bajo la identidad del proceso de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="0051a-116">In some cases, you may want to configure an application specifically as a library application so that it runs under the identity of the hosting process.</span></span> <span data-ttu-id="0051a-117">Esto limita fundamentalmente la aplicación para que pueda tener acceso solo a los recursos a los que puede tener acceso el cliente, el proceso de host.</span><span class="sxs-lookup"><span data-stu-id="0051a-117">Doing so fundamentally limits the application so that it can access only those resources that its client, the host process, can access.</span></span> <span data-ttu-id="0051a-118">Los subprocesos en los que se ejecutan los componentes de la aplicación de biblioteca usarán el token de proceso de forma predeterminada y, por lo tanto, cuando realicen llamadas fuera de la aplicación o los recursos de acceso, como los archivos protegidos con un descriptor de seguridad, parecerá que son el cliente.</span><span class="sxs-lookup"><span data-stu-id="0051a-118">The threads that the library application components run on will use the process token by default, and therefore when they make calls outside of the application or access resources such as files guarded with a security descriptor, they will appear to be the client.</span></span> <span data-ttu-id="0051a-119">En el caso de las aplicaciones que realizan trabajo confidencial, puede ser una forma sencilla de controlar el ámbito de sus acciones.</span><span class="sxs-lookup"><span data-stu-id="0051a-119">For applications that perform sensitive work, this may be an easy way to control the scope of their actions.</span></span>

## <a name="effectively-securing-library-applications"></a><span data-ttu-id="0051a-120">Proteger eficazmente aplicaciones de biblioteca</span><span class="sxs-lookup"><span data-stu-id="0051a-120">Effectively Securing Library Applications</span></span>

<span data-ttu-id="0051a-121">Hay algunas consideraciones especiales para configurar la seguridad basada en roles y la autenticación para las aplicaciones de biblioteca, de modo que funcionen según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="0051a-121">There are special considerations in configuring role-based security and authentication for library applications so that they perform as expected.</span></span> <span data-ttu-id="0051a-122">Para obtener más información, consulte [configuración de la seguridad para aplicaciones de biblioteca](configuring-security-for-library-applications.md).</span><span class="sxs-lookup"><span data-stu-id="0051a-122">For details, see [Configuring Security for Library Applications](configuring-security-for-library-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0051a-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0051a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0051a-124">Autenticación de cliente</span><span class="sxs-lookup"><span data-stu-id="0051a-124">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="0051a-125">Suplantación y delegación de cliente</span><span class="sxs-lookup"><span data-stu-id="0051a-125">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="0051a-126">Seguridad de aplicaciones de niveles múltiples</span><span class="sxs-lookup"><span data-stu-id="0051a-126">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="0051a-127">Seguridad de componentes mediante programación</span><span class="sxs-lookup"><span data-stu-id="0051a-127">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="0051a-128">Administración de la seguridad basada en roles</span><span class="sxs-lookup"><span data-stu-id="0051a-128">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="0051a-129">Usar la Directiva de restricción de software en COM+</span><span class="sxs-lookup"><span data-stu-id="0051a-129">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



