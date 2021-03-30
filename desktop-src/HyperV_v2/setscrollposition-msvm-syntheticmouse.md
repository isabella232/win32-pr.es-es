---
description: Establece la coordenada z del control de rueda del dispositivo señalador.
ms.assetid: 02349957-6BAA-42E7-B3D4-F39E748615E6
title: Método SetScrollPosition de la clase Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6d82ad2cd75b41ca914d0db49d5de4709790ea6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156724"
---
# <a name="setscrollposition-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="e01ed-103">Método SetScrollPosition de la \_ clase SyntheticMouse de MSVM</span><span class="sxs-lookup"><span data-stu-id="e01ed-103">SetScrollPosition method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="e01ed-104">Establece la coordenada z del control de rueda del dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="e01ed-104">Sets the z-coordinate of the wheel control of the pointing device.</span></span> <span data-ttu-id="e01ed-105">Los valores escritos en esta propiedad son siempre desplazamientos de coordenadas relativos.</span><span class="sxs-lookup"><span data-stu-id="e01ed-105">Values written to this property are always relative coordinate offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="e01ed-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e01ed-106">Syntax</span></span>


```mof
uint32 SetScrollPosition(
  [in] sint32 scrollPositionDelta
);
```



## <a name="parameters"></a><span data-ttu-id="e01ed-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e01ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e01ed-108">*scrollPositionDelta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e01ed-108">*scrollPositionDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e01ed-109">Tipo: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e01ed-109">Type: **sint32**</span></span>

<span data-ttu-id="e01ed-110">Delta de la posición de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="e01ed-110">The delta of the scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e01ed-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e01ed-111">Return value</span></span>

<span data-ttu-id="e01ed-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e01ed-112">Type: **uint32**</span></span>

<span data-ttu-id="e01ed-113">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e01ed-113">A return value of zero indicates success.</span></span> <span data-ttu-id="e01ed-114">Un valor distinto de cero indica un error al modificar la posición de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="e01ed-114">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="e01ed-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="e01ed-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e01ed-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e01ed-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e01ed-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="e01ed-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e01ed-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e01ed-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e01ed-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="e01ed-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e01ed-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e01ed-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e01ed-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="e01ed-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e01ed-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e01ed-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e01ed-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e01ed-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e01ed-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="e01ed-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e01ed-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e01ed-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e01ed-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="e01ed-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e01ed-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e01ed-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e01ed-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e01ed-128">Remarks</span></span>

<span data-ttu-id="e01ed-129">El acceso a la clase [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="e01ed-129">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e01ed-130">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e01ed-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e01ed-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e01ed-131">Requirements</span></span>



| <span data-ttu-id="e01ed-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e01ed-132">Requirement</span></span> | <span data-ttu-id="e01ed-133">Value</span><span class="sxs-lookup"><span data-stu-id="e01ed-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e01ed-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e01ed-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e01ed-135">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e01ed-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e01ed-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e01ed-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e01ed-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e01ed-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e01ed-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e01ed-138">Namespace</span></span><br/>                | <span data-ttu-id="e01ed-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e01ed-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e01ed-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e01ed-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e01ed-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e01ed-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e01ed-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e01ed-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e01ed-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e01ed-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e01ed-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="e01ed-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e01ed-145">**MSVM \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="e01ed-145">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

