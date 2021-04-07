---
description: Ajusta la coordenada z del control de rueda del dispositivo señalador.
ms.assetid: FF1929EE-4A2D-4761-8919-488369FAEE1F
title: Método SetScrollPosition de la clase Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffec8e05acf2210c55038edde5def8373e900ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911001"
---
# <a name="setscrollposition-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="a3871-103">Método SetScrollPosition de la \_ clase Ps2Mouse de MSVM</span><span class="sxs-lookup"><span data-stu-id="a3871-103">SetScrollPosition method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="a3871-104">Ajusta la coordenada z del control de rueda del dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="a3871-104">Adjusts the z-coordinate of the wheel control of the pointing device.</span></span> <span data-ttu-id="a3871-105">Los valores escritos en esta propiedad son siempre desplazamientos de coordenadas relativos.</span><span class="sxs-lookup"><span data-stu-id="a3871-105">Values written to this property are always relative coordinate offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3871-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3871-106">Syntax</span></span>


```mof
uint32 SetScrollPosition(
  [in] sint8 scrollPositionDelta
);
```



## <a name="parameters"></a><span data-ttu-id="a3871-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3871-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3871-108">*scrollPositionDelta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3871-108">*scrollPositionDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3871-109">Tipo: **sint8**</span><span class="sxs-lookup"><span data-stu-id="a3871-109">Type: **sint8**</span></span>

<span data-ttu-id="a3871-110">Delta de la posición de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="a3871-110">The delta of the scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3871-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3871-111">Return value</span></span>

<span data-ttu-id="a3871-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a3871-112">Type: **uint32**</span></span>

<span data-ttu-id="a3871-113">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a3871-113">A return value of zero indicates success.</span></span> <span data-ttu-id="a3871-114">Un valor distinto de cero indica un error al modificar la posición de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="a3871-114">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="a3871-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="a3871-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a3871-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a3871-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a3871-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="a3871-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a3871-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="a3871-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a3871-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="a3871-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a3871-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="a3871-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a3871-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="a3871-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a3871-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a3871-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a3871-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a3871-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a3871-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="a3871-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a3871-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a3871-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a3871-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="a3871-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a3871-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a3871-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a3871-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3871-128">Remarks</span></span>

<span data-ttu-id="a3871-129">El acceso a la clase [**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="a3871-129">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a3871-130">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a3871-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3871-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3871-131">Requirements</span></span>



| <span data-ttu-id="a3871-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3871-132">Requirement</span></span> | <span data-ttu-id="a3871-133">Value</span><span class="sxs-lookup"><span data-stu-id="a3871-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3871-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3871-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a3871-135">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a3871-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a3871-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3871-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a3871-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a3871-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a3871-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a3871-138">Namespace</span></span><br/>                | <span data-ttu-id="a3871-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a3871-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a3871-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a3871-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3871-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3871-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3871-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a3871-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3871-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a3871-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a3871-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3871-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3871-145">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="a3871-145">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

