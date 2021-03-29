---
description: Simula una secuencia de teclas mediante códigos de recorrido.
ms.assetid: F67D2FBA-3CE0-4135-9043-FAB59381DE3C
title: Método TypeScancodes de la clase Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeScancodes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 97479a1a0926894f72472b7459f77cd9325ac6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810418"
---
# <a name="typescancodes-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="f70f5-103">Método TypeScancodes de la \_ clase de teclado MSVM</span><span class="sxs-lookup"><span data-stu-id="f70f5-103">TypeScancodes method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="f70f5-104">Simula una secuencia de teclas mediante códigos de recorrido.</span><span class="sxs-lookup"><span data-stu-id="f70f5-104">Simulates a key sequence using scan codes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f70f5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f70f5-105">Syntax</span></span>


```mof
uint32 TypeScancodes(
  [in] uint8 Scancodes[]
);
```



## <a name="parameters"></a><span data-ttu-id="f70f5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f70f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f70f5-107">*Scancodes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f70f5-107">*Scancodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f70f5-108">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="f70f5-108">Type: **uint8\[\]**</span></span>

<span data-ttu-id="f70f5-109">Una matriz que contiene los códigos de recorrido que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="f70f5-109">An array that contains the scan codes to type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f70f5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f70f5-110">Return value</span></span>

<span data-ttu-id="f70f5-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f70f5-111">Type: **uint32**</span></span>

<span data-ttu-id="f70f5-112">Este método devuelve 0 si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="f70f5-112">This method returns 0 if it succeeds.</span></span> <span data-ttu-id="f70f5-113">Cualquier otro valor devuelto indica un error.</span><span class="sxs-lookup"><span data-stu-id="f70f5-113">Any other return value indicates an error.</span></span> <span data-ttu-id="f70f5-114">El valor devuelto puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f70f5-114">The return value can be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f70f5-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="f70f5-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f70f5-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f70f5-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f70f5-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="f70f5-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f70f5-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="f70f5-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f70f5-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="f70f5-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f70f5-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="f70f5-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f70f5-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="f70f5-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f70f5-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f70f5-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f70f5-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f70f5-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f70f5-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="f70f5-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f70f5-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f70f5-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f70f5-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="f70f5-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f70f5-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f70f5-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f70f5-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f70f5-128">Remarks</span></span>

<span data-ttu-id="f70f5-129">El acceso a la clase de [**\_ teclado MSVM**](msvm-keyboard.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="f70f5-129">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f70f5-130">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f70f5-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f70f5-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f70f5-131">Requirements</span></span>



| <span data-ttu-id="f70f5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f70f5-132">Requirement</span></span> | <span data-ttu-id="f70f5-133">Value</span><span class="sxs-lookup"><span data-stu-id="f70f5-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f70f5-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f70f5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f70f5-135">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f70f5-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f70f5-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f70f5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f70f5-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f70f5-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f70f5-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f70f5-138">Namespace</span></span><br/>                | <span data-ttu-id="f70f5-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f70f5-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f70f5-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f70f5-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f70f5-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f70f5-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f70f5-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f70f5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f70f5-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f70f5-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f70f5-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="f70f5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70f5-145">**\_Teclado MSVM**</span><span class="sxs-lookup"><span data-stu-id="f70f5-145">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

