---
description: Inicia el depurador actualmente registrado para este proceso.
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: Método AttachDebugger de la clase Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 041bdeeab634ebed5c7ec2eccffe01f7cecce709
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907050"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a><span data-ttu-id="c0f5a-103">Método AttachDebugger de la \_ clase Process de Win32</span><span class="sxs-lookup"><span data-stu-id="c0f5a-103">AttachDebugger method of the Win32\_Process class</span></span>

<span data-ttu-id="c0f5a-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AttachDebugger** inicia el depurador actualmente registrado para este proceso.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-104">The **AttachDebugger** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method starts the debugger that is currently registered for this process.</span></span>

<span data-ttu-id="c0f5a-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c0f5a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c0f5a-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c0f5a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f5a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0f5a-107">Syntax</span></span>


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a><span data-ttu-id="c0f5a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0f5a-108">Parameters</span></span>

<span data-ttu-id="c0f5a-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0f5a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0f5a-110">Return value</span></span>

<span data-ttu-id="c0f5a-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="c0f5a-112">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c0f5a-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c0f5a-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c0f5a-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c0f5a-114">**Completado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="c0f5a-115">0</span><span class="sxs-lookup"><span data-stu-id="c0f5a-115">0</span></span>

<span data-ttu-id="c0f5a-116">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="c0f5a-117">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="c0f5a-118">2</span><span class="sxs-lookup"><span data-stu-id="c0f5a-118">2</span></span>

<span data-ttu-id="c0f5a-119">El usuario no tiene acceso a la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-119">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="c0f5a-120">**Privilegio insuficiente**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="c0f5a-121">3</span><span class="sxs-lookup"><span data-stu-id="c0f5a-121">3</span></span>

<span data-ttu-id="c0f5a-122">El usuario no tiene privilegios suficientes.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="c0f5a-123">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="c0f5a-124">8</span><span class="sxs-lookup"><span data-stu-id="c0f5a-124">8</span></span>

<span data-ttu-id="c0f5a-125">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="c0f5a-126">**No se encuentra la ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="c0f5a-127">9</span><span class="sxs-lookup"><span data-stu-id="c0f5a-127">9</span></span>

<span data-ttu-id="c0f5a-128">La ruta especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="c0f5a-129">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c0f5a-130">21</span><span class="sxs-lookup"><span data-stu-id="c0f5a-130">21</span></span>

<span data-ttu-id="c0f5a-131">El parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-131">The specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c0f5a-132">**Otros**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c0f5a-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="c0f5a-133">22 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0f5a-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0f5a-134">Requirements</span></span>



| <span data-ttu-id="c0f5a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0f5a-135">Requirement</span></span> | <span data-ttu-id="c0f5a-136">Value</span><span class="sxs-lookup"><span data-stu-id="c0f5a-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f5a-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0f5a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f5a-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0f5a-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0f5a-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0f5a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f5a-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0f5a-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0f5a-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c0f5a-141">Namespace</span></span><br/>                | <span data-ttu-id="c0f5a-142">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c0f5a-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c0f5a-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c0f5a-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0f5a-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0f5a-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0f5a-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c0f5a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0f5a-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0f5a-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0f5a-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0f5a-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="c0f5a-148">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0f5a-148">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c0f5a-149">**\_Proceso Win32**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

