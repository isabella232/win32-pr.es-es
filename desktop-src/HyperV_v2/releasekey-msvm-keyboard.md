---
description: Simula una versión de clave.
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: Método ReleaseKey de la clase Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.ReleaseKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2193a4b78128ff3f65e98b4425528a51f6cf5916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546827"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="f4553-103">Método ReleaseKey de la \_ clase de teclado MSVM</span><span class="sxs-lookup"><span data-stu-id="f4553-103">ReleaseKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="f4553-104">Simula una versión de clave.</span><span class="sxs-lookup"><span data-stu-id="f4553-104">Simulates a key release.</span></span> <span data-ttu-id="f4553-105">Cuando se realice correctamente, la clave estará en estado activo.</span><span class="sxs-lookup"><span data-stu-id="f4553-105">When successful, the key will be in the up state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4553-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4553-106">Syntax</span></span>


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="f4553-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4553-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4553-108">*KeyCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f4553-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4553-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4553-109">Type: **uint32**</span></span>

<span data-ttu-id="f4553-110">Código de tecla virtual de la clave que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="f4553-110">The virtual key code of the key to release.</span></span> <span data-ttu-id="f4553-111">Para obtener la lista de códigos de tecla virtual, consulte [**códigos de tecla virtual**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f4553-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4553-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4553-112">Return value</span></span>

<span data-ttu-id="f4553-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4553-113">Type: **uint32**</span></span>

<span data-ttu-id="f4553-114">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f4553-114">A return value of zero indicates success.</span></span> <span data-ttu-id="f4553-115">Un valor distinto de cero indica un error al modificar el estado de la clave.</span><span class="sxs-lookup"><span data-stu-id="f4553-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="f4553-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="f4553-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f4553-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f4553-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f4553-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="f4553-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f4553-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="f4553-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f4553-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="f4553-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f4553-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="f4553-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f4553-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="f4553-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f4553-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f4553-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f4553-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f4553-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f4553-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="f4553-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f4553-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f4553-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f4553-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="f4553-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f4553-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f4553-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f4553-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4553-129">Remarks</span></span>

<span data-ttu-id="f4553-130">El método **ReleaseKey** asigna referencias a los **\_ menús VK** (18), **VK \_ (** 17) y **VK \_ Shift** (16) a **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) y **VK \_ LSHIFT** (160), respectivamente, ya que el **\_ menú VK**, el **\_ control VK** y los códigos de tecla virtual **\_ Shift de VK** no representan claves reales en un teclado.</span><span class="sxs-lookup"><span data-stu-id="f4553-130">The **ReleaseKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="f4553-131">El acceso a la clase de [**\_ teclado MSVM**](msvm-keyboard.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="f4553-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f4553-132">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f4553-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4553-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4553-133">Requirements</span></span>



| <span data-ttu-id="f4553-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4553-134">Requirement</span></span> | <span data-ttu-id="f4553-135">Value</span><span class="sxs-lookup"><span data-stu-id="f4553-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4553-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4553-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f4553-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4553-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f4553-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4553-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f4553-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4553-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f4553-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f4553-140">Namespace</span></span><br/>                | <span data-ttu-id="f4553-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f4553-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f4553-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f4553-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4553-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4553-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4553-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f4553-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4553-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f4553-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f4553-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4553-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4553-147">**\_Teclado MSVM**</span><span class="sxs-lookup"><span data-stu-id="f4553-147">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="f4553-148">**Códigos de tecla virtual**</span><span class="sxs-lookup"><span data-stu-id="f4553-148">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

