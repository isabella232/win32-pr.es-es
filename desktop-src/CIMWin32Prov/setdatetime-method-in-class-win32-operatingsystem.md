---
description: SetDateTime&\# 8194; El método de clase WMI establece la hora actual del sistema en el equipo.
ms.assetid: b9b86a52-c3d7-489d-8632-b297970dbeac
ms.tgt_platform: multiple
title: Método SetDateTime de la clase Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.SetDateTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60316904d58ffec38aa912a1454082e7edfae5a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659392"
---
# <a name="setdatetime-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="3121e-103">Método SetDateTime de la \_ clase Win32 OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3121e-103">SetDateTime method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="3121e-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDateTime** establece la hora actual del sistema en el equipo.</span><span class="sxs-lookup"><span data-stu-id="3121e-104">The **SetDateTime** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the current system time on the computer.</span></span>

<span data-ttu-id="3121e-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3121e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3121e-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3121e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3121e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3121e-107">Syntax</span></span>


```mof
uint32 SetDateTime(
  [in] datetime LocalDatetime
);
```



## <a name="parameters"></a><span data-ttu-id="3121e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3121e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3121e-109">*LocalDatetime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3121e-109">*LocalDatetime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3121e-110">Valor de la hora actual.</span><span class="sxs-lookup"><span data-stu-id="3121e-110">Value of the current time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3121e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3121e-111">Return value</span></span>

<span data-ttu-id="3121e-112">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3121e-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="3121e-113">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="3121e-113">Any other number indicates an error.</span></span> <span data-ttu-id="3121e-114">Para ver los códigos de error, consulte [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3121e-114">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3121e-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3121e-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3121e-116">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="3121e-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3121e-117">**Otro** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="3121e-117">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="3121e-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3121e-118">Remarks</span></span>

<span data-ttu-id="3121e-119">El proceso de llamada debe tener el \_ privilegio de nombre SYSTEMTIME de se \_ .</span><span class="sxs-lookup"><span data-stu-id="3121e-119">The calling process must have the SE\_SYSTEMTIME\_NAME privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="3121e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3121e-120">Requirements</span></span>



| <span data-ttu-id="3121e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3121e-121">Requirement</span></span> | <span data-ttu-id="3121e-122">Value</span><span class="sxs-lookup"><span data-stu-id="3121e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3121e-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3121e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3121e-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3121e-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3121e-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3121e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3121e-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3121e-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3121e-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3121e-127">Namespace</span></span><br/>                | <span data-ttu-id="3121e-128">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3121e-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3121e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="3121e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3121e-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3121e-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3121e-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3121e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3121e-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3121e-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3121e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3121e-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="3121e-134">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3121e-134">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3121e-135">**OperatingSystem de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="3121e-135">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="3121e-136">Tareas WMI: administración de escritorio</span><span class="sxs-lookup"><span data-stu-id="3121e-136">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

