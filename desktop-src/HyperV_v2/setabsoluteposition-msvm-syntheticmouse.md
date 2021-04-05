---
description: Establece la posición horizontal y vertical del cursor del mouse.
ms.assetid: 7845E10A-7F61-4134-BF81-AED5483F36AD
title: Método SetAbsolutePosition de la clase Msvm_SyntheticMouse (Dbdao. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetAbsolutePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b8ffb3a4d415f76dedf30acba5869b4cc585eb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909506"
---
# <a name="setabsoluteposition-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="df045-103">Método SetAbsolutePosition de la \_ clase SyntheticMouse de MSVM</span><span class="sxs-lookup"><span data-stu-id="df045-103">SetAbsolutePosition method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="df045-104">Establece la posición horizontal y vertical del cursor del mouse.</span><span class="sxs-lookup"><span data-stu-id="df045-104">Sets the horizontal and vertical position of the mouse cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="df045-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df045-105">Syntax</span></span>


```mof
uint32 SetAbsolutePosition(
  [in] sint32 horizontalPosition,
  [in] sint32 verticalPosition
);
```



## <a name="parameters"></a><span data-ttu-id="df045-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df045-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df045-107">*horizontalPosition* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="df045-107">*horizontalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df045-108">Tipo: **sint32**</span><span class="sxs-lookup"><span data-stu-id="df045-108">Type: **sint32**</span></span>

<span data-ttu-id="df045-109">Nueva posición horizontal del cursor del mouse, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="df045-109">The new horizontal position of the mouse cursor, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="df045-110">*verticalPosition* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="df045-110">*verticalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df045-111">Tipo: **sint32**</span><span class="sxs-lookup"><span data-stu-id="df045-111">Type: **sint32**</span></span>

<span data-ttu-id="df045-112">Nueva posición vertical del cursor del mouse, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="df045-112">The new vertical position of the mouse cursor, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df045-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df045-113">Return value</span></span>

<span data-ttu-id="df045-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df045-114">Type: **uint32**</span></span>

<span data-ttu-id="df045-115">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="df045-115">A return value of zero indicates success.</span></span> <span data-ttu-id="df045-116">Un valor distinto de cero indica un error al modificar la posición de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="df045-116">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="df045-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="df045-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="df045-118">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="df045-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="df045-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="df045-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="df045-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="df045-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="df045-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="df045-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="df045-122">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="df045-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="df045-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="df045-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="df045-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="df045-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="df045-125">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="df045-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="df045-126">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="df045-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="df045-127">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="df045-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="df045-128">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="df045-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="df045-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="df045-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="df045-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df045-130">Remarks</span></span>

<span data-ttu-id="df045-131">El acceso a la clase [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="df045-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="df045-132">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="df045-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="df045-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df045-133">Requirements</span></span>



| <span data-ttu-id="df045-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="df045-134">Requirement</span></span> | <span data-ttu-id="df045-135">Value</span><span class="sxs-lookup"><span data-stu-id="df045-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df045-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df045-136">Minimum supported client</span></span><br/> | <span data-ttu-id="df045-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="df045-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="df045-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df045-138">Minimum supported server</span></span><br/> | <span data-ttu-id="df045-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="df045-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="df045-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="df045-140">Namespace</span></span><br/>                | <span data-ttu-id="df045-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="df045-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="df045-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df045-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="df045-143"><dt>Dbdao. h</dt></span><span class="sxs-lookup"><span data-stu-id="df045-143"><dt>Dbdao.h</dt></span></span> </dl>                      |
| <span data-ttu-id="df045-144">MOF</span><span class="sxs-lookup"><span data-stu-id="df045-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df045-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df045-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="df045-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="df045-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df045-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="df045-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="df045-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="df045-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df045-149">**MSVM \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="df045-149">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

