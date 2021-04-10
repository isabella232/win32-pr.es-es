---
description: Propiedad de contexto de seguridad
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Propiedad de contexto de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b061ef7c0d0d0c146b626c11fd550c48ab488a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275085"
---
# <a name="security-context-property"></a><span data-ttu-id="48850-103">Propiedad de contexto de seguridad</span><span class="sxs-lookup"><span data-stu-id="48850-103">Security Context Property</span></span>

<span data-ttu-id="48850-104">Como con cada servicio automático proporcionado por COM+, la comprobación automática de roles se basa en las propiedades incluidas en el contexto del objeto.</span><span class="sxs-lookup"><span data-stu-id="48850-104">As with every automatic service provided by COM+, automatic role checking is based on properties included on the object context.</span></span> <span data-ttu-id="48850-105">La determinación de si una comprobación de seguridad debe realizarse en una llamada a un componente se basa en la propiedad de seguridad en el contexto del objeto creado cuando se crea una instancia del componente configurado.</span><span class="sxs-lookup"><span data-stu-id="48850-105">The determination of whether a security check must be carried out on a call into a component is based on the security property on the object context created when the configured component is instantiated.</span></span>

<span data-ttu-id="48850-106">Por lo general, no es necesario preocuparse por esta propiedad. lo usa directamente COM+, no.</span><span class="sxs-lookup"><span data-stu-id="48850-106">You generally don't need to be concerned with this property; it is used directly by COM+, not you.</span></span> <span data-ttu-id="48850-107">Sin embargo, en algunas circunstancias, puede que desee tener un control estricto sobre la activación de un objeto.</span><span class="sxs-lookup"><span data-stu-id="48850-107">However, in some circumstances, you might want strict control over the activation of an object.</span></span> <span data-ttu-id="48850-108">En este caso, la propiedad de seguridad puede afectar al contexto en el que se activa el objeto.</span><span class="sxs-lookup"><span data-stu-id="48850-108">In this case, the security property can affect which context your object is activated in.</span></span> <span data-ttu-id="48850-109">Es decir, si un objeto tiene una configuración incompatible con el contexto de su creador, se activará en su propio contexto.</span><span class="sxs-lookup"><span data-stu-id="48850-109">That is, if an object has a configuration incompatible with the context of its creator, it will be activated in its own context.</span></span> <span data-ttu-id="48850-110">La propiedad de seguridad puede influir en esto, como puede ser cualquier propiedad en el contexto del objeto.</span><span class="sxs-lookup"><span data-stu-id="48850-110">The security property can influence this, as can any property on the object context.</span></span>

<span data-ttu-id="48850-111">Si no desea que la configuración de seguridad afecte a la activación, puede elegir solo la comprobación de acceso de nivel de proceso.</span><span class="sxs-lookup"><span data-stu-id="48850-111">If you don't want security settings to influence activation, you can choose process-level access checking only.</span></span> <span data-ttu-id="48850-112">De este modo se suprime la propiedad de seguridad en el contexto del objeto, aunque se deshabilita la comprobación basada en roles y la [información del contexto de llamada de seguridad](security-call-context-information.md) no está disponible.</span><span class="sxs-lookup"><span data-stu-id="48850-112">This suppresses the security property on the object context, although it effectively disables role-based checking and makes [security call context information](security-call-context-information.md) unavailable.</span></span>

<span data-ttu-id="48850-113">Para obtener más información sobre las comprobaciones de acceso de nivel de proceso, vea [límites de seguridad](security-boundaries.md).</span><span class="sxs-lookup"><span data-stu-id="48850-113">For more information about process-level access checks, see [Security Boundaries](security-boundaries.md).</span></span> <span data-ttu-id="48850-114">Para ver cómo establecer la seguridad de nivel de proceso, consulte [configuración de un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="48850-114">To see how to set process-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="48850-115">Para obtener más información sobre el contexto del objeto, vea [contextos](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="48850-115">For more information about object context, see [Contexts](com--contexts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="48850-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="48850-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48850-117">Diseñar roles de forma eficaz</span><span class="sxs-lookup"><span data-stu-id="48850-117">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="48850-118">Límites de seguridad</span><span class="sxs-lookup"><span data-stu-id="48850-118">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="48850-119">Información de contexto de llamada de seguridad</span><span class="sxs-lookup"><span data-stu-id="48850-119">Security Call Context Information</span></span>](security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="48850-120">Uso de roles para la autorización de cliente</span><span class="sxs-lookup"><span data-stu-id="48850-120">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



