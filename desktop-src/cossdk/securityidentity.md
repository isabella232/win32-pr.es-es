---
description: Proporciona acceso a una colección de información de seguridad que representa la identidad de un llamador. Con esta clase, puede encontrar información sobre un llamador determinado en una cadena de llamadores que forma parte del contexto de la llamada de seguridad.
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: SecurityIdentity (clase) (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: 6775c06bc25bfb32a1c2c247868fd2a9fbc9aade
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103820431"
---
# <a name="securityidentity-class"></a><span data-ttu-id="2ae88-104">SecurityIdentity (clase)</span><span class="sxs-lookup"><span data-stu-id="2ae88-104">SecurityIdentity class</span></span>

<span data-ttu-id="2ae88-105">Proporciona acceso a una colección de información de seguridad que representa la identidad de un llamador.</span><span class="sxs-lookup"><span data-stu-id="2ae88-105">Provides access to a collection of security information representing a caller's identity.</span></span> <span data-ttu-id="2ae88-106">Con esta clase, puede encontrar información sobre un llamador determinado en una cadena de llamadores que forma parte del contexto de la llamada de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2ae88-106">Using this class, you can find out about a particular caller in a chain of callers that is part of the security call context.</span></span> <span data-ttu-id="2ae88-107">Para obtener más información sobre cómo se obtiene acceso a la información de contexto de llamadas de seguridad, vea seguridad de componentes de programación.</span><span class="sxs-lookup"><span data-stu-id="2ae88-107">For more information about how security call context information is accessed, see Programmatic Component Security.</span></span>

<span data-ttu-id="2ae88-108">Solo las aplicaciones COM+ que utilizan la seguridad basada en roles pueden tener acceso a la clase **SecurityIdentity** .</span><span class="sxs-lookup"><span data-stu-id="2ae88-108">Only COM+ applications that use role-based security can access the **SecurityIdentity** class.</span></span> <span data-ttu-id="2ae88-109">Para obtener más información sobre los roles, consulte [Administración de la seguridad basada en roles](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="2ae88-109">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="2ae88-110">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="2ae88-110">When to implement</span></span>

<span data-ttu-id="2ae88-111">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="2ae88-111">This class is implemented by COM+.</span></span>



| <span data-ttu-id="2ae88-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ae88-112">Requirement</span></span> | <span data-ttu-id="2ae88-113">Value</span><span class="sxs-lookup"><span data-stu-id="2ae88-113">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="2ae88-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="2ae88-114">Interfaces</span></span> | [<span data-ttu-id="2ae88-115">**ISecurityIdentityColl**</span><span class="sxs-lookup"><span data-stu-id="2ae88-115">**ISecurityIdentityColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="2ae88-116">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="2ae88-116">When to use</span></span>

<span data-ttu-id="2ae88-117">Utilice esta clase para tener acceso a los métodos de [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span><span class="sxs-lookup"><span data-stu-id="2ae88-117">Use this class to access the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="2ae88-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ae88-118">Remarks</span></span>

<span data-ttu-id="2ae88-119">No se puede crear directamente un objeto **SecurityIdentity** .</span><span class="sxs-lookup"><span data-stu-id="2ae88-119">You cannot directly create a **SecurityIdentity** object.</span></span> <span data-ttu-id="2ae88-120">Para utilizar los métodos de [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), debe obtener una referencia a su implementación mediante una llamada a [**COGETCALLCONTEXT**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), proporcionando IID \_ ISecurityCallContext para el parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="2ae88-120">To use the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="2ae88-121">Después, llame a [**ISecurityCallContext:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) solicitando un elemento de contexto de llamada de seguridad que sea una colección de identidades de seguridad (como "DirectCaller" o "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="2ae88-121">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="2ae88-122">Después, llame a [**ISecurityIdentityColl:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) para recuperar un elemento de identidad de seguridad (por ejemplo, "Name" o "AuthenticationService").</span><span class="sxs-lookup"><span data-stu-id="2ae88-122">Then call [**ISecurityIdentityColl::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

<span data-ttu-id="2ae88-123">Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="2ae88-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="2ae88-124">No se puede crear directamente un objeto SecurityIdentity.</span><span class="sxs-lookup"><span data-stu-id="2ae88-124">You cannot directly create a SecurityIdentity object.</span></span> <span data-ttu-id="2ae88-125">Para usar sus propiedades, debe obtener específica a su implementación mediante [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="2ae88-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="2ae88-126">A continuación, obtenga la propiedad Item del objeto, solicitando un elemento de contexto de llamada de seguridad que sea una colección de identidades de seguridad (como "DirectCaller" o "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="2ae88-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="2ae88-127">A continuación, use la propiedad Item del objeto SecurityIdentity para recuperar un elemento de identidad de seguridad (por ejemplo, "Name" o "AuthenticationService").</span><span class="sxs-lookup"><span data-stu-id="2ae88-127">Then, use the Item property of the SecurityIdentity object to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

## <a name="requirements"></a><span data-ttu-id="2ae88-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ae88-128">Requirements</span></span>



| <span data-ttu-id="2ae88-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ae88-129">Requirement</span></span> | <span data-ttu-id="2ae88-130">Value</span><span class="sxs-lookup"><span data-stu-id="2ae88-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae88-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ae88-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2ae88-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2ae88-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2ae88-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ae88-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2ae88-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ae88-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2ae88-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ae88-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ae88-136"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ae88-136"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ae88-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ae88-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae88-138">**GetSecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="2ae88-138">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="2ae88-139">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="2ae88-139">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="2ae88-140">Seguridad de componentes mediante programación</span><span class="sxs-lookup"><span data-stu-id="2ae88-140">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="2ae88-141">Administración de la seguridad basada en roles</span><span class="sxs-lookup"><span data-stu-id="2ae88-141">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="2ae88-142">**SecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="2ae88-142">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="2ae88-143">**SecurityCallers**</span><span class="sxs-lookup"><span data-stu-id="2ae88-143">**SecurityCallers**</span></span>](securitycallers.md)
</dt> </dl>

 

