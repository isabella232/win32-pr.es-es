---
title: Método ConnectionSettings de la clase Win32_TSClientSetting
description: El método ConnectionSettings establece la configuración de sesión que se aplica a la conexión y al proceso de inicio de sesión.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- Método ConnectionSettings Servicios de Escritorio remoto
- Método ConnectionSettings Servicios de Escritorio remoto, clase Win32_TSClientSetting
- Win32_TSClientSetting de clase Servicios de Escritorio remoto, método ConnectionSettings
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec255f00656684751b750e92d7a3df8290e3573e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534060"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="a4e1a-106">Método ConnectionSettings de la \_ clase TSClientSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="a4e1a-106">ConnectionSettings method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="a4e1a-107">El método **ConnectionSettings** establece la configuración de sesión que se aplica a la conexión y al proceso de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-107">The **ConnectionSettings** method sets the session settings that apply to the connection and logon process.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4e1a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4e1a-108">Syntax</span></span>


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="a4e1a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4e1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4e1a-110">*ConnectClientDrivesAtLogon* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4e1a-110">*ConnectClientDrivesAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4e1a-111">Marca que habilita o deshabilita la propiedad **ConnectClientDrivesAtLogon** , que especifica si las unidades del cliente se conectan automáticamente durante el procedimiento de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-111">Flag enabling or disabling the **ConnectClientDrivesAtLogon** property which specifies whether the client's drives are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a4e1a-112"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="a4e1a-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a4e1a-113">Las unidades del cliente no se conectan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-113">The client's drives are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="a4e1a-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="a4e1a-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="a4e1a-115">Las unidades del cliente se conectan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-115">The client's drives are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a4e1a-116">*ConnectPrinterAtLogon* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4e1a-116">*ConnectPrinterAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4e1a-117">Marca que habilita o deshabilita la propiedad **ConnectPrinterAtLogon** , que especifica si todas las impresoras de cliente local asignadas se conectan automáticamente durante el procedimiento de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-117">Flag enabling or disabling the **ConnectPrinterAtLogon** property, which specifies whether all mapped local client printers are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a4e1a-118"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="a4e1a-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a4e1a-119">Todas las impresoras locales asignadas no se conectan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-119">All mapped local printers are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="a4e1a-120"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="a4e1a-120"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="a4e1a-121">Todas las impresoras locales asignadas se conectan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-121">All mapped local printers are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a4e1a-122">*DefaultToClientPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4e1a-122">*DefaultToClientPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4e1a-123">Marca que habilita o deshabilita la propiedad **DefaultToClientPrinter** , que especifica si los trabajos de impresión se envían automáticamente a la impresora local del cliente.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-123">Flag enabling or disabling the **DefaultToClientPrinter** property which specifies whether print jobs are automatically sent to the client's local printer.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a4e1a-124"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="a4e1a-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a4e1a-125">Los trabajos de impresión no se envían automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-125">Print jobs are not automatically sent.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="a4e1a-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="a4e1a-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="a4e1a-127">Los trabajos de impresión se envían automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-127">Print jobs are automatically sent.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4e1a-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4e1a-128">Return value</span></span>

<span data-ttu-id="a4e1a-129">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-129">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a4e1a-130">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="a4e1a-131">El método devuelve un error si el servidor invalida la configuración de conexión del usuario.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-131">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4e1a-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4e1a-132">Remarks</span></span>

<span data-ttu-id="a4e1a-133">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a4e1a-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a4e1a-134">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a4e1a-135">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a4e1a-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a4e1a-136">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a4e1a-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4e1a-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4e1a-137">Requirements</span></span>



| <span data-ttu-id="a4e1a-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4e1a-138">Requirement</span></span> | <span data-ttu-id="a4e1a-139">Value</span><span class="sxs-lookup"><span data-stu-id="a4e1a-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e1a-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4e1a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a4e1a-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4e1a-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4e1a-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4e1a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a4e1a-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4e1a-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4e1a-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a4e1a-144">Namespace</span></span><br/>                | <span data-ttu-id="a4e1a-145">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a4e1a-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a4e1a-146">MOF</span><span class="sxs-lookup"><span data-stu-id="a4e1a-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4e1a-147"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4e1a-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4e1a-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a4e1a-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4e1a-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4e1a-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4e1a-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4e1a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e1a-151">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="a4e1a-151">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

