---
description: Recupera el estado actual del botón del dispositivo especificado.
ms.assetid: 66363AF1-E360-478D-8E62-513DE66EF130
title: Método GetButtonState de la clase Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3812d3e019a303656305471fc097fb1479fa1ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686894"
---
# <a name="getbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="bdbb7-103">Método GetButtonState de la \_ clase SyntheticMouse de MSVM</span><span class="sxs-lookup"><span data-stu-id="bdbb7-103">GetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="bdbb7-104">Recupera el estado actual del botón del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="bdbb7-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdbb7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bdbb7-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="bdbb7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bdbb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdbb7-107">*buttonIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bdbb7-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbb7-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bdbb7-108">Type: **uint32**</span></span>

<span data-ttu-id="bdbb7-109">Índice de base 1 del botón que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="bdbb7-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="bdbb7-110">*isDown* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bdbb7-110">*isDown* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbb7-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bdbb7-111">Type: **boolean**</span></span>

<span data-ttu-id="bdbb7-112">Estado actual del botón.</span><span class="sxs-lookup"><span data-stu-id="bdbb7-112">The current down state of the button.</span></span> <span data-ttu-id="bdbb7-113">Un valor **true** significa que el botón está inactivo.</span><span class="sxs-lookup"><span data-stu-id="bdbb7-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdbb7-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bdbb7-114">Return value</span></span>

<span data-ttu-id="bdbb7-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bdbb7-115">Type: **uint32**</span></span>

<span data-ttu-id="bdbb7-116">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bdbb7-116">A return value of zero indicates success.</span></span> <span data-ttu-id="bdbb7-117">Un valor distinto de cero indica un error en la consulta.</span><span class="sxs-lookup"><span data-stu-id="bdbb7-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="bdbb7-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="bdbb7-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bdbb7-119">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="bdbb7-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bdbb7-120">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="bdbb7-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bdbb7-121">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="bdbb7-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bdbb7-122">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="bdbb7-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bdbb7-123">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="bdbb7-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bdbb7-124">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="bdbb7-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bdbb7-125">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="bdbb7-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bdbb7-126">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="bdbb7-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bdbb7-127">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="bdbb7-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bdbb7-128">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="bdbb7-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bdbb7-129">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="bdbb7-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bdbb7-130">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="bdbb7-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bdbb7-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdbb7-131">Remarks</span></span>

<span data-ttu-id="bdbb7-132">El acceso a la clase [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="bdbb7-132">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bdbb7-133">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bdbb7-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdbb7-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdbb7-134">Requirements</span></span>



| <span data-ttu-id="bdbb7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdbb7-135">Requirement</span></span> | <span data-ttu-id="bdbb7-136">Value</span><span class="sxs-lookup"><span data-stu-id="bdbb7-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdbb7-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdbb7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bdbb7-138">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="bdbb7-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bdbb7-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdbb7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bdbb7-140">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="bdbb7-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bdbb7-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bdbb7-141">Namespace</span></span><br/>                | <span data-ttu-id="bdbb7-142">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bdbb7-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bdbb7-143">MOF</span><span class="sxs-lookup"><span data-stu-id="bdbb7-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bdbb7-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bdbb7-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bdbb7-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bdbb7-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdbb7-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bdbb7-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bdbb7-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdbb7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdbb7-148">**MSVM \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="bdbb7-148">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

