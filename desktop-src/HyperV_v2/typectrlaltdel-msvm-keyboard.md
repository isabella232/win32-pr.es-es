---
description: Simula una secuencia de teclas Ctrl + Alt + Supr.
ms.assetid: C24C9C42-844F-4560-B8C1-0054F5E913D6
title: Método TypeCtrlAltDel de la clase Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeCtrlAltDel
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 64ebc4bddf8adccd7098cafed1df43d1cf1cb4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361233"
---
# <a name="typectrlaltdel-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="5e086-103">Método TypeCtrlAltDel de la \_ clase de teclado MSVM</span><span class="sxs-lookup"><span data-stu-id="5e086-103">TypeCtrlAltDel method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="5e086-104">Simula una secuencia de teclas Ctrl + Alt + Supr.</span><span class="sxs-lookup"><span data-stu-id="5e086-104">Simulates a Ctrl+Alt+Del key sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e086-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e086-105">Syntax</span></span>


```mof
uint32 TypeCtrlAltDel();
```



## <a name="parameters"></a><span data-ttu-id="5e086-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e086-106">Parameters</span></span>

<span data-ttu-id="5e086-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5e086-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e086-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e086-108">Return value</span></span>

<span data-ttu-id="5e086-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e086-109">Type: **uint32**</span></span>

<span data-ttu-id="5e086-110">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5e086-110">A return value of zero indicates success.</span></span> <span data-ttu-id="5e086-111">Un valor distinto de cero indica un error de envío.</span><span class="sxs-lookup"><span data-stu-id="5e086-111">A nonzero value indicates a failure to send.</span></span>

<dl> <dt>

<span data-ttu-id="5e086-112">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="5e086-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5e086-113">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="5e086-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5e086-114">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="5e086-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5e086-115">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="5e086-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5e086-116">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="5e086-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5e086-117">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="5e086-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5e086-118">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="5e086-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5e086-119">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="5e086-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5e086-120">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="5e086-120">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5e086-121">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="5e086-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5e086-122">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="5e086-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5e086-123">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="5e086-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5e086-124">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="5e086-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="5e086-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e086-125">Remarks</span></span>

<span data-ttu-id="5e086-126">El acceso a la clase de [**\_ teclado MSVM**](msvm-keyboard.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="5e086-126">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5e086-127">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5e086-127">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e086-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e086-128">Requirements</span></span>



| <span data-ttu-id="5e086-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e086-129">Requirement</span></span> | <span data-ttu-id="5e086-130">Value</span><span class="sxs-lookup"><span data-stu-id="5e086-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e086-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e086-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5e086-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e086-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5e086-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e086-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5e086-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e086-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e086-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5e086-135">Namespace</span></span><br/>                | <span data-ttu-id="5e086-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5e086-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5e086-137">MOF</span><span class="sxs-lookup"><span data-stu-id="5e086-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e086-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e086-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e086-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e086-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e086-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5e086-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5e086-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e086-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e086-142">**\_Teclado MSVM**</span><span class="sxs-lookup"><span data-stu-id="5e086-142">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

