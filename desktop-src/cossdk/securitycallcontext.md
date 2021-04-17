---
description: Proporciona acceso al contexto de seguridad de la llamada actual, que contiene información sobre los llamadores de un objeto.
ms.assetid: e8ac05fb-6665-4e57-b64e-82d9799d29d4
title: SecurityCallContext (clase) (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallContext
api_type:
- COM
ms.openlocfilehash: bd15b7e0317a507a2340cc148bb927bb5d94a37b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717433"
---
# <a name="securitycallcontext-class"></a><span data-ttu-id="46499-103">SecurityCallContext (clase)</span><span class="sxs-lookup"><span data-stu-id="46499-103">SecurityCallContext class</span></span>

<span data-ttu-id="46499-104">Proporciona acceso al contexto de seguridad de la llamada actual, que contiene información sobre los llamadores de un objeto.</span><span class="sxs-lookup"><span data-stu-id="46499-104">Provides access to the current call's security context, which contains information about an object's callers.</span></span> <span data-ttu-id="46499-105">Con esta clase, también puede averiguar si el llamador directo de un objeto es miembro de un rol determinado y si la seguridad está habilitada para el objeto.</span><span class="sxs-lookup"><span data-stu-id="46499-105">Using this class, you can also find out whether an object's direct caller is a member of a particular role and whether security is enabled for the object.</span></span>

<span data-ttu-id="46499-106">Solo las aplicaciones COM+ que utilizan la seguridad basada en roles pueden tener acceso a la clase **SecurityCallContext** .</span><span class="sxs-lookup"><span data-stu-id="46499-106">Only COM+ applications that use role-based security can access the **SecurityCallContext** class.</span></span> <span data-ttu-id="46499-107">Para obtener más información sobre los roles, consulte [Administración de la seguridad basada en roles](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="46499-107">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="46499-108">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="46499-108">When to implement</span></span>

<span data-ttu-id="46499-109">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="46499-109">This class is implemented by COM+.</span></span>



| <span data-ttu-id="46499-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="46499-110">Requirement</span></span> | <span data-ttu-id="46499-111">Value</span><span class="sxs-lookup"><span data-stu-id="46499-111">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="46499-112">Interfaces</span><span class="sxs-lookup"><span data-stu-id="46499-112">Interfaces</span></span> | [<span data-ttu-id="46499-113">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="46499-113">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="46499-114">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="46499-114">When to use</span></span>

<span data-ttu-id="46499-115">Utilice esta clase para tener acceso a los métodos de [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="46499-115">Use this class to access the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="remarks"></a><span data-ttu-id="46499-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46499-116">Remarks</span></span>

<span data-ttu-id="46499-117">No se puede crear directamente un objeto **SecurityCallContext** .</span><span class="sxs-lookup"><span data-stu-id="46499-117">You cannot directly create a **SecurityCallContext** object.</span></span> <span data-ttu-id="46499-118">Para utilizar los métodos de [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), debe obtener una referencia a su implementación llamando a [**COGETCALLCONTEXT**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), proporcionando IID \_ ISecurityCallContext para el parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="46499-118">To use the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span>

<span data-ttu-id="46499-119">Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="46499-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="46499-120">Un objeto SecurityCallContext puede declararse con "COMSVCSLib. SecurityCallContext" como nombre de clase; se crea llamando a [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="46499-120">A SecurityCallContext object can be declared using "COMSVCSLib.SecurityCallContext" as the class name; it is created by calling [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="46499-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46499-121">Requirements</span></span>



| <span data-ttu-id="46499-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="46499-122">Requirement</span></span> | <span data-ttu-id="46499-123">Value</span><span class="sxs-lookup"><span data-stu-id="46499-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="46499-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46499-124">Minimum supported client</span></span><br/> | <span data-ttu-id="46499-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="46499-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="46499-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46499-126">Minimum supported server</span></span><br/> | <span data-ttu-id="46499-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="46499-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="46499-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46499-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="46499-129"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="46499-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46499-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="46499-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46499-131">**GetSecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="46499-131">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="46499-132">**ISecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="46499-132">**ISecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="46499-133">Seguridad de componentes mediante programación</span><span class="sxs-lookup"><span data-stu-id="46499-133">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="46499-134">Administración de la seguridad basada en roles</span><span class="sxs-lookup"><span data-stu-id="46499-134">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="46499-135">**SecurityCallers**</span><span class="sxs-lookup"><span data-stu-id="46499-135">**SecurityCallers**</span></span>](securitycallers.md)
</dt> <dt>

[<span data-ttu-id="46499-136">**SecurityIdentity**</span><span class="sxs-lookup"><span data-stu-id="46499-136">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

