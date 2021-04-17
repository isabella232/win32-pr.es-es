---
description: Recupera los objetos de error del trabajo, si existen.
ms.assetid: B4B4F60C-9221-4125-8D42-F0F1D32C3E79
title: Método GetErrorEx de la clase Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e938d41afad430051bebb08fc77d6edf6da44691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686889"
---
# <a name="geterrorex-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="b8bbd-103">Método GetErrorEx de la \_ clase ConcreteJob de MSVM</span><span class="sxs-lookup"><span data-stu-id="b8bbd-103">GetErrorEx method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="b8bbd-104">Recupera los objetos de error del trabajo, si existen.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="b8bbd-105">Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna instancia de [**\_ error MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="b8bbd-105">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="b8bbd-106">Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque el trabajo ha sido terminado por un cliente, se devuelven una o varias instancias de **\_ error de MSVM** .</span><span class="sxs-lookup"><span data-stu-id="b8bbd-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8bbd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8bbd-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="b8bbd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8bbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8bbd-109">*Errores* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b8bbd-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8bbd-110">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="b8bbd-110">Type: **string\[\]**</span></span>

<span data-ttu-id="b8bbd-111">Si el estado operativo del trabajo no es 2 (correcto), este método devuelve una o varias instancias incrustadas de la clase de [**\_ error MSVM**](msvm-error.md) , en formato CIM-XML, que representan los errores encontrados en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-111">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="b8bbd-112">Si el estado operativo del trabajo es 2 (correcto), se devuelve **null** .</span><span class="sxs-lookup"><span data-stu-id="b8bbd-112">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8bbd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8bbd-113">Return value</span></span>

<span data-ttu-id="b8bbd-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8bbd-114">Type: **uint32**</span></span>

<span data-ttu-id="b8bbd-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b8bbd-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="b8bbd-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b8bbd-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="b8bbd-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b8bbd-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="b8bbd-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b8bbd-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="b8bbd-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b8bbd-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="b8bbd-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b8bbd-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="b8bbd-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b8bbd-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b8bbd-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b8bbd-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b8bbd-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b8bbd-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="b8bbd-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b8bbd-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b8bbd-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b8bbd-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="b8bbd-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b8bbd-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b8bbd-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b8bbd-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8bbd-128">Remarks</span></span>

<span data-ttu-id="b8bbd-129">El acceso a la clase [**MSVM \_ ConcreteJob**](msvm-concretejob.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="b8bbd-129">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b8bbd-130">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b8bbd-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8bbd-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8bbd-131">Requirements</span></span>



| <span data-ttu-id="b8bbd-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8bbd-132">Requirement</span></span> | <span data-ttu-id="b8bbd-133">Value</span><span class="sxs-lookup"><span data-stu-id="b8bbd-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8bbd-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8bbd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b8bbd-135">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8bbd-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b8bbd-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8bbd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b8bbd-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8bbd-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8bbd-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8bbd-138">Namespace</span></span><br/>                | <span data-ttu-id="b8bbd-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b8bbd-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b8bbd-140">MOF</span><span class="sxs-lookup"><span data-stu-id="b8bbd-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8bbd-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8bbd-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8bbd-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8bbd-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8bbd-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8bbd-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b8bbd-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8bbd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8bbd-145">**MSVM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="b8bbd-145">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

