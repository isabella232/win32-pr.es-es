---
description: Deshabilita una GPU física para la virtualización.
ms.assetid: 280a3c25-7b8f-4113-bf35-171d15f4aea7
title: Método DisableGPUForVirtualization de la clase Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.DisableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2634a3196e0c59368002151426e6f1407a13db8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360126"
---
# <a name="disablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a><span data-ttu-id="15928-103">Método DisableGPUForVirtualization de la \_ clase Synthetic3DService de MSVM</span><span class="sxs-lookup"><span data-stu-id="15928-103">DisableGPUForVirtualization method of the Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="15928-104">Deshabilita una GPU física para la virtualización.</span><span class="sxs-lookup"><span data-stu-id="15928-104">Disables a physical GPU for virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="15928-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15928-105">Syntax</span></span>


```mof
uint32 DisableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="15928-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15928-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15928-107">*PhysicalGPU* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="15928-107">*PhysicalGPU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15928-108">Referencia a una instancia de la clase [**MSVM \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) que representa la GPU física que se va a deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="15928-108">A reference to an instance of the [**Msvm\_Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) class that represents the physical GPU to be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="15928-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="15928-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15928-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="15928-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15928-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15928-111">Return value</span></span>

<span data-ttu-id="15928-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="15928-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="15928-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="15928-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="15928-114">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="15928-114">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="15928-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15928-115">Requirements</span></span>



| <span data-ttu-id="15928-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="15928-116">Requirement</span></span> | <span data-ttu-id="15928-117">Value</span><span class="sxs-lookup"><span data-stu-id="15928-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15928-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15928-118">Minimum supported client</span></span><br/> | <span data-ttu-id="15928-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="15928-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="15928-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15928-120">Minimum supported server</span></span><br/> | <span data-ttu-id="15928-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="15928-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15928-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="15928-122">Namespace</span></span><br/>                | <span data-ttu-id="15928-123">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="15928-123">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="15928-124">MOF</span><span class="sxs-lookup"><span data-stu-id="15928-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15928-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15928-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15928-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15928-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15928-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15928-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15928-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="15928-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15928-129">**MSVM \_ Synthetic3DService**</span><span class="sxs-lookup"><span data-stu-id="15928-129">**Msvm\_Synthetic3DService**</span></span>](msvm-synthetic3dservice.md)
</dt> </dl>

 

