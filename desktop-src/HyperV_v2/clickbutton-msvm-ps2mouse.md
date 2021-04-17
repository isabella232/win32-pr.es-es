---
description: Simula un clic en el botón del dispositivo especificado.
ms.assetid: 77CFA2E9-E422-464C-B124-6F7D3D56BA4C
title: Método ClickButton de la clase Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.ClickButton
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffaded2a5e9a8e4e37a158e3aa91b27520dff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687336"
---
# <a name="clickbutton-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="a995b-103">Método ClickButton de la \_ clase Ps2Mouse de MSVM</span><span class="sxs-lookup"><span data-stu-id="a995b-103">ClickButton method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="a995b-104">Simula un clic en el botón del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a995b-104">Simulates a click of the specified device button.</span></span> <span data-ttu-id="a995b-105">Esto es equivalente a llamar a [**SetButtonState**](setbuttonstate-msvm-syntheticmouse.md) dos veces, primero para presionar el botón y volver a publicarlo.</span><span class="sxs-lookup"><span data-stu-id="a995b-105">This is equivalent to calling [**SetButtonState**](setbuttonstate-msvm-syntheticmouse.md) twice, first to press the button, and again to release it.</span></span>

## <a name="syntax"></a><span data-ttu-id="a995b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a995b-106">Syntax</span></span>


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="a995b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a995b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a995b-108">*buttonIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a995b-108">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a995b-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a995b-109">Type: **uint32**</span></span>

<span data-ttu-id="a995b-110">Índice de base 1 del botón.</span><span class="sxs-lookup"><span data-stu-id="a995b-110">The 1-based index of the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a995b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a995b-111">Return value</span></span>

<span data-ttu-id="a995b-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a995b-112">Type: **uint32**</span></span>

<span data-ttu-id="a995b-113">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a995b-113">A return value of zero indicates success.</span></span> <span data-ttu-id="a995b-114">Un valor distinto de cero indica un error al modificar el estado del botón.</span><span class="sxs-lookup"><span data-stu-id="a995b-114">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="a995b-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="a995b-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a995b-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a995b-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a995b-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="a995b-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a995b-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="a995b-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a995b-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="a995b-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a995b-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="a995b-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a995b-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="a995b-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a995b-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a995b-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a995b-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a995b-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a995b-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="a995b-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a995b-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a995b-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a995b-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="a995b-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a995b-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a995b-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a995b-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a995b-128">Remarks</span></span>

<span data-ttu-id="a995b-129">El acceso a la clase [**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="a995b-129">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a995b-130">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a995b-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a995b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a995b-131">Requirements</span></span>



| <span data-ttu-id="a995b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a995b-132">Requirement</span></span> | <span data-ttu-id="a995b-133">Value</span><span class="sxs-lookup"><span data-stu-id="a995b-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a995b-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a995b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a995b-135">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a995b-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a995b-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a995b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a995b-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a995b-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a995b-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a995b-138">Namespace</span></span><br/>                | <span data-ttu-id="a995b-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a995b-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a995b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a995b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a995b-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a995b-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a995b-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a995b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a995b-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a995b-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a995b-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a995b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a995b-145">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="a995b-145">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

