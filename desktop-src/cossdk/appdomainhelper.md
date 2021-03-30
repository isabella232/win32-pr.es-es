---
description: Enlaza un objeto administrado a un dominio de aplicación, que es un entorno aislado donde se ejecutan las aplicaciones.
ms.assetid: 9357ea5d-6f86-4747-a923-16575ff13122
title: Clase AppDomainHelper (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AppDomainHelper
api_type:
- COM
ms.openlocfilehash: 6b4fbedbca631ec49dc2e416d939abdeb239e5b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538734"
---
# <a name="appdomainhelper-class"></a><span data-ttu-id="9b44e-103">Clase AppDomainHelper</span><span class="sxs-lookup"><span data-stu-id="9b44e-103">AppDomainHelper class</span></span>

<span data-ttu-id="9b44e-104">Enlaza un objeto administrado a un dominio de aplicación, que es un entorno aislado donde se ejecutan las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9b44e-104">Binds a managed object to an application domain, which is an isolated environment where applications execute.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="9b44e-105">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="9b44e-105">When to implement</span></span>

<span data-ttu-id="9b44e-106">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="9b44e-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="9b44e-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b44e-107">Requirement</span></span> | <span data-ttu-id="9b44e-108">Value</span><span class="sxs-lookup"><span data-stu-id="9b44e-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="9b44e-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="9b44e-109">CLSID</span></span>      | <span data-ttu-id="9b44e-110">GUID \_ AppDomainHelper</span><span class="sxs-lookup"><span data-stu-id="9b44e-110">GUID\_AppDomainHelper</span></span>                                 |
| <span data-ttu-id="9b44e-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="9b44e-111">ProgID</span></span>     | <span data-ttu-id="9b44e-112">L "System. EnterpriseServices. Internal. AppDomainHelper"</span><span class="sxs-lookup"><span data-stu-id="9b44e-112">L"System.EnterpriseServices.Internal.AppDomainHelper"</span></span> |
| <span data-ttu-id="9b44e-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="9b44e-113">Interfaces</span></span> | [<span data-ttu-id="9b44e-114">**IAppDomainHelper**</span><span class="sxs-lookup"><span data-stu-id="9b44e-114">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)          |



 

## <a name="when-to-use"></a><span data-ttu-id="9b44e-115">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="9b44e-115">When to use</span></span>

<span data-ttu-id="9b44e-116">Utilice esta clase para tener acceso a los métodos de [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).</span><span class="sxs-lookup"><span data-stu-id="9b44e-116">Use this class to access the methods of [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b44e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b44e-117">Remarks</span></span>

<span data-ttu-id="9b44e-118">Para crear este objeto, llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="9b44e-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="9b44e-119">Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="9b44e-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="9b44e-120">Un objeto AppDomainHelper se puede declarar con "COMSVCSLib. AppDomainHelper" como nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="9b44e-120">An AppDomainHelper object can be declared using "COMSVCSLib.AppDomainHelper" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b44e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b44e-121">Requirements</span></span>



| <span data-ttu-id="9b44e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b44e-122">Requirement</span></span> | <span data-ttu-id="9b44e-123">Value</span><span class="sxs-lookup"><span data-stu-id="9b44e-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9b44e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b44e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9b44e-125">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b44e-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9b44e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b44e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9b44e-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b44e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9b44e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b44e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b44e-129"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b44e-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b44e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b44e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b44e-131">**IAppDomainHelper**</span><span class="sxs-lookup"><span data-stu-id="9b44e-131">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

