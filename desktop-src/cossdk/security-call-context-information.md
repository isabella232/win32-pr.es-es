---
description: Información de contexto de llamada de seguridad
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Información de contexto de llamada de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213e21d684d004ed18e5b9aa536e03ae8292307e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275087"
---
# <a name="security-call-context-information"></a><span data-ttu-id="fb521-103">Información de contexto de llamada de seguridad</span><span class="sxs-lookup"><span data-stu-id="fb521-103">Security Call Context Information</span></span>

<span data-ttu-id="fb521-104">La seguridad basada en roles se basa en un mecanismo general que permite recuperar información de seguridad con respecto a todos los llamadores ascendentes en la cadena de llamadas al componente.</span><span class="sxs-lookup"><span data-stu-id="fb521-104">Role-based security is built on a general mechanism that enables you to retrieve security information regarding all upstream callers in the chain of calls to your component.</span></span> <span data-ttu-id="fb521-105">Esta información solo está disponible cuando tiene habilitada la comprobación de roles de nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="fb521-105">This information is available only when you have component-level role checking enabled.</span></span> <span data-ttu-id="fb521-106">Para obtener más información sobre cómo establecer la seguridad de nivel de componente, vea [establecer un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="fb521-106">For details about how to set component-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="fb521-107">Puede utilizar la interfaz [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) para tener acceso a la información de contexto de llamadas de seguridad mediante programación.</span><span class="sxs-lookup"><span data-stu-id="fb521-107">You can use the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface to access security call context information programmatically.</span></span> <span data-ttu-id="fb521-108">Para obtener una descripción, vea [seguridad de componentes de programación](programmatic-component-security.md).</span><span class="sxs-lookup"><span data-stu-id="fb521-108">For a description, see [Programmatic Component Security](programmatic-component-security.md).</span></span>

<span data-ttu-id="fb521-109">El contexto de la llamada de seguridad se pasa a cada vez que se cruza un límite de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fb521-109">Security call context is passed along every time a security boundary is crossed.</span></span> <span data-ttu-id="fb521-110">En el caso de las llamadas entre los componentes de una aplicación, que residen dentro del mismo límite de seguridad, no se pasa ninguna información de contexto de llamada.</span><span class="sxs-lookup"><span data-stu-id="fb521-110">For calls between components within an application, which reside within the same security boundary, no call context information is passed.</span></span> <span data-ttu-id="fb521-111">En el caso de las llamadas entre procesos o entre aplicaciones dentro de un proceso, los flujos de información del contexto de llamada se transmiten.</span><span class="sxs-lookup"><span data-stu-id="fb521-111">For calls between processes or between applications within a process, call context information flows along.</span></span>

<span data-ttu-id="fb521-112">Esta característica es especialmente útil si desea realizar auditorías y registros detallados.</span><span class="sxs-lookup"><span data-stu-id="fb521-112">This facility is particularly useful if you wish to do detailed auditing and logging.</span></span> <span data-ttu-id="fb521-113">Puede recuperar y registrar información de seguridad para cada llamador de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="fb521-113">You can retrieve and record security information for every upstream caller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb521-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb521-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb521-115">Diseñar roles de forma eficaz</span><span class="sxs-lookup"><span data-stu-id="fb521-115">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="fb521-116">Límites de seguridad</span><span class="sxs-lookup"><span data-stu-id="fb521-116">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="fb521-117">Propiedad de contexto de seguridad</span><span class="sxs-lookup"><span data-stu-id="fb521-117">Security Context Property</span></span>](security-context-property.md)
</dt> <dt>

[<span data-ttu-id="fb521-118">Uso de roles para la autorización de cliente</span><span class="sxs-lookup"><span data-stu-id="fb521-118">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



