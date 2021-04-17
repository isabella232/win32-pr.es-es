---
description: Inserta una interrupción no enmascarable en la máquina virtual.
ms.assetid: 897AD1B9-0EDD-4DCE-963D-D5DE03AF55A9
title: 'Msvm_ComputerSystem:: InjectNonMaskableInterrupt (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.InjectNonMaskableInterrupt
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5798079a8866d9fb67356adff43c0ac1e993e6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666337"
---
# <a name="msvm_computersysteminjectnonmaskableinterrupt-method"></a><span data-ttu-id="b2300-103">MSVM \_ ComputerSystem:: InjectNonMaskableInterrupt (método)</span><span class="sxs-lookup"><span data-stu-id="b2300-103">Msvm\_ComputerSystem::InjectNonMaskableInterrupt method</span></span>

<span data-ttu-id="b2300-104">Inserta una interrupción no enmascarable en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b2300-104">Injects a non-maskable interrupt into the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2300-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2300-105">Syntax</span></span>


```C++
uint32 InjectNonMaskableInterrupt(
  [out] CIM_ConcreteJob Job
);
```



## <a name="parameters"></a><span data-ttu-id="b2300-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2300-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2300-107">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b2300-107">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2300-108">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) para realizar un seguimiento del estado de la inserción de interrupción.</span><span class="sxs-lookup"><span data-stu-id="b2300-108">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) to track the status of the interrupt injection.</span></span> <span data-ttu-id="b2300-109">Esta referencia puede ser **null** si la tarea se ha completado.</span><span class="sxs-lookup"><span data-stu-id="b2300-109">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2300-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2300-110">Return value</span></span>

<span data-ttu-id="b2300-111">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b2300-111">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b2300-112">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="b2300-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b2300-113">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b2300-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b2300-114">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="b2300-114">**Access Denied** (32769)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b2300-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2300-115">Requirements</span></span>



| <span data-ttu-id="b2300-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2300-116">Requirement</span></span> | <span data-ttu-id="b2300-117">Value</span><span class="sxs-lookup"><span data-stu-id="b2300-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2300-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2300-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2300-119">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="b2300-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b2300-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2300-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2300-121">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2300-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b2300-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b2300-122">Namespace</span></span><br/>                | <span data-ttu-id="b2300-123">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b2300-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="b2300-124">MOF</span><span class="sxs-lookup"><span data-stu-id="b2300-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2300-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2300-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2300-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2300-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2300-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2300-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2300-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2300-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2300-129">**MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="b2300-129">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

