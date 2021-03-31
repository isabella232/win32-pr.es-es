---
description: El propósito de la regla de directiva de autorización central (CAPR) es proporcionar una definición en todo el dominio de un aspecto aislado de la Directiva de autorización de la organización.
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: Regla de directiva de autorización central
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda6279b2bf28f80f99a0e2608b5bf209855a76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083500"
---
# <a name="central-authorization-policy-rule"></a><span data-ttu-id="09b48-103">Regla de directiva de autorización central</span><span class="sxs-lookup"><span data-stu-id="09b48-103">Central Authorization Policy Rule</span></span>

<span data-ttu-id="09b48-104">El propósito de la regla de directiva de autorización central (CAPR) es proporcionar una definición en todo el dominio de un aspecto aislado de la Directiva de autorización de la organización.</span><span class="sxs-lookup"><span data-stu-id="09b48-104">The purpose of the Central Authorization Policy Rule (CAPR) is to provide a domain-wide definition of an isolated aspect of the organization's authorization policy.</span></span> <span data-ttu-id="09b48-105">El administrador define el CAPR para que aplique uno de los requisitos de autorización específicos.</span><span class="sxs-lookup"><span data-stu-id="09b48-105">The administrator defines the CAPR to enforce one of the specific authorization requirements.</span></span> <span data-ttu-id="09b48-106">Puesto que CAPR define solo un requisito concreto de la Directiva de autorización, se puede definir y entender más fácilmente que si todos los requisitos de la Directiva de autorización de la organización se compilan en una única definición de directiva.</span><span class="sxs-lookup"><span data-stu-id="09b48-106">Since the CAPR defines only one specific desired requirement of the authorization policy it can be more simply defined and understood than if all the authorization policy requirements of the organization are compiled into a single policy definition.</span></span>

<span data-ttu-id="09b48-107">CAPR tiene los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="09b48-107">The CAPR has the following attributes:</span></span>

-   <span data-ttu-id="09b48-108">Nombre: identifica el CAPR para los administradores.</span><span class="sxs-lookup"><span data-stu-id="09b48-108">Name – identifies the CAPR to the administrators.</span></span>
-   <span data-ttu-id="09b48-109">Descripción: define el propósito del CAPR y cualquier información que puedan necesitar los consumidores de la CAPR.</span><span class="sxs-lookup"><span data-stu-id="09b48-109">Description – defines the purpose of the CAPR and any information that may be needed by consumers of the CAPR.</span></span>
-   <span data-ttu-id="09b48-110">Expresión de aplicabilidad: define los recursos o las situaciones en las que se aplicará la Directiva.</span><span class="sxs-lookup"><span data-stu-id="09b48-110">Applicability Expression – defines the resources or situations in which the policy will be applied.</span></span>
-   <span data-ttu-id="09b48-111">ID: identificador que se usa en la auditoría de cambios en CAPR.</span><span class="sxs-lookup"><span data-stu-id="09b48-111">ID – identifier for use in auditing of changes to the CAPR.</span></span>
-   <span data-ttu-id="09b48-112">Directiva de Access Control efectiva: un descriptor de seguridad de Windows que contiene una DACL que define la Directiva de autorización efectiva.</span><span class="sxs-lookup"><span data-stu-id="09b48-112">Effective Access Control Policy – a Windows security descriptor containing a DACL that defines the effective authorization policy.</span></span>
-   <span data-ttu-id="09b48-113">Expresión de excepción: una o más expresiones que proporcionan un medio para invalidar la Directiva y conceder acceso a una entidad de seguridad de acuerdo con la evaluación de la expresión.</span><span class="sxs-lookup"><span data-stu-id="09b48-113">Exception Expression – one or more expressions that provide a means to override the policy and grant access to a principal according to the evaluation of the expression.</span></span>
-   <span data-ttu-id="09b48-114">Directiva de almacenamiento provisional: un descriptor de seguridad de Windows opcional que contiene una DACL que define una directiva de autorización propuesta (lista de entradas de control de acceso) que se probará con la Directiva vigente, pero no se aplicará.</span><span class="sxs-lookup"><span data-stu-id="09b48-114">Staging Policy – an optional Windows security descriptor containing a DACL that defines a proposed authorization policy (list of access control entries) that will be tested against the effective policy but not enforced.</span></span> <span data-ttu-id="09b48-115">Si hay una diferencia entre los resultados de la Directiva efectiva y la Directiva de almacenamiento provisional, la diferencia se registrará en el registro de eventos de auditoría.</span><span class="sxs-lookup"><span data-stu-id="09b48-115">If there is a difference between the results of the effective policy and the staging policy the difference will be recorded in the audit event log.</span></span>
    -   <span data-ttu-id="09b48-116">Dado que el almacenamiento provisional puede tener un efecto imprevisible en el rendimiento del sistema, un administrador de directiva de grupo debe ser capaz de seleccionar equipos específicos en los que se aplicará el almacenamiento provisional.</span><span class="sxs-lookup"><span data-stu-id="09b48-116">Since staging can have an unpredictable effect on system performance, a Group Policy administrator must be able to select specific machines on which staging will be in effect.</span></span> <span data-ttu-id="09b48-117">Esto permite que la directiva existente esté en su lugar en la mayoría de los equipos de una unidad organizativa mientras se está realizando el almacenamiento provisional en un subconjunto de los equipos.</span><span class="sxs-lookup"><span data-stu-id="09b48-117">This allows the existing policy to be in place on most machines in an OU while staging is happening on a subset of the machines.</span></span>
    -   <span data-ttu-id="09b48-118">P2: un administrador local en un equipo determinado debe poder deshabilitar el almacenamiento provisional si el almacenamiento provisional en dicho equipo está causando una degradación del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="09b48-118">P2 – A local administrator on a particular machine should be able to disable staging if staging on that machine is causing too much of a performance degradation.</span></span>
-   <span data-ttu-id="09b48-119">Backlink to CAP: una lista de vínculos a cualquier Cap que puedan hacer referencia a este CAPR.</span><span class="sxs-lookup"><span data-stu-id="09b48-119">Backlink to CAP – A list of backlinks to any CAPs that may be referring to this CAPR.</span></span>

<span data-ttu-id="09b48-120">Durante la comprobación de acceso, se evalúa la aplicabilidad de CAPR en función de la expresión de aplicabilidad.</span><span class="sxs-lookup"><span data-stu-id="09b48-120">During access check, the CAPR is be evaluated for applicability based on the applicability expression.</span></span> <span data-ttu-id="09b48-121">Si un CAPR es aplicable, se evalúa para determinar si proporciona al usuario solicitante el acceso solicitado al recurso identificado.</span><span class="sxs-lookup"><span data-stu-id="09b48-121">If a CAPR is applicable, it is evaluated for whether it provides the requesting user the requested access to the identified resource.</span></span> <span data-ttu-id="09b48-122">Después, los resultados de la evaluación de cabo se unen lógicamente por **y** con los resultados de la DACL en el recurso y cualquier otro CAPRs aplicable en el recurso.</span><span class="sxs-lookup"><span data-stu-id="09b48-122">The results of the CAPE evaluation is then logically joined by **AND** with the results of the DACL on the resource and any other applicable CAPRs in effect on the resource.</span></span>

<span data-ttu-id="09b48-123">CAPRs de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="09b48-123">Example CAPRs:</span></span>

``` syntax
[HBI-POLICY]
APPLIES-TO="(@resource.confidentiality == HBI"
SD ="D:(A;;FA;;;AU;(@memberOf("Smartcard Logon")))"
StagingSD = "D:(A;;FA;;;AU;(@memberOf("Smartcard Logon") AND memberOfAny(Resource.ProjectGroups)))"
description="Control access to sensitive information"
 
[RETENTION-POLICY]
Applies-To="@resource.retention == true"
SD ="D:(A;;;FA;;BA)(A;;FR;;;WD)"
description="If the document is marked for retention, then it is read-only for everyone however Local Admins have 
full control to them to put them out of retention when the time comes"
 
[TEST-FINANCE-POLICY]
Applies-To="@resource.label == 'finance'"
SD="D:(A;;FA;;;AU;(member_of(FinanceGroup))"
description="Department: Only employees of the finance department should be able to read documents labeled as finance"
```

## <a name="deny-aces-in-capes"></a><span data-ttu-id="09b48-124">Denegar ACE en CAPEs</span><span class="sxs-lookup"><span data-stu-id="09b48-124">Deny ACEs in CAPEs</span></span>

<span data-ttu-id="09b48-125">En Windows 8, las ACE de denegación no se admitirán en CAPR.</span><span class="sxs-lookup"><span data-stu-id="09b48-125">In Windows 8 deny ACEs will not be supported in a CAPR.</span></span> <span data-ttu-id="09b48-126">La experiencia de usuario de creación de CAPR no permitirá la creación de una ACE de denegación.</span><span class="sxs-lookup"><span data-stu-id="09b48-126">The CAPR authoring UX will not allow creation of a deny ACE.</span></span> <span data-ttu-id="09b48-127">Además, cuando LSA recupera el CAP de Active Directory, LSA comprobará que ningún CAPRs tenga ACE de denegación.</span><span class="sxs-lookup"><span data-stu-id="09b48-127">Additionally, when the LSA retrieves the CAP from Active Directory, LSA will verify that no CAPRs have deny ACEs.</span></span> <span data-ttu-id="09b48-128">Si se encuentra una ACE deny en un CAPR, el extremo se tratará como no válido y no se copiará en el registro o en SRM.</span><span class="sxs-lookup"><span data-stu-id="09b48-128">If a deny ACE is found in a CAPR then the CAP will be treated as invalid and not be copied to the registry or SRM.</span></span>

> [!Note]  
> <span data-ttu-id="09b48-129">La comprobación de acceso no exigirá que haya ninguna ACE de denegación presente.</span><span class="sxs-lookup"><span data-stu-id="09b48-129">The access check will not enforce that no deny ACEs are present.</span></span> <span data-ttu-id="09b48-130">Se aplicarán las ACE de denegación en un CAPR.</span><span class="sxs-lookup"><span data-stu-id="09b48-130">Deny ACEs in a CAPR will be applied.</span></span> <span data-ttu-id="09b48-131">Se espera que las herramientas de creación impidan que esto suceda.</span><span class="sxs-lookup"><span data-stu-id="09b48-131">It is expected that authoring tools will prevent this from happening.</span></span>

 

## <a name="cape-definition"></a><span data-ttu-id="09b48-132">Definición de cabo</span><span class="sxs-lookup"><span data-stu-id="09b48-132">CAPE Definition</span></span>

<span data-ttu-id="09b48-133">CAPRs se crean mediante una nueva experiencia de usuario que se proporciona en Centro de administración de Active Directory (ADAC). En ADAC, se proporciona una nueva opción de tarea para crear un CAPR.</span><span class="sxs-lookup"><span data-stu-id="09b48-133">CAPRs are created though a new UX provided in Active Directory Administrative Center (ADAC.) In ADAC a new task option is provided to create a CAPR.</span></span> <span data-ttu-id="09b48-134">Cuando se selecciona esta tarea, ADAC solicitará al usuario un cuadro de diálogo que pide al usuario un nombre de CAPR y una descripción.</span><span class="sxs-lookup"><span data-stu-id="09b48-134">When this task is selected, ADAC will prompt the user with a dialog asking the user for a CAPR name and a description.</span></span> <span data-ttu-id="09b48-135">Cuando se proporcionan, se habilitan los controles para definir cualquiera de los elementos CAPR restantes.</span><span class="sxs-lookup"><span data-stu-id="09b48-135">When these are provided, the controls to define any of the remaining CAPR elements become enabled.</span></span> <span data-ttu-id="09b48-136">Para cada uno de los elementos CAPR restantes, el UX llamará a la interfaz de usuario de ACL para permitir la definición de expresiones y/o ACL.</span><span class="sxs-lookup"><span data-stu-id="09b48-136">For each of the remaining CAPR elements, the UX will call out to the ACL-UI to allow definition of expression and/or ACLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09b48-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09b48-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09b48-138">**AccessCheck**</span><span class="sxs-lookup"><span data-stu-id="09b48-138">**AccessCheck**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[<span data-ttu-id="09b48-139">Escenario de Access Control dinámico (DAC)</span><span class="sxs-lookup"><span data-stu-id="09b48-139">Dynamic Access Control (DAC) scenario</span></span>](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 
