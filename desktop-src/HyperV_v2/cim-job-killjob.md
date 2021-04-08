---
description: Método para eliminar este trabajo y los procesos subyacentes, y para quitar las asociaciones pendientes. Este método está en desuso; Use RequestChangeState en su lugar.
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: Método KillJob de la clase CIM_Job
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job.KillJob
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 967e5e8510d4456a085f393291f8c41afb5be446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001776"
---
# <a name="killjob-method-of-the-cim_job-class"></a><span data-ttu-id="7392f-104">Método KillJob de la \_ clase de trabajo CIM</span><span class="sxs-lookup"><span data-stu-id="7392f-104">KillJob method of the CIM\_Job class</span></span>

<span data-ttu-id="7392f-105">Un método para eliminar este trabajo y los procesos subyacentes, y para quitar cualquier asociación "pendiente".</span><span class="sxs-lookup"><span data-stu-id="7392f-105">A method to kill this job and any underlying processes, and to remove any 'dangling' associations.</span></span> <span data-ttu-id="7392f-106">Este método está en desuso; Use **RequestChangeState** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7392f-106">This method is deprecated; use **RequestChangeState** instead.</span></span> <span data-ttu-id="7392f-107">**KillJob** está en desuso porque no se realiza ninguna distinción entre un cierre ordenado y una eliminación inmediata.</span><span class="sxs-lookup"><span data-stu-id="7392f-107">**KillJob** is being deprecated because there is no distinction made between an orderly shutdown and an immediate kill.</span></span> <span data-ttu-id="7392f-108">[**CIM \_ ConcreteJob**](cim-concretejob.md). **RequestStateChange**() proporciona las opciones ' Terminate ' y ' Kill ' para permitir esta distinción.</span><span class="sxs-lookup"><span data-stu-id="7392f-108">[**CIM\_ConcreteJob**](cim-concretejob.md).**RequestStateChange**() provides 'Terminate' and 'Kill' options to allow this distinction.</span></span>

## <a name="syntax"></a><span data-ttu-id="7392f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7392f-109">Syntax</span></span>


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a><span data-ttu-id="7392f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7392f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7392f-111">*DeleteOnKill* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7392f-111">*DeleteOnKill* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7392f-112">Indica si el trabajo debe eliminarse automáticamente tras la terminación.</span><span class="sxs-lookup"><span data-stu-id="7392f-112">Indicates whether or not the Job should be automatically deleted upon termination.</span></span> <span data-ttu-id="7392f-113">Este parámetro tiene prioridad sobre la propiedad **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="7392f-113">This parameter takes precedence over the **DeleteOnCompletion** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7392f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7392f-114">Return value</span></span>

<span data-ttu-id="7392f-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="7392f-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="7392f-116">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="7392f-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7392f-117">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="7392f-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7392f-118">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="7392f-118">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7392f-119">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="7392f-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7392f-120">**Error** (4)</span><span class="sxs-lookup"><span data-stu-id="7392f-120">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7392f-121">**Acceso denegado** (6)</span><span class="sxs-lookup"><span data-stu-id="7392f-121">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7392f-122">**No encontrado** (7)</span><span class="sxs-lookup"><span data-stu-id="7392f-122">**Not Found** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7392f-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="7392f-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7392f-124">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="7392f-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7392f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7392f-125">Requirements</span></span>



| <span data-ttu-id="7392f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7392f-126">Requirement</span></span> | <span data-ttu-id="7392f-127">Value</span><span class="sxs-lookup"><span data-stu-id="7392f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7392f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7392f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7392f-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7392f-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7392f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7392f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7392f-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7392f-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7392f-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7392f-132">Namespace</span></span><br/>                | <span data-ttu-id="7392f-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="7392f-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7392f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7392f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7392f-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7392f-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7392f-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7392f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7392f-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7392f-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7392f-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="7392f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7392f-139">**Trabajo de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="7392f-139">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

 




