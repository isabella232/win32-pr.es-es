---
description: Recupera un error debido a un trabajo con error.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: Método GetError de la clase CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aa9ed87f2d484286d91d14c4183d2ce3b6f41cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687047"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a><span data-ttu-id="1cc1e-103">Método GetError de la \_ clase ConcreteJob de CIM</span><span class="sxs-lookup"><span data-stu-id="1cc1e-103">GetError method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="1cc1e-104">Recupera un error debido a un trabajo con error.</span><span class="sxs-lookup"><span data-stu-id="1cc1e-104">Retrieves an error due to a failed job.</span></span> <span data-ttu-id="1cc1e-105">Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna instancia de [**\_ error de CIM**](cim-error.md) .</span><span class="sxs-lookup"><span data-stu-id="1cc1e-105">When the job is executing or has terminated without error, then this method returns no [**CIM\_Error**](cim-error.md) instance.</span></span> <span data-ttu-id="1cc1e-106">Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque el trabajo ha sido terminado por un cliente, se devuelve una instancia de **\_ error de CIM** .</span><span class="sxs-lookup"><span data-stu-id="1cc1e-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc1e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cc1e-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="1cc1e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cc1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc1e-109">*Error* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1cc1e-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc1e-110">Devuelve una instancia de [**\_ error de CIM**](cim-error.md) si el valor de **OperationalStatus** en el trabajo no es "OK"; en caso contrario, devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="1cc1e-110">Returns a [**CIM\_Error**](cim-error.md) instance if the **OperationalStatus** on the Job is not "OK"; otherwise, returns **null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc1e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cc1e-111">Return value</span></span>

<span data-ttu-id="1cc1e-112">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="1cc1e-112">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1cc1e-113">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="1cc1e-113">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1cc1e-114">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="1cc1e-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1cc1e-115">**Error no especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="1cc1e-115">**Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1cc1e-116">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="1cc1e-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1cc1e-117">**Error** (4)</span><span class="sxs-lookup"><span data-stu-id="1cc1e-117">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1cc1e-118">**Parámetro no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="1cc1e-118">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1cc1e-119">**Acceso denegado** (6)</span><span class="sxs-lookup"><span data-stu-id="1cc1e-119">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1cc1e-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1cc1e-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1cc1e-121">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="1cc1e-121">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1cc1e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cc1e-122">Requirements</span></span>



| <span data-ttu-id="1cc1e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc1e-123">Requirement</span></span> | <span data-ttu-id="1cc1e-124">Value</span><span class="sxs-lookup"><span data-stu-id="1cc1e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc1e-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cc1e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1cc1e-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1cc1e-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1cc1e-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cc1e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1cc1e-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1cc1e-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1cc1e-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1cc1e-129">Namespace</span></span><br/>                | <span data-ttu-id="1cc1e-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1cc1e-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1cc1e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1cc1e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1cc1e-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1cc1e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1cc1e-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1cc1e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cc1e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1cc1e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1cc1e-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cc1e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc1e-136">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="1cc1e-136">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 




