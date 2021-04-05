---
description: Simula una secuencia de teclas de la versión de lanzamiento.
ms.assetid: 4166BA71-315D-41BD-857C-48AFB702911E
title: Método TypeKey de la clase Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1b978da48600cc52472ab8bdec011ddbaa5ff624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002786"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="b8773-103">Método TypeKey de la \_ clase de teclado MSVM</span><span class="sxs-lookup"><span data-stu-id="b8773-103">TypeKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="b8773-104">Simula una secuencia de teclas de la versión de lanzamiento.</span><span class="sxs-lookup"><span data-stu-id="b8773-104">Simulates a press-release key sequence.</span></span> <span data-ttu-id="b8773-105">Esto es equivalente a llamar a [**PressKey**](presskey-msvm-keyboard.md) seguido de [**ReleaseKey**](releasekey-msvm-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="b8773-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8773-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8773-106">Syntax</span></span>


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="b8773-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8773-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8773-108">*KeyCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8773-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8773-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8773-109">Type: **uint32**</span></span>

<span data-ttu-id="b8773-110">Código de tecla virtual de la tecla que se va a presionar.</span><span class="sxs-lookup"><span data-stu-id="b8773-110">The virtual key code of the key to press.</span></span> <span data-ttu-id="b8773-111">Para obtener la lista de códigos de tecla virtual, consulte [**códigos de tecla virtual**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b8773-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8773-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8773-112">Return value</span></span>

<span data-ttu-id="b8773-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8773-113">Type: **uint32**</span></span>

<span data-ttu-id="b8773-114">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b8773-114">A return value of zero indicates success.</span></span> <span data-ttu-id="b8773-115">Un valor distinto de cero indica un error al modificar el estado de la clave.</span><span class="sxs-lookup"><span data-stu-id="b8773-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="b8773-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="b8773-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b8773-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b8773-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b8773-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="b8773-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b8773-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="b8773-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b8773-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="b8773-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b8773-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="b8773-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b8773-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="b8773-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b8773-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b8773-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b8773-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b8773-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b8773-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="b8773-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b8773-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b8773-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b8773-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="b8773-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b8773-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b8773-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b8773-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8773-129">Remarks</span></span>

<span data-ttu-id="b8773-130">El acceso a la clase de [**\_ teclado MSVM**](msvm-keyboard.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="b8773-130">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b8773-131">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b8773-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8773-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8773-132">Requirements</span></span>



| <span data-ttu-id="b8773-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8773-133">Requirement</span></span> | <span data-ttu-id="b8773-134">Value</span><span class="sxs-lookup"><span data-stu-id="b8773-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8773-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8773-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b8773-136">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8773-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b8773-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8773-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b8773-138">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8773-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8773-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8773-139">Namespace</span></span><br/>                | <span data-ttu-id="b8773-140">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b8773-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b8773-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b8773-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8773-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8773-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8773-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8773-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8773-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8773-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b8773-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8773-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8773-146">**\_Teclado MSVM**</span><span class="sxs-lookup"><span data-stu-id="b8773-146">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="b8773-147">**Códigos de tecla virtual**</span><span class="sxs-lookup"><span data-stu-id="b8773-147">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

