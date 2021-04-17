---
description: GetOwnerSid&\# 8194; El método de clase WMI recupera el identificador de seguridad (SID) del propietario de este proceso.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Método GetOwnerSid de la clase Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3ed34d132d363c0ce9f83511459ec40f340a06c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659476"
---
# <a name="getownersid-method-of-the-win32_process-class"></a><span data-ttu-id="9a573-103">Método GetOwnerSid de la \_ clase Process de Win32</span><span class="sxs-lookup"><span data-stu-id="9a573-103">GetOwnerSid method of the Win32\_Process class</span></span>

<span data-ttu-id="9a573-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwnerSid** recupera el identificador de seguridad (SID) para el propietario de este proceso.</span><span class="sxs-lookup"><span data-stu-id="9a573-104">The **GetOwnerSid** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the security identifier (SID) for the owner of this process.</span></span>

<span data-ttu-id="9a573-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9a573-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9a573-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9a573-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9a573-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a573-107">Syntax</span></span>


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a><span data-ttu-id="9a573-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a573-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a573-109">*SID* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9a573-109">*Sid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a573-110">Devuelve el descriptor de identificador de seguridad para este proceso.</span><span class="sxs-lookup"><span data-stu-id="9a573-110">Returns the security identifier descriptor for this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a573-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a573-111">Return value</span></span>

<span data-ttu-id="9a573-112">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9a573-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="9a573-113">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="9a573-113">Any other number indicates an error.</span></span> <span data-ttu-id="9a573-114">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9a573-114">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9a573-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9a573-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9a573-116">**Finalización correcta** (0)</span><span class="sxs-lookup"><span data-stu-id="9a573-116">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9a573-117">**Acceso denegado** (2)</span><span class="sxs-lookup"><span data-stu-id="9a573-117">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9a573-118">**Privilegios insuficientes** (3)</span><span class="sxs-lookup"><span data-stu-id="9a573-118">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9a573-119">**Error desconocido** (8)</span><span class="sxs-lookup"><span data-stu-id="9a573-119">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9a573-120">**No se encontró la ruta de acceso** (9)</span><span class="sxs-lookup"><span data-stu-id="9a573-120">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9a573-121">**Parámetro no válido** (21)</span><span class="sxs-lookup"><span data-stu-id="9a573-121">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="9a573-122">**Otro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="9a573-122">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="9a573-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9a573-123">Examples</span></span>

<span data-ttu-id="9a573-124">En el ejemplo de código de PowerShell [Buscar el usuario que ha iniciado sesión en un sistema remoto/s versión 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) se consultan equipos remotos para ver quién ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="9a573-124">The [Find the logged on users on a remote system/s version 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) PowerShell code example queries remote machines to see who is logged on.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a573-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a573-125">Requirements</span></span>



| <span data-ttu-id="9a573-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a573-126">Requirement</span></span> | <span data-ttu-id="9a573-127">Value</span><span class="sxs-lookup"><span data-stu-id="9a573-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a573-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a573-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9a573-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a573-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a573-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a573-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9a573-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a573-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a573-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9a573-132">Namespace</span></span><br/>                | <span data-ttu-id="9a573-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9a573-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9a573-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9a573-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a573-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a573-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a573-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a573-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a573-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a573-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a573-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a573-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="9a573-139">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a573-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9a573-140">**\_Proceso Win32**</span><span class="sxs-lookup"><span data-stu-id="9a573-140">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

