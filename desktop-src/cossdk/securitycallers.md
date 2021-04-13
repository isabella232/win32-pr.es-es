---
description: Proporciona acceso a información sobre los llamadores individuales de una colección de llamadores. La colección representa la cadena de llamadas que finalizan con la llamada actual y cada llamador de la colección representa la identidad de un llamador.
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: Clase SecurityCallers (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: c757b11bba6a30e8951915e1eace0811b6b6f732
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360037"
---
# <a name="securitycallers-class"></a><span data-ttu-id="30f7f-104">SecurityCallers (clase)</span><span class="sxs-lookup"><span data-stu-id="30f7f-104">SecurityCallers class</span></span>

<span data-ttu-id="30f7f-105">Proporciona acceso a información sobre los llamadores individuales de una colección de llamadores.</span><span class="sxs-lookup"><span data-stu-id="30f7f-105">Provides access to information about individual callers in a collection of callers.</span></span> <span data-ttu-id="30f7f-106">La colección representa la cadena de llamadas que finalizan con la llamada actual y cada llamador de la colección representa la identidad de un llamador.</span><span class="sxs-lookup"><span data-stu-id="30f7f-106">The collection represents the chain of calls ending with the current call, and each caller in the collection represents the identity of one caller.</span></span> <span data-ttu-id="30f7f-107">Solo los llamadores que cruzan un límite en el que se comprueba la seguridad se incluyen en la cadena de llamadores.</span><span class="sxs-lookup"><span data-stu-id="30f7f-107">Only callers who cross a boundary where security is checked are included in the chain of callers.</span></span> <span data-ttu-id="30f7f-108">(En el entorno de COM+, se comprueba la seguridad en los límites de la aplicación). El acceso a la información sobre la identidad de un llamador determinado se proporciona a través de la clase [**SecurityIdentity**](securityidentity.md) , una colección de identidades.</span><span class="sxs-lookup"><span data-stu-id="30f7f-108">(In the COM+ environment, security is checked at application boundaries.) Access to information about a particular caller's identity is provided through the [**SecurityIdentity**](securityidentity.md) class, an identity collection.</span></span>

<span data-ttu-id="30f7f-109">Solo las aplicaciones COM+ que utilizan la seguridad basada en roles pueden tener acceso a la clase **SecurityCallers** .</span><span class="sxs-lookup"><span data-stu-id="30f7f-109">Only COM+ applications that use role-based security can access the **SecurityCallers** class.</span></span> <span data-ttu-id="30f7f-110">Para obtener más información sobre los roles, consulte [Administración de la seguridad basada en roles](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="30f7f-110">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="30f7f-111">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="30f7f-111">When to implement</span></span>

<span data-ttu-id="30f7f-112">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="30f7f-112">This class is implemented by COM+.</span></span>



| <span data-ttu-id="30f7f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="30f7f-113">Requirement</span></span> | <span data-ttu-id="30f7f-114">Value</span><span class="sxs-lookup"><span data-stu-id="30f7f-114">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="30f7f-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="30f7f-115">Interfaces</span></span> | [<span data-ttu-id="30f7f-116">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="30f7f-116">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="30f7f-117">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="30f7f-117">When to use</span></span>

<span data-ttu-id="30f7f-118">Utilice esta clase para tener acceso a los métodos de [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span><span class="sxs-lookup"><span data-stu-id="30f7f-118">Use this class to access the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="30f7f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30f7f-119">Remarks</span></span>

<span data-ttu-id="30f7f-120">No se puede crear directamente un objeto **SecurityCallers** .</span><span class="sxs-lookup"><span data-stu-id="30f7f-120">You cannot directly create a **SecurityCallers** object.</span></span> <span data-ttu-id="30f7f-121">Para utilizar los métodos de [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), debe obtener una referencia a su implementación mediante una llamada a [**COGETCALLCONTEXT**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), proporcionando IID \_ ISecurityCallContext para el parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="30f7f-121">To use the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="30f7f-122">Después, llame a [**ISecurityCallContext:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) solicitando un elemento de contexto de llamada de seguridad que sea una colección de identidades de seguridad (como "DirectCaller" o "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="30f7f-122">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

<span data-ttu-id="30f7f-123">Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="30f7f-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="30f7f-124">No se puede crear directamente un objeto SecurityCallers.</span><span class="sxs-lookup"><span data-stu-id="30f7f-124">You cannot directly create a SecurityCallers object.</span></span> <span data-ttu-id="30f7f-125">Para usar sus propiedades, debe obtener específica a su implementación mediante [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="30f7f-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="30f7f-126">A continuación, obtenga la propiedad Item del objeto, solicitando un elemento de contexto de llamada de seguridad que sea una colección de identidades de seguridad (como "DirectCaller" o "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="30f7f-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

## <a name="requirements"></a><span data-ttu-id="30f7f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30f7f-127">Requirements</span></span>



| <span data-ttu-id="30f7f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="30f7f-128">Requirement</span></span> | <span data-ttu-id="30f7f-129">Value</span><span class="sxs-lookup"><span data-stu-id="30f7f-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="30f7f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30f7f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="30f7f-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="30f7f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="30f7f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30f7f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="30f7f-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="30f7f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="30f7f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30f7f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="30f7f-135"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="30f7f-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30f7f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="30f7f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f7f-137">**GetSecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="30f7f-137">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="30f7f-138">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="30f7f-138">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="30f7f-139">Seguridad de componentes mediante programación</span><span class="sxs-lookup"><span data-stu-id="30f7f-139">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="30f7f-140">Administración de la seguridad basada en roles</span><span class="sxs-lookup"><span data-stu-id="30f7f-140">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="30f7f-141">**SecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="30f7f-141">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="30f7f-142">**SecurityIdentity**</span><span class="sxs-lookup"><span data-stu-id="30f7f-142">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

