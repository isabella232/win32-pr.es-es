---
description: Cuando se utiliza la seguridad basada en roles, el objeto de contexto de llamada de seguridad se puede utilizar para tener acceso a la información de seguridad sobre la llamada actual.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Obtener acceso a la información de contexto de llamada de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275028"
---
# <a name="accessing-security-call-context-information"></a><span data-ttu-id="4ed54-103">Obtener acceso a la información de contexto de llamada de seguridad</span><span class="sxs-lookup"><span data-stu-id="4ed54-103">Accessing Security Call Context Information</span></span>

<span data-ttu-id="4ed54-104">Cuando se utiliza la seguridad basada en roles, el objeto de contexto de llamada de seguridad se puede utilizar para tener acceso a la información de seguridad sobre la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="4ed54-104">When role-based security is being used, the security call context object can be used to access security information about the current call.</span></span>

<span data-ttu-id="4ed54-105">Las siguientes colecciones de propiedades están disponibles en el objeto de contexto de llamada de seguridad:</span><span class="sxs-lookup"><span data-stu-id="4ed54-105">The following collections of properties are available from the security call context object:</span></span>

-   [<span data-ttu-id="4ed54-106">SecurityCallContext (colección)</span><span class="sxs-lookup"><span data-stu-id="4ed54-106">SecurityCallContext Collection</span></span>](#securitycallcontext-collection)
-   [<span data-ttu-id="4ed54-107">Colección SecurityCallers</span><span class="sxs-lookup"><span data-stu-id="4ed54-107">SecurityCallers Collection</span></span>](#securitycallers-collection)
-   [<span data-ttu-id="4ed54-108">SecurityIdentity (colección)</span><span class="sxs-lookup"><span data-stu-id="4ed54-108">SecurityIdentity Collection</span></span>](#securityidentity-collection)
-   [<span data-ttu-id="4ed54-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4ed54-109">Related topics</span></span>](#related-topics)

## <a name="securitycallcontext-collection"></a><span data-ttu-id="4ed54-110">SecurityCallContext (colección)</span><span class="sxs-lookup"><span data-stu-id="4ed54-110">SecurityCallContext Collection</span></span>



| <span data-ttu-id="4ed54-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4ed54-111">Property</span></span>                          | <span data-ttu-id="4ed54-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ed54-112">Description</span></span>                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed54-113">NumCallers</span><span class="sxs-lookup"><span data-stu-id="4ed54-113">NumCallers</span></span><br/>             | <span data-ttu-id="4ed54-114">Número de llamadores de la cadena de llamadas.</span><span class="sxs-lookup"><span data-stu-id="4ed54-114">The number of callers in the chain of calls.</span></span><br/>                                                                                |
| <span data-ttu-id="4ed54-115">MinAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="4ed54-115">MinAuthenticationLevel</span></span><br/> | <span data-ttu-id="4ed54-116">Nivel de autenticación menos seguro de todos los llamadores de la cadena.</span><span class="sxs-lookup"><span data-stu-id="4ed54-116">The least secure authentication level of all callers in the chain.</span></span><br/>                                                          |
| <span data-ttu-id="4ed54-117">Los llamadores</span><span class="sxs-lookup"><span data-stu-id="4ed54-117">Callers</span></span><br/>                | <span data-ttu-id="4ed54-118">Información sobre la identidad de los llamadores de nivel superior, en forma de una colección [**SecurityCallers**](securitycallers.md) .</span><span class="sxs-lookup"><span data-stu-id="4ed54-118">Information about the identity of upstream callers, in the form of a [**SecurityCallers**](securitycallers.md) collection.</span></span><br/> |
| <span data-ttu-id="4ed54-119">DirectCaller</span><span class="sxs-lookup"><span data-stu-id="4ed54-119">DirectCaller</span></span><br/>           | <span data-ttu-id="4ed54-120">Llamador que llamó directamente al objeto (sin ningún llamador que intervenga).</span><span class="sxs-lookup"><span data-stu-id="4ed54-120">The caller that called the object directly (with no intervening callers).</span></span> <br/>                                                  |
| <span data-ttu-id="4ed54-121">OriginalCaller</span><span class="sxs-lookup"><span data-stu-id="4ed54-121">OriginalCaller</span></span><br/>         | <span data-ttu-id="4ed54-122">Llamador que originó la cadena de llamadas al objeto.</span><span class="sxs-lookup"><span data-stu-id="4ed54-122">The caller that originated the chain of calls to the object.</span></span> <br/>                                                               |



 

<span data-ttu-id="4ed54-123">Para obtener más información sobre cómo usar esta colección, los desarrolladores de Microsoft Visual Basic deben ver la clase [**SecurityCallContext**](securitycallcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="4ed54-123">For more information about how to use this collection, Microsoft Visual Basic developers should see the [**SecurityCallContext**](securitycallcontext.md) class.</span></span> <span data-ttu-id="4ed54-124">Los desarrolladores de C y C++ deben hacer referencia a [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="4ed54-124">C and C++ developers should refer to [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="securitycallers-collection"></a><span data-ttu-id="4ed54-125">Colección SecurityCallers</span><span class="sxs-lookup"><span data-stu-id="4ed54-125">SecurityCallers Collection</span></span>

<span data-ttu-id="4ed54-126">La colección [**SecurityCallers**](securitycallers.md) representa a los llamadores que se pueden recuperar mediante un índice entre 0 y 1 menor que NumCallers, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="4ed54-126">The [**SecurityCallers**](securitycallers.md) collection represents callers that can be retrieved by using an index between 0 and 1 less than NumCallers, inclusive.</span></span> <span data-ttu-id="4ed54-127">Cada llamador se representa mediante un objeto [**SecurityIdentity**](securityidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="4ed54-127">Each caller is represented by a [**SecurityIdentity**](securityidentity.md) object.</span></span>

<span data-ttu-id="4ed54-128">Para obtener más información sobre esta colección, los desarrolladores de Visual Basic deberían ver la clase [**SecurityCallers**](securitycallers.md) .</span><span class="sxs-lookup"><span data-stu-id="4ed54-128">For more information about this collection, Visual Basic developers should see the [**SecurityCallers**](securitycallers.md) class.</span></span> <span data-ttu-id="4ed54-129">Los desarrolladores de C y C++ deben hacer referencia a [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span><span class="sxs-lookup"><span data-stu-id="4ed54-129">C and C++ developers should refer to [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="securityidentity-collection"></a><span data-ttu-id="4ed54-130">SecurityIdentity (colección)</span><span class="sxs-lookup"><span data-stu-id="4ed54-130">SecurityIdentity Collection</span></span>



| <span data-ttu-id="4ed54-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4ed54-131">Property</span></span>                         | <span data-ttu-id="4ed54-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ed54-132">Description</span></span>                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed54-133">SID</span><span class="sxs-lookup"><span data-stu-id="4ed54-133">SID</span></span><br/>                   | <span data-ttu-id="4ed54-134">El identificador de seguridad para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="4ed54-134">The security identifier for the caller.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="4ed54-135">AccountName</span><span class="sxs-lookup"><span data-stu-id="4ed54-135">AccountName</span></span><br/>           | <span data-ttu-id="4ed54-136">Nombre de cuenta del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="4ed54-136">The account name of the caller.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="4ed54-137">AuthenticationService</span><span class="sxs-lookup"><span data-stu-id="4ed54-137">AuthenticationService</span></span><br/> | <span data-ttu-id="4ed54-138">Servicio de autenticación usado, como NTLMSSP, Kerberos o SSL.</span><span class="sxs-lookup"><span data-stu-id="4ed54-138">The authentication service used, such as NTLMSSP, Kerberos, or SSL.</span></span><br/>                                                                                       |
| <span data-ttu-id="4ed54-139">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="4ed54-139">AuthenticationLevel</span></span><br/>   | <span data-ttu-id="4ed54-140">El nivel de autenticación utilizado, que representa la cantidad de protección utilizada al comunicarse con el objeto.</span><span class="sxs-lookup"><span data-stu-id="4ed54-140">The authentication level used, which represents the amount of protection used when communicating with the object.</span></span><br/>                                         |
| <span data-ttu-id="4ed54-141">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="4ed54-141">ImpersonationLevel</span></span><br/>    | <span data-ttu-id="4ed54-142">Nivel de suplantación establecido por el cliente, si se ha utilizado la suplantación.</span><span class="sxs-lookup"><span data-stu-id="4ed54-142">The level of impersonation set by the client, if impersonation was used.</span></span> <span data-ttu-id="4ed54-143">Este nivel indica la cantidad de autoridad proporcionada al servidor por el cliente.</span><span class="sxs-lookup"><span data-stu-id="4ed54-143">This level indicates the amount of authority given to the server by the client.</span></span> <br/> |



 

<span data-ttu-id="4ed54-144">Para obtener más información sobre esta colección, los desarrolladores de Visual Basic deberían ver la clase [**SecurityIdentity**](securityidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="4ed54-144">For more information on this collection, Visual Basic developers should see the [**SecurityIdentity**](securityidentity.md) class.</span></span> <span data-ttu-id="4ed54-145">Los desarrolladores de C y C++ deben hacer referencia a [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span><span class="sxs-lookup"><span data-stu-id="4ed54-145">C and C++ developers should refer to [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ed54-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4ed54-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ed54-147">Comprobando la pertenencia al rol</span><span class="sxs-lookup"><span data-stu-id="4ed54-147">Checking Role Membership</span></span>](checking-role-membership.md)
</dt> <dt>

[<span data-ttu-id="4ed54-148">Determinar si está habilitada la seguridad de Role-Based</span><span class="sxs-lookup"><span data-stu-id="4ed54-148">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[<span data-ttu-id="4ed54-149">Seguridad de componentes mediante programación</span><span class="sxs-lookup"><span data-stu-id="4ed54-149">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 




