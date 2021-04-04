---
description: Recupera información acerca de un ensamblado cuando se usa código administrado en el Common Language Runtime de .NET Framework.
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: Clase ClrAssemblyLocator (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: ff5c1d21525a950208c1b919d4dee0e2122d2e50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907105"
---
# <a name="clrassemblylocator-class"></a><span data-ttu-id="c5bfd-103">Clase ClrAssemblyLocator</span><span class="sxs-lookup"><span data-stu-id="c5bfd-103">ClrAssemblyLocator class</span></span>

<span data-ttu-id="c5bfd-104">Recupera información acerca de un ensamblado cuando se usa código administrado en el Common Language Runtime de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c5bfd-104">Retrieves information about an assembly when using managed code in the .NET Framework common language runtime.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="c5bfd-105">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="c5bfd-105">When to implement</span></span>

<span data-ttu-id="c5bfd-106">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="c5bfd-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="c5bfd-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5bfd-107">Requirement</span></span> | <span data-ttu-id="c5bfd-108">Value</span><span class="sxs-lookup"><span data-stu-id="c5bfd-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="c5bfd-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="c5bfd-109">CLSID</span></span>      | <span data-ttu-id="c5bfd-110">GUID \_ AssemblyLocator</span><span class="sxs-lookup"><span data-stu-id="c5bfd-110">GUID\_AssemblyLocator</span></span>                                 |
| <span data-ttu-id="c5bfd-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="c5bfd-111">ProgID</span></span>     | <span data-ttu-id="c5bfd-112">L "System. EnterpriseServices. Internal. AssemblyLocator"</span><span class="sxs-lookup"><span data-stu-id="c5bfd-112">L"System.EnterpriseServices.Internal.AssemblyLocator"</span></span> |
| <span data-ttu-id="c5bfd-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="c5bfd-113">Interfaces</span></span> | [<span data-ttu-id="c5bfd-114">**IAssemblyLocator**</span><span class="sxs-lookup"><span data-stu-id="c5bfd-114">**IAssemblyLocator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a><span data-ttu-id="c5bfd-115">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="c5bfd-115">When to use</span></span>

<span data-ttu-id="c5bfd-116">Utilice esta clase para tener acceso a los métodos de [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).</span><span class="sxs-lookup"><span data-stu-id="c5bfd-116">Use this class to access the methods of [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).</span></span>

## <a name="remarks"></a><span data-ttu-id="c5bfd-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5bfd-117">Remarks</span></span>

<span data-ttu-id="c5bfd-118">Para crear este objeto, llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="c5bfd-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="c5bfd-119">Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="c5bfd-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="c5bfd-120">Un objeto ClrAssemblyLocator se puede declarar con "COMSVCSLib. ClrAssemblyLocator" como nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="c5bfd-120">A ClrAssemblyLocator object can be declared using "COMSVCSLib.ClrAssemblyLocator" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5bfd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5bfd-121">Requirements</span></span>



| <span data-ttu-id="c5bfd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5bfd-122">Requirement</span></span> | <span data-ttu-id="c5bfd-123">Value</span><span class="sxs-lookup"><span data-stu-id="c5bfd-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c5bfd-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5bfd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c5bfd-125">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5bfd-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c5bfd-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5bfd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c5bfd-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5bfd-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c5bfd-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5bfd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5bfd-129"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5bfd-129"><dt>ComSvcs.h</dt></span></span> </dl> |



 

