---
description: Recupera el estado actual del botón del dispositivo especificado.
ms.assetid: 7772A3AC-1677-44A7-9E5E-D31E90988705
title: Método GetButtonState de la clase Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8bb0df6ad49f0d260d95c6f65e0f0f481b393dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666560"
---
# <a name="getbuttonstate-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="826cc-103">Método GetButtonState de la \_ clase Ps2Mouse de MSVM</span><span class="sxs-lookup"><span data-stu-id="826cc-103">GetButtonState method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="826cc-104">Recupera el estado actual del botón del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="826cc-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="826cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="826cc-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean buttonState
);
```



## <a name="parameters"></a><span data-ttu-id="826cc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="826cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="826cc-107">*buttonIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="826cc-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="826cc-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="826cc-108">Type: **uint32**</span></span>

<span data-ttu-id="826cc-109">Índice de base 1 del botón que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="826cc-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="826cc-110">*buttonState* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="826cc-110">*buttonState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="826cc-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="826cc-111">Type: **boolean**</span></span>

<span data-ttu-id="826cc-112">Estado actual del botón.</span><span class="sxs-lookup"><span data-stu-id="826cc-112">The current down state of the button.</span></span> <span data-ttu-id="826cc-113">Un valor **true** significa que el botón está inactivo.</span><span class="sxs-lookup"><span data-stu-id="826cc-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="826cc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="826cc-114">Return value</span></span>

<span data-ttu-id="826cc-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="826cc-115">Type: **uint32**</span></span>

<span data-ttu-id="826cc-116">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="826cc-116">A return value of zero indicates success.</span></span> <span data-ttu-id="826cc-117">Un valor distinto de cero indica un error en la consulta.</span><span class="sxs-lookup"><span data-stu-id="826cc-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="826cc-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="826cc-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="826cc-119">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="826cc-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="826cc-120">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="826cc-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="826cc-121">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="826cc-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="826cc-122">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="826cc-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="826cc-123">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="826cc-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="826cc-124">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="826cc-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="826cc-125">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="826cc-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="826cc-126">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="826cc-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="826cc-127">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="826cc-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="826cc-128">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="826cc-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="826cc-129">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="826cc-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="826cc-130">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="826cc-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="826cc-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="826cc-131">Remarks</span></span>

<span data-ttu-id="826cc-132">El acceso a la clase [**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="826cc-132">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="826cc-133">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="826cc-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="826cc-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="826cc-134">Requirements</span></span>



| <span data-ttu-id="826cc-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="826cc-135">Requirement</span></span> | <span data-ttu-id="826cc-136">Value</span><span class="sxs-lookup"><span data-stu-id="826cc-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="826cc-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="826cc-137">Minimum supported client</span></span><br/> | <span data-ttu-id="826cc-138">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="826cc-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="826cc-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="826cc-139">Minimum supported server</span></span><br/> | <span data-ttu-id="826cc-140">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="826cc-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="826cc-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="826cc-141">Namespace</span></span><br/>                | <span data-ttu-id="826cc-142">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="826cc-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="826cc-143">MOF</span><span class="sxs-lookup"><span data-stu-id="826cc-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="826cc-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="826cc-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="826cc-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="826cc-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="826cc-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="826cc-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="826cc-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="826cc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826cc-148">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="826cc-148">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

