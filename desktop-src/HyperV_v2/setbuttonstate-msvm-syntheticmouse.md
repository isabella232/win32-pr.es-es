---
description: Establece el estado actual del botón del dispositivo especificado.
ms.assetid: 942DB31C-09A2-43B6-A666-267AF6A84E0E
title: Método SetButtonState de la clase Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c99915fa8ede9cbb405f4483ac10ca9ff8efaf71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276730"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="d5251-103">Método SetButtonState de la \_ clase SyntheticMouse de MSVM</span><span class="sxs-lookup"><span data-stu-id="d5251-103">SetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="d5251-104">Establece el estado actual del botón del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d5251-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5251-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5251-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="d5251-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5251-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5251-107">*buttonIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5251-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5251-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d5251-108">Type: **uint32**</span></span>

<span data-ttu-id="d5251-109">Índice de base 1 del botón que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="d5251-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="d5251-110">*isDown* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5251-110">*isDown* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5251-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d5251-111">Type: **boolean**</span></span>

<span data-ttu-id="d5251-112">Nuevo estado de inactividad del botón.</span><span class="sxs-lookup"><span data-stu-id="d5251-112">The new down state of the button.</span></span> <span data-ttu-id="d5251-113">Un valor **true** significa que el botón está inactivo.</span><span class="sxs-lookup"><span data-stu-id="d5251-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5251-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5251-114">Return value</span></span>

<span data-ttu-id="d5251-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d5251-115">Type: **uint32**</span></span>

<span data-ttu-id="d5251-116">Un valor distinto de cero indica un error al modificar el estado del botón.</span><span class="sxs-lookup"><span data-stu-id="d5251-116">Non zero values indicate a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="d5251-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="d5251-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d5251-118">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="d5251-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d5251-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="d5251-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d5251-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="d5251-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d5251-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="d5251-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d5251-122">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="d5251-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d5251-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="d5251-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d5251-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="d5251-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d5251-125">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="d5251-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d5251-126">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="d5251-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d5251-127">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="d5251-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d5251-128">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="d5251-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d5251-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="d5251-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d5251-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5251-130">Remarks</span></span>

<span data-ttu-id="d5251-131">El acceso a la clase [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="d5251-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d5251-132">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d5251-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5251-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5251-133">Requirements</span></span>



| <span data-ttu-id="d5251-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5251-134">Requirement</span></span> | <span data-ttu-id="d5251-135">Value</span><span class="sxs-lookup"><span data-stu-id="d5251-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5251-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5251-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d5251-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5251-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d5251-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5251-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d5251-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5251-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d5251-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d5251-140">Namespace</span></span><br/>                | <span data-ttu-id="d5251-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d5251-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d5251-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d5251-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5251-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5251-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5251-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d5251-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5251-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d5251-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d5251-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5251-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5251-147">**MSVM \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="d5251-147">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

