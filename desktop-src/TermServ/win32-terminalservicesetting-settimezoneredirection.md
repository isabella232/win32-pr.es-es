---
title: Método SetTimeZoneRedirection de la clase Win32_TerminalServiceSetting
description: El método SetTimeZoneRedirection establece la propiedad TimeZoneRedirection, que permite al equipo cliente redirigir su configuración de zona horaria a la sesión de Servicios de Escritorio remoto.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- Método SetTimeZoneRedirection Servicios de Escritorio remoto
- Método SetTimeZoneRedirection Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetTimeZoneRedirection
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetTimeZoneRedirection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2761567c724abf129ac881188bc468b228d7fd11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676725"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="27631-106">Método SetTimeZoneRedirection de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="27631-106">SetTimeZoneRedirection method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="27631-107">El método **SetTimeZoneRedirection** establece la propiedad **TimeZoneRedirection** , que permite al equipo cliente redirigir su configuración de zona horaria a la sesión de servicios de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="27631-107">The **SetTimeZoneRedirection** method sets the **TimeZoneRedirection** property, which allows the client computer to redirect its time zone settings to the Remote Desktop Services session.</span></span>

## <a name="syntax"></a><span data-ttu-id="27631-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27631-108">Syntax</span></span>


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a><span data-ttu-id="27631-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27631-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27631-110">*TimeZoneRedirection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27631-110">*TimeZoneRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27631-111">Nuevo valor de la propiedad **TimeZoneRedirection** .</span><span class="sxs-lookup"><span data-stu-id="27631-111">The new value for the **TimeZoneRedirection** property.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="27631-112"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="27631-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="27631-113">Deshabilita la propiedad **TimeZoneRedirection** .</span><span class="sxs-lookup"><span data-stu-id="27631-113">Disables the **TimeZoneRedirection** property.</span></span> <span data-ttu-id="27631-114">No se produce la redirección de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="27631-114">No time zone redirection occurs.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="27631-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="27631-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="27631-116">Habilita la propiedad **TimeZoneRedirection** .</span><span class="sxs-lookup"><span data-stu-id="27631-116">Enables the **TimeZoneRedirection** property.</span></span> <span data-ttu-id="27631-117">La zona horaria del cliente se redirige a la zona horaria de la sesión.</span><span class="sxs-lookup"><span data-stu-id="27631-117">The client's time zone is redirected to the session's time zone.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27631-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27631-118">Return value</span></span>

<span data-ttu-id="27631-119">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="27631-119">Returns 0 on success; otherwise returns a WMI error code.</span></span> <span data-ttu-id="27631-120">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="27631-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="27631-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27631-121">Remarks</span></span>

<span data-ttu-id="27631-122">De forma predeterminada, la zona horaria de la sesión Servicios de Escritorio remoto es la misma que la zona horaria del servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="27631-122">By default, the time zone for the Remote Desktop Services session is the same as the time zone for the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="27631-123">Los equipos cliente no pueden redirigir la información de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="27631-123">Client computers cannot redirect time zone information.</span></span>

<span data-ttu-id="27631-124">Si se deshabilita la redirección de zona horaria, las nuevas sesiones heredan la zona horaria del servidor.</span><span class="sxs-lookup"><span data-stu-id="27631-124">If time zone redirection is disabled, new sessions inherit the server time zone.</span></span> <span data-ttu-id="27631-125">Cuando una sesión se vuelve a conectar, la sesión conserva la zona horaria que tenía antes de la desconexión.</span><span class="sxs-lookup"><span data-stu-id="27631-125">When a session reconnects, the session retains the time zone it had prior to disconnecting.</span></span>

<span data-ttu-id="27631-126">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="27631-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="27631-127">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="27631-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="27631-128">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="27631-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="27631-129">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="27631-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="27631-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27631-130">Requirements</span></span>



| <span data-ttu-id="27631-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="27631-131">Requirement</span></span> | <span data-ttu-id="27631-132">Value</span><span class="sxs-lookup"><span data-stu-id="27631-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27631-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27631-133">Minimum supported client</span></span><br/> | <span data-ttu-id="27631-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27631-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27631-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27631-135">Minimum supported server</span></span><br/> | <span data-ttu-id="27631-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27631-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27631-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="27631-137">Namespace</span></span><br/>                | <span data-ttu-id="27631-138">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="27631-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="27631-139">MOF</span><span class="sxs-lookup"><span data-stu-id="27631-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27631-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27631-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="27631-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27631-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27631-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27631-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27631-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="27631-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27631-144">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="27631-144">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

