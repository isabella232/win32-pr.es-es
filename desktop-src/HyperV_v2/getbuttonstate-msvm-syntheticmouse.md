---
description: 'Método GetButtonState de la Msvm_SyntheticMouse : recupera el estado actual del botón de dispositivo especificado.'
ms.assetid: 66363AF1-E360-478D-8E62-513DE66EF130
title: Método GetButtonState de la Msvm_SyntheticMouse clase
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
ms.openlocfilehash: 26839292cf2fb3099e740629b28c7de0fbe3f60f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119393"
---
# <a name="getbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="6be5e-103">Método GetButtonState de la clase \_ Msvm SyntheticMouse</span><span class="sxs-lookup"><span data-stu-id="6be5e-103">GetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="6be5e-104">Recupera el estado actual del botón de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="6be5e-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="6be5e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6be5e-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="6be5e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6be5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6be5e-107">*buttonIndex* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6be5e-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6be5e-108">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="6be5e-108">Type: **uint32**</span></span>

<span data-ttu-id="6be5e-109">Índice basado en 1 del botón que se consulta.</span><span class="sxs-lookup"><span data-stu-id="6be5e-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="6be5e-110">*isDown* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6be5e-110">*isDown* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6be5e-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6be5e-111">Type: **boolean**</span></span>

<span data-ttu-id="6be5e-112">Estado actual hacia abajo del botón.</span><span class="sxs-lookup"><span data-stu-id="6be5e-112">The current down state of the button.</span></span> <span data-ttu-id="6be5e-113">Un **valor True** significa que el botón está apagado.</span><span class="sxs-lookup"><span data-stu-id="6be5e-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6be5e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6be5e-114">Return value</span></span>

<span data-ttu-id="6be5e-115">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="6be5e-115">Type: **uint32**</span></span>

<span data-ttu-id="6be5e-116">Un valor devuelto de cero indica que se ha correcto.</span><span class="sxs-lookup"><span data-stu-id="6be5e-116">A return value of zero indicates success.</span></span> <span data-ttu-id="6be5e-117">Un valor distinto de cero indica un error de consulta.</span><span class="sxs-lookup"><span data-stu-id="6be5e-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="6be5e-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="6be5e-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6be5e-119">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="6be5e-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6be5e-120">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="6be5e-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6be5e-121">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="6be5e-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6be5e-122">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="6be5e-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6be5e-123">**El estado es desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="6be5e-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6be5e-124">**Tiempo de** espera (32772)</span><span class="sxs-lookup"><span data-stu-id="6be5e-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6be5e-125">**Parámetro no** válido (32773)</span><span class="sxs-lookup"><span data-stu-id="6be5e-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6be5e-126">**Sistema en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="6be5e-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6be5e-127">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="6be5e-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6be5e-128">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="6be5e-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6be5e-129">**El sistema no está** disponible (32777)</span><span class="sxs-lookup"><span data-stu-id="6be5e-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6be5e-130">**Memoria sin memoria** (32778)</span><span class="sxs-lookup"><span data-stu-id="6be5e-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6be5e-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6be5e-131">Remarks</span></span>

<span data-ttu-id="6be5e-132">El acceso a [**la clase \_ Msvm SyntheticMouse**](msvm-syntheticmouse.md) podría estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="6be5e-132">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6be5e-133">Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="6be5e-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6be5e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6be5e-134">Requirements</span></span>



| <span data-ttu-id="6be5e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6be5e-135">Requirement</span></span> | <span data-ttu-id="6be5e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="6be5e-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6be5e-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6be5e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6be5e-138">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="6be5e-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6be5e-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6be5e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6be5e-140">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="6be5e-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6be5e-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6be5e-141">Namespace</span></span><br/>                | <span data-ttu-id="6be5e-142">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="6be5e-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6be5e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="6be5e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6be5e-144"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="6be5e-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6be5e-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6be5e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6be5e-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6be5e-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6be5e-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6be5e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6be5e-148">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="6be5e-148">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

