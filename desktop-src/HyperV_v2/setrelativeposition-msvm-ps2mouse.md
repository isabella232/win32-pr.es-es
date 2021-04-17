---
description: Desplaza la posición del puntero del mouse según las diferencias horizontales y verticales especificadas.
ms.assetid: C74E4BEA-C7E1-44C7-B4FC-8926F23DF1FE
title: Método SetRelativePosition de la clase Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetRelativePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b7f4d10f48bce4b33cd4965f08633b85b5a738bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667817"
---
# <a name="setrelativeposition-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="2041f-103">Método SetRelativePosition de la \_ clase Ps2Mouse de MSVM</span><span class="sxs-lookup"><span data-stu-id="2041f-103">SetRelativePosition method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="2041f-104">Desplaza la posición del puntero del mouse según las diferencias horizontales y verticales especificadas.</span><span class="sxs-lookup"><span data-stu-id="2041f-104">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span>

## <a name="syntax"></a><span data-ttu-id="2041f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2041f-105">Syntax</span></span>


```mof
uint32 SetRelativePosition(
  [in] sint8 horizontalDelta,
  [in] sint8 verticalDelta
);
```



## <a name="parameters"></a><span data-ttu-id="2041f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2041f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2041f-107">*horizontalDelta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2041f-107">*horizontalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2041f-108">Tipo: **sint8**</span><span class="sxs-lookup"><span data-stu-id="2041f-108">Type: **sint8**</span></span>

<span data-ttu-id="2041f-109">Cambio horizontal en la posición del mouse, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="2041f-109">The horizontal change for the mouse position, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="2041f-110">*verticalDelta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2041f-110">*verticalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2041f-111">Tipo: **sint8**</span><span class="sxs-lookup"><span data-stu-id="2041f-111">Type: **sint8**</span></span>

<span data-ttu-id="2041f-112">Cambio vertical en la posición del mouse, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="2041f-112">The vertical change for the mouse position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2041f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2041f-113">Return value</span></span>

<span data-ttu-id="2041f-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2041f-114">Type: **uint32**</span></span>

<span data-ttu-id="2041f-115">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2041f-115">A return value of zero indicates success.</span></span> <span data-ttu-id="2041f-116">Un valor distinto de cero indica un error al modificar la posición del mouse.</span><span class="sxs-lookup"><span data-stu-id="2041f-116">A nonzero value indicates a failure to alter the mouse position.</span></span>

<dl> <dt>

<span data-ttu-id="2041f-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="2041f-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2041f-118">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="2041f-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2041f-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="2041f-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2041f-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="2041f-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2041f-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="2041f-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2041f-122">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="2041f-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2041f-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="2041f-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2041f-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="2041f-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2041f-125">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="2041f-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2041f-126">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="2041f-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2041f-127">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="2041f-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2041f-128">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="2041f-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2041f-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="2041f-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2041f-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2041f-130">Remarks</span></span>

<span data-ttu-id="2041f-131">El acceso a la clase [**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="2041f-131">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2041f-132">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2041f-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2041f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2041f-133">Requirements</span></span>



| <span data-ttu-id="2041f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2041f-134">Requirement</span></span> | <span data-ttu-id="2041f-135">Value</span><span class="sxs-lookup"><span data-stu-id="2041f-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2041f-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2041f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2041f-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2041f-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2041f-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2041f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2041f-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2041f-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2041f-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2041f-140">Namespace</span></span><br/>                | <span data-ttu-id="2041f-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2041f-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2041f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2041f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2041f-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2041f-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2041f-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2041f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2041f-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2041f-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2041f-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="2041f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2041f-147">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="2041f-147">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

