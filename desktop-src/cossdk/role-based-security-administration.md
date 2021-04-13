---
description: Administración de la seguridad de Role-Based
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Administración de la seguridad de Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714cede74e105a68b0a5fed2371858054add954e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539183"
---
# <a name="role-based-security-administration"></a><span data-ttu-id="b8617-103">Administración de la seguridad de Role-Based</span><span class="sxs-lookup"><span data-stu-id="b8617-103">Role-Based Security Administration</span></span>

<span data-ttu-id="b8617-104">La seguridad basada en roles es un servicio automático proporcionado por COM+ que permite construir y aplicar de forma administrativa una directiva de control de acceso para la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="b8617-104">Role-based security is an automatic service provided by COM+ that enables you to administratively construct and enforce an access control policy for your COM+ application.</span></span> <span data-ttu-id="b8617-105">Con un modelo de configuración de seguridad flexible y extensible, la seguridad basada en roles ofrece una ventaja considerable en cuanto a la aplicación de toda la seguridad dentro de los componentes y proporciona las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="b8617-105">With a flexible and extensible security configuration model, role-based security offers a considerable advantage over enforcing all security within your components and provides the following benefits:</span></span>

-   <span data-ttu-id="b8617-106">Puede configurar la seguridad de forma administrativa mediante la herramienta administrativa Servicios de componentes o las funciones administrativas.</span><span class="sxs-lookup"><span data-stu-id="b8617-106">You can configure security administratively, using either the Component Services administrative tool or the Administrative functions.</span></span>
-   <span data-ttu-id="b8617-107">No es necesario escribir lógica relacionada con la seguridad en los componentes cuando la protección de roles en el nivel de método proporciona un control de acceso suficiente.</span><span class="sxs-lookup"><span data-stu-id="b8617-107">You don't have to write security-related logic into your components when role protection at the method level provides you with fine enough access control.</span></span>
-   <span data-ttu-id="b8617-108">No tiene que factorizar la seguridad en el diseño de interfaces o componentes.</span><span class="sxs-lookup"><span data-stu-id="b8617-108">You don't have to factor security into interface or component design.</span></span> <span data-ttu-id="b8617-109">En su lugar, puede establecer la seguridad para cada método.</span><span class="sxs-lookup"><span data-stu-id="b8617-109">Instead, you can set security on a method-by-method basis.</span></span>
-   <span data-ttu-id="b8617-110">Puede centrarse en la estructura de la Directiva de seguridad que desea aplicar y, a través de los roles, la Directiva se puede expresar claramente en los administradores que implementan la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b8617-110">You can focus on the structure of the security policy you want to enforce, and through roles, that policy can be clearly expressed to the administrators deploying your application.</span></span>
-   <span data-ttu-id="b8617-111">Puede modificar fácilmente una directiva de seguridad para adaptarse a los requisitos de seguridad en constante evolución de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b8617-111">You can easily modify a security policy to adapt to evolving security requirements for an application.</span></span>
-   <span data-ttu-id="b8617-112">Puede crear directivas de seguridad más granulares mediante programación si es necesario, mediante el uso de la seguridad basada en roles como plataforma auxiliar.</span><span class="sxs-lookup"><span data-stu-id="b8617-112">You can build more granular security policies programmatically if you need to, using role-based security as a supporting platform.</span></span>
-   <span data-ttu-id="b8617-113">Puede aprovechar la seguridad basada en roles para realizar auditorías detalladas, ya que puede obtener información de seguridad del autor de la llamada para toda una cadena de llamadas de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="b8617-113">You can leverage role-based security to do detailed auditing, because you can obtain caller security information for an entire chain of upstream calls.</span></span>

> [!Note]  
> <span data-ttu-id="b8617-114">Los usuarios de la función Administrador de la aplicación del sistema deben ser miembros del grupo local Administradores.</span><span class="sxs-lookup"><span data-stu-id="b8617-114">Users in the Administrator role for the System Application must be members of the local administrators group.</span></span> <span data-ttu-id="b8617-115">Además, a partir de Windows Server 2003, la capacidad de autenticación para la aplicación del sistema COM+ incluye el valor EOAC \_ Disable \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="b8617-115">Also, as of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="b8617-116">Este valor, que deshabilita las activaciones de activación como activador (AAA), se utiliza en la llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) al iniciar la aplicación del sistema.</span><span class="sxs-lookup"><span data-stu-id="b8617-116">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="b8617-117">Establecer la capacidad de autenticación en EOAC \_ deshabilitar \_ AAA permite que una aplicación que se ejecuta en una cuenta con privilegios (como LocalSystem) ayude a evitar que se use su identidad para iniciar componentes que no son de confianza.</span><span class="sxs-lookup"><span data-stu-id="b8617-117">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

 

<span data-ttu-id="b8617-118">Vea los temas siguientes en esta sección para obtener información acerca de cómo funcionan la seguridad basada en roles y los problemas que se deben tener en cuenta cuando se usa para construir una directiva de seguridad para una aplicación:</span><span class="sxs-lookup"><span data-stu-id="b8617-118">See the following topics in this section for information about how role-based security works and issues to consider when using it to construct a security policy for an application:</span></span>

-   [<span data-ttu-id="b8617-119">Uso de roles para la autorización de cliente</span><span class="sxs-lookup"><span data-stu-id="b8617-119">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
-   [<span data-ttu-id="b8617-120">Diseñar roles de forma eficaz</span><span class="sxs-lookup"><span data-stu-id="b8617-120">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
-   [<span data-ttu-id="b8617-121">Límites de seguridad</span><span class="sxs-lookup"><span data-stu-id="b8617-121">Security Boundaries</span></span>](security-boundaries.md)
-   [<span data-ttu-id="b8617-122">Información de contexto de llamada de seguridad</span><span class="sxs-lookup"><span data-stu-id="b8617-122">Security Call Context Information</span></span>](security-call-context-information.md)
-   [<span data-ttu-id="b8617-123">Propiedad de contexto de seguridad</span><span class="sxs-lookup"><span data-stu-id="b8617-123">Security Context Property</span></span>](security-context-property.md)

<span data-ttu-id="b8617-124">Para obtener descripciones detalladas de los pasos necesarios para configurar la seguridad basada en roles de una aplicación, consulte Configuración de la [seguridad de Role-Based](configuring-role-based-security.md).</span><span class="sxs-lookup"><span data-stu-id="b8617-124">For detailed how-to descriptions of the steps involved in configuring role-based security for an application, see [Configuring Role-Based Security](configuring-role-based-security.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8617-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8617-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8617-126">Autenticación de cliente</span><span class="sxs-lookup"><span data-stu-id="b8617-126">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="b8617-127">Suplantación y delegación de cliente</span><span class="sxs-lookup"><span data-stu-id="b8617-127">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="b8617-128">Seguridad de aplicaciones de biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8617-128">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="b8617-129">Seguridad de aplicaciones de niveles múltiples</span><span class="sxs-lookup"><span data-stu-id="b8617-129">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="b8617-130">Seguridad de componentes mediante programación</span><span class="sxs-lookup"><span data-stu-id="b8617-130">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="b8617-131">Usar la Directiva de restricción de software en COM+</span><span class="sxs-lookup"><span data-stu-id="b8617-131">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
