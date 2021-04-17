---
description: Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna \_ instancia de error MSVM.
ms.assetid: 119E7EFD-78C9-46F1-8A53-C51A7A34B32E
title: Método GetErrorEx de la clase Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26d5aff37631de00cffccd49cf54f0ba09ce5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666553"
---
# <a name="geterrorex-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="e91b6-103">Método GetErrorEx de la \_ clase StorageJob de MSVM</span><span class="sxs-lookup"><span data-stu-id="e91b6-103">GetErrorEx method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="e91b6-104">Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna instancia de [**\_ error MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="e91b6-104">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="e91b6-105">Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque el trabajo ha sido terminado por un cliente, se devuelven una o varias instancias de **\_ error de MSVM** .</span><span class="sxs-lookup"><span data-stu-id="e91b6-105">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="e91b6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e91b6-106">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="e91b6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e91b6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e91b6-108">*Errores* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e91b6-108">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e91b6-109">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e91b6-109">Type: **string\[\]**</span></span>

<span data-ttu-id="e91b6-110">Si el estado operativo del trabajo no es "correcto", este método devuelve una matriz de instancias [**de \_ error de MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="e91b6-110">If the operational status of the job is not "OK", this method returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="e91b6-111">De lo contrario, si el trabajo es "OK", se devuelve **null** .</span><span class="sxs-lookup"><span data-stu-id="e91b6-111">Otherwise, if the job is "OK", **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e91b6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e91b6-112">Return value</span></span>

<span data-ttu-id="e91b6-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e91b6-113">Type: **uint32**</span></span>

<span data-ttu-id="e91b6-114">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e91b6-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e91b6-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="e91b6-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e91b6-116">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="e91b6-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e91b6-117">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e91b6-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e91b6-118">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="e91b6-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e91b6-119">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e91b6-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e91b6-120">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="e91b6-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e91b6-121">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e91b6-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e91b6-122">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e91b6-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e91b6-123">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="e91b6-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e91b6-124">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e91b6-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e91b6-125">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="e91b6-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e91b6-126">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e91b6-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e91b6-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e91b6-127">Remarks</span></span>

<span data-ttu-id="e91b6-128">El acceso a la clase [**MSVM \_ StorageJob**](msvm-storagejob.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="e91b6-128">Access to the [**Msvm\_StorageJob**](msvm-storagejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e91b6-129">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e91b6-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e91b6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e91b6-130">Requirements</span></span>



| <span data-ttu-id="e91b6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e91b6-131">Requirement</span></span> | <span data-ttu-id="e91b6-132">Value</span><span class="sxs-lookup"><span data-stu-id="e91b6-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e91b6-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e91b6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e91b6-134">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e91b6-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e91b6-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e91b6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e91b6-136">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e91b6-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e91b6-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e91b6-137">Namespace</span></span><br/>                | <span data-ttu-id="e91b6-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e91b6-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e91b6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e91b6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e91b6-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e91b6-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e91b6-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e91b6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e91b6-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e91b6-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e91b6-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="e91b6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e91b6-144">**MSVM \_ StorageJob**</span><span class="sxs-lookup"><span data-stu-id="e91b6-144">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

