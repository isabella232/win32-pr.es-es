---
description: 'Método SetButtonState de la Msvm_SyntheticMouse : establece el estado actual del botón de dispositivo especificado.'
ms.assetid: 942DB31C-09A2-43B6-A666-267AF6A84E0E
title: Método SetButtonState de la Msvm_SyntheticMouse clase
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
ms.openlocfilehash: 161520ac1b7e9dba1a084a8fb3c623155aa135fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109213"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="8c4fd-103">Método SetButtonState de la clase \_ Msvm SyntheticMouse</span><span class="sxs-lookup"><span data-stu-id="8c4fd-103">SetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="8c4fd-104">Establece el estado actual del botón de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="8c4fd-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c4fd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c4fd-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="8c4fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c4fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c4fd-107">*buttonIndex* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8c4fd-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c4fd-108">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c4fd-108">Type: **uint32**</span></span>

<span data-ttu-id="8c4fd-109">Índice basado en 1 del botón que se modificará.</span><span class="sxs-lookup"><span data-stu-id="8c4fd-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="8c4fd-110">*isDown* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8c4fd-110">*isDown* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c4fd-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8c4fd-111">Type: **boolean**</span></span>

<span data-ttu-id="8c4fd-112">Nuevo estado hacia abajo del botón.</span><span class="sxs-lookup"><span data-stu-id="8c4fd-112">The new down state of the button.</span></span> <span data-ttu-id="8c4fd-113">Un **valor True** significa que el botón está apagado.</span><span class="sxs-lookup"><span data-stu-id="8c4fd-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c4fd-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c4fd-114">Return value</span></span>

<span data-ttu-id="8c4fd-115">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c4fd-115">Type: **uint32**</span></span>

<span data-ttu-id="8c4fd-116">Los valores distintos de cero indican un error al modificar el estado del botón.</span><span class="sxs-lookup"><span data-stu-id="8c4fd-116">Non zero values indicate a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="8c4fd-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8c4fd-118">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8c4fd-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8c4fd-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8c4fd-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8c4fd-122">**El estado es desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8c4fd-123">**Tiempo de** espera (32772)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8c4fd-124">**Parámetro no** válido (32773)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8c4fd-125">**Sistema en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8c4fd-126">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8c4fd-127">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8c4fd-128">**El sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8c4fd-129">**Memoria sin memoria** (32778)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="8c4fd-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c4fd-130">Remarks</span></span>

<span data-ttu-id="8c4fd-131">El acceso a [**la clase \_ Msvm SyntheticMouse**](msvm-syntheticmouse.md) podría estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="8c4fd-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8c4fd-132">Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="8c4fd-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c4fd-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c4fd-133">Requirements</span></span>



| <span data-ttu-id="8c4fd-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c4fd-134">Requirement</span></span> | <span data-ttu-id="8c4fd-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8c4fd-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4fd-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c4fd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8c4fd-137">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="8c4fd-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8c4fd-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c4fd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8c4fd-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c4fd-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c4fd-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c4fd-140">Namespace</span></span><br/>                | <span data-ttu-id="8c4fd-141">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="8c4fd-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8c4fd-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8c4fd-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c4fd-143"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c4fd-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c4fd-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c4fd-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c4fd-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8c4fd-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8c4fd-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8c4fd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c4fd-147">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="8c4fd-147">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

