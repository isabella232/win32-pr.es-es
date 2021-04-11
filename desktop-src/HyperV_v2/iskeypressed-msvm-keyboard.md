---
description: Recupera el estado de clave de una clave.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Método IsKeyPressed de la clase Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.IsKeyPressed
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 44af7a3dc82c0d4d20a2e4c6aff21f7a47837490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275937"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="5281f-103">Método IsKeyPressed de la \_ clase de teclado MSVM</span><span class="sxs-lookup"><span data-stu-id="5281f-103">IsKeyPressed method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="5281f-104">Recupera el estado de clave de una clave.</span><span class="sxs-lookup"><span data-stu-id="5281f-104">Retrieves the key state of a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="5281f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5281f-105">Syntax</span></span>


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a><span data-ttu-id="5281f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5281f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5281f-107">*KeyCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5281f-107">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5281f-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5281f-108">Type: **uint32**</span></span>

<span data-ttu-id="5281f-109">Código de tecla virtual de la clave que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="5281f-109">The virtual key code of the key to query.</span></span> <span data-ttu-id="5281f-110">Para obtener la lista de códigos de tecla virtual, consulte [**códigos de tecla virtual**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5281f-110">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="5281f-111">*keyState* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5281f-111">*keyState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5281f-112">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5281f-112">Type: **boolean**</span></span>

<span data-ttu-id="5281f-113">El estado actual de la clave.</span><span class="sxs-lookup"><span data-stu-id="5281f-113">The current down state of the key.</span></span> <span data-ttu-id="5281f-114">Un valor **true** significa que la tecla está inactiva.</span><span class="sxs-lookup"><span data-stu-id="5281f-114">A **True** value means the key is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5281f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5281f-115">Return value</span></span>

<span data-ttu-id="5281f-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5281f-116">Type: **uint32**</span></span>

<span data-ttu-id="5281f-117">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5281f-117">A return value of zero indicates success.</span></span> <span data-ttu-id="5281f-118">Un valor distinto de cero indica un error al consultar el estado de la clave.</span><span class="sxs-lookup"><span data-stu-id="5281f-118">A nonzero value indicates a failure to query the key state.</span></span>

<dl> <dt>

<span data-ttu-id="5281f-119">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="5281f-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5281f-120">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="5281f-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5281f-121">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="5281f-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5281f-122">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="5281f-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5281f-123">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="5281f-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5281f-124">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="5281f-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5281f-125">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="5281f-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5281f-126">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="5281f-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5281f-127">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="5281f-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5281f-128">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="5281f-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5281f-129">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="5281f-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5281f-130">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="5281f-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5281f-131">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="5281f-131">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="5281f-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5281f-132">Remarks</span></span>

<span data-ttu-id="5281f-133">El método **IsKeyPressed** siempre devolverá **false** para **el \_ menú VK** (18), el **\_ control VK** (17) y el **\_ desplazamiento de VK** (16) porque no son claves reales en un teclado.</span><span class="sxs-lookup"><span data-stu-id="5281f-133">The **IsKeyPressed** method will always return **False** for the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) because these are not real keys on a keyboard.</span></span> <span data-ttu-id="5281f-134">Estos códigos de tecla virtual siempre se asignan a **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) y **VK \_ LSHIFT** (160), respectivamente, por los métodos [**PressKey**](presskey-msvm-keyboard.md) y [**ReleaseKey**](releasekey-msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="5281f-134">These virtual key codes are always mapped to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, by the [**PressKey**](presskey-msvm-keyboard.md) and [**ReleaseKey**](releasekey-msvm-keyboard.md) methods.</span></span>

<span data-ttu-id="5281f-135">El acceso a la clase de [**\_ teclado MSVM**](msvm-keyboard.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="5281f-135">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5281f-136">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5281f-136">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5281f-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5281f-137">Requirements</span></span>



| <span data-ttu-id="5281f-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="5281f-138">Requirement</span></span> | <span data-ttu-id="5281f-139">Value</span><span class="sxs-lookup"><span data-stu-id="5281f-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5281f-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5281f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5281f-141">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="5281f-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5281f-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5281f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5281f-143">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="5281f-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5281f-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5281f-144">Namespace</span></span><br/>                | <span data-ttu-id="5281f-145">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5281f-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5281f-146">MOF</span><span class="sxs-lookup"><span data-stu-id="5281f-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5281f-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5281f-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5281f-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5281f-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5281f-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5281f-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5281f-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="5281f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5281f-151">**\_Teclado MSVM**</span><span class="sxs-lookup"><span data-stu-id="5281f-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="5281f-152">**Códigos de tecla virtual**</span><span class="sxs-lookup"><span data-stu-id="5281f-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

