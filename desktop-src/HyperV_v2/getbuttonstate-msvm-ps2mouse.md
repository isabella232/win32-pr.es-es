---
description: 'Método GetButtonState de Msvm_Ps2Mouse clase : recupera el estado actual del botón de dispositivo especificado.'
ms.assetid: 7772A3AC-1677-44A7-9E5E-D31E90988705
title: Método GetButtonState de la Msvm_Ps2Mouse clase
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
ms.openlocfilehash: 160134a2ae48bb23dc525eeded70b483484e0b71
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112203"
---
# <a name="getbuttonstate-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="741c2-103">Método GetButtonState de la clase \_ Ps2Mouse de Msvm</span><span class="sxs-lookup"><span data-stu-id="741c2-103">GetButtonState method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="741c2-104">Recupera el estado actual del botón de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="741c2-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="741c2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="741c2-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean buttonState
);
```



## <a name="parameters"></a><span data-ttu-id="741c2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="741c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="741c2-107">*buttonIndex* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="741c2-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="741c2-108">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="741c2-108">Type: **uint32**</span></span>

<span data-ttu-id="741c2-109">Índice basado en 1 del botón que se consulta.</span><span class="sxs-lookup"><span data-stu-id="741c2-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="741c2-110">*buttonState* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="741c2-110">*buttonState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="741c2-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="741c2-111">Type: **boolean**</span></span>

<span data-ttu-id="741c2-112">Estado de apagado actual del botón.</span><span class="sxs-lookup"><span data-stu-id="741c2-112">The current down state of the button.</span></span> <span data-ttu-id="741c2-113">Un **valor True** significa que el botón está apagado.</span><span class="sxs-lookup"><span data-stu-id="741c2-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="741c2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="741c2-114">Return value</span></span>

<span data-ttu-id="741c2-115">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="741c2-115">Type: **uint32**</span></span>

<span data-ttu-id="741c2-116">Un valor devuelto de cero indica que el resultado es correcto.</span><span class="sxs-lookup"><span data-stu-id="741c2-116">A return value of zero indicates success.</span></span> <span data-ttu-id="741c2-117">Un valor distinto de cero indica un error de consulta.</span><span class="sxs-lookup"><span data-stu-id="741c2-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="741c2-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="741c2-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="741c2-119">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="741c2-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="741c2-120">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="741c2-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="741c2-121">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="741c2-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="741c2-122">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="741c2-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="741c2-123">**El estado es desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="741c2-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="741c2-124">**Tiempo de** espera (32772)</span><span class="sxs-lookup"><span data-stu-id="741c2-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="741c2-125">**Parámetro no** válido (32773)</span><span class="sxs-lookup"><span data-stu-id="741c2-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="741c2-126">**Sistema en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="741c2-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="741c2-127">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="741c2-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="741c2-128">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="741c2-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="741c2-129">**El sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="741c2-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="741c2-130">**Memoria sin memoria** (32778)</span><span class="sxs-lookup"><span data-stu-id="741c2-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="741c2-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="741c2-131">Remarks</span></span>

<span data-ttu-id="741c2-132">El acceso a [**la clase \_ Ps2Mouse de Msvm**](msvm-ps2mouse.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="741c2-132">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="741c2-133">Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="741c2-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="741c2-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="741c2-134">Requirements</span></span>



| <span data-ttu-id="741c2-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="741c2-135">Requirement</span></span> | <span data-ttu-id="741c2-136">Valor</span><span class="sxs-lookup"><span data-stu-id="741c2-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="741c2-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="741c2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="741c2-138">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="741c2-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="741c2-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="741c2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="741c2-140">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="741c2-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="741c2-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="741c2-141">Namespace</span></span><br/>                | <span data-ttu-id="741c2-142">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="741c2-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="741c2-143">MOF</span><span class="sxs-lookup"><span data-stu-id="741c2-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="741c2-144"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="741c2-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="741c2-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="741c2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="741c2-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="741c2-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="741c2-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="741c2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="741c2-148">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="741c2-148">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

