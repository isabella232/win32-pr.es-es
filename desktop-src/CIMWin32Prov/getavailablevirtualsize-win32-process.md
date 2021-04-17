---
description: Recupera el tamaño actual, en bytes, del espacio de direcciones virtuales libre disponible para el proceso.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Método GetAvailableVirtualSize de la clase Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ee6e798b8df32822de481f3af1dc6b21a81d1024
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659482"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a><span data-ttu-id="eb024-103">Método GetAvailableVirtualSize de la \_ clase Process de Win32</span><span class="sxs-lookup"><span data-stu-id="eb024-103">GetAvailableVirtualSize method of the Win32\_Process class</span></span>

<span data-ttu-id="eb024-104">Recupera el tamaño actual, en bytes, del espacio de direcciones virtuales libre disponible para el proceso.</span><span class="sxs-lookup"><span data-stu-id="eb024-104">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb024-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb024-105">Syntax</span></span>


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a><span data-ttu-id="eb024-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb024-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb024-107">*AvailableVirtualSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="eb024-107">*AvailableVirtualSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb024-108">El parámetro *AvailableVirtualSize* devuelve el espacio de direcciones virtuales disponible para este proceso.</span><span class="sxs-lookup"><span data-stu-id="eb024-108">The *AvailableVirtualSize* parameter returns the free virtual address space available to this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb024-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb024-109">Return value</span></span>

<span data-ttu-id="eb024-110">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="eb024-110">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="eb024-111">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="eb024-111">Any other number indicates an error.</span></span> <span data-ttu-id="eb024-112">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="eb024-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="eb024-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="eb024-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="eb024-114">**Completado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="eb024-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="eb024-115">0</span><span class="sxs-lookup"><span data-stu-id="eb024-115">0</span></span>

<span data-ttu-id="eb024-116">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="eb024-116">The operation completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="eb024-117">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="eb024-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="eb024-118">2</span><span class="sxs-lookup"><span data-stu-id="eb024-118">2</span></span>

<span data-ttu-id="eb024-119">El usuario no tiene acceso a la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="eb024-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="eb024-120">**Privilegio insuficiente**</span><span class="sxs-lookup"><span data-stu-id="eb024-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="eb024-121">3</span><span class="sxs-lookup"><span data-stu-id="eb024-121">3</span></span>

<span data-ttu-id="eb024-122">El usuario no tiene privilegios suficientes.</span><span class="sxs-lookup"><span data-stu-id="eb024-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="eb024-123">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="eb024-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="eb024-124">8</span><span class="sxs-lookup"><span data-stu-id="eb024-124">8</span></span>

<span data-ttu-id="eb024-125">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="eb024-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="eb024-126">**No se encuentra la ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="eb024-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="eb024-127">9</span><span class="sxs-lookup"><span data-stu-id="eb024-127">9</span></span>

<span data-ttu-id="eb024-128">La ruta especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="eb024-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="eb024-129">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="eb024-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="eb024-130">21</span><span class="sxs-lookup"><span data-stu-id="eb024-130">21</span></span>

<span data-ttu-id="eb024-131">El parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="eb024-131">The specified parameter is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="eb024-132">**Otros**</span><span class="sxs-lookup"><span data-stu-id="eb024-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="eb024-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="eb024-133">22 4294967295</span></span>

<span data-ttu-id="eb024-134">Para valores distintos de los enumerados, consulte la documentación de [códigos de error del sistema](/windows/desktop/Debug/system-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="eb024-134">For values other than those listed, refer to the [System Error Codes](/windows/desktop/Debug/system-error-codes) documentation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb024-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb024-135">Requirements</span></span>



| <span data-ttu-id="eb024-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb024-136">Requirement</span></span> | <span data-ttu-id="eb024-137">Value</span><span class="sxs-lookup"><span data-stu-id="eb024-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb024-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb024-138">Minimum supported client</span></span><br/> | <span data-ttu-id="eb024-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="eb024-139">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="eb024-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb024-140">Minimum supported server</span></span><br/> | <span data-ttu-id="eb024-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="eb024-141">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="eb024-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb024-142">Namespace</span></span><br/>                | <span data-ttu-id="eb024-143">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="eb024-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb024-144">MOF</span><span class="sxs-lookup"><span data-stu-id="eb024-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb024-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb024-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb024-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eb024-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb024-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb024-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb024-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb024-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb024-149">**\_Proceso Win32**</span><span class="sxs-lookup"><span data-stu-id="eb024-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

