---
title: Método Create de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Crea una directiva de autorización de conexión Escritorio remoto (RD \ 160; CAP) usando los valores especificados. El nuevo RD \ 160; El límite se insertará en la parte superior de la RD \ 160; Orden de evaluación CAP, con un valor de propiedad order de \ 0034; 1 \ 0034;.
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- Crear método Servicios de Escritorio remoto
- Create Method Servicios de Escritorio remoto, Win32_TSGatewayConnectionAuthorizationPolicy (clase)
- Win32_TSGatewayConnectionAuthorizationPolicy Servicios de Escritorio remoto de clase, Create (método)
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc027c2f7fc90318bd1af6fd1254077a860a5d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079037"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="fba48-107">Método Create de la \_ clase Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="fba48-107">Create method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="fba48-108">Crea una directiva de autorización de conexión Escritorio remoto (CAP de RD) mediante los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="fba48-108">Creates a Remote Desktop connection authorization policy (RD CAP) by using the specified values.</span></span> <span data-ttu-id="fba48-109">La nueva CAP de RD se insertará en la parte superior del orden de evaluación de CAP de RD, con un valor de propiedad **Order** de "1".</span><span class="sxs-lookup"><span data-stu-id="fba48-109">The new RD CAP will be inserted at the top of the RD CAP evaluation order, with an **Order** property value of "1".</span></span>

## <a name="syntax"></a><span data-ttu-id="fba48-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fba48-110">Syntax</span></span>


```mof
uint32 Create(
  [in] string  Name,
  [in] string  UserGroupNames,
  [in] string  ComputerGroupNames,
  [in] boolean SmartCard,
  [in] boolean Password,
  [in] boolean SecureId,
  [in] boolean Enabled,
  [in] uint32  DeviceRedirectionType,
  [in] boolean DiskDrivesDisabled,
  [in] boolean PrintersDisabled,
  [in] boolean SerialPortsDisabled,
  [in] boolean ClipboardDisabled,
  [in] boolean PlugAndPlayDevicesDisabled,
  [in] uint32  IdleTimeout,
  [in] uint32  SessionTimeout,
  [in] uint32  SessionTimeoutAction,
  [in] boolean AllowOnlySDRServers,
  [in] boolean CookieAuthentication
);
```



## <a name="parameters"></a><span data-ttu-id="fba48-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fba48-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba48-112">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-113">Nombre de la CAP de RD.</span><span class="sxs-lookup"><span data-stu-id="fba48-113">Name of the RD CAP.</span></span> <span data-ttu-id="fba48-114">El nombre debe tener 64 caracteres o menos, único (se omite el caso) y no puede contener los siguientes caracteres reservados:</span><span class="sxs-lookup"><span data-stu-id="fba48-114">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="fba48-115"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="fba48-115"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="fba48-116">\*\[Pestaña\]</span><span class="sxs-lookup"><span data-stu-id="fba48-116">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="fba48-117">*UserGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-117">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-118">Lista de nombres de grupos de usuarios, separados por punto y coma, para la nueva CAP de RD.</span><span class="sxs-lookup"><span data-stu-id="fba48-118">List of user group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="fba48-119">*ComputerGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-120">Lista de nombres de grupos de equipos, separados por punto y coma, para la nueva CAP de RD.</span><span class="sxs-lookup"><span data-stu-id="fba48-120">List of computer group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="fba48-121">*Tarjeta inteligente* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-121">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-122">Especifica si las tarjetas inteligentes se pueden usar para autenticarse con el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fba48-122">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="fba48-123">*Contraseña* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-123">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-124">Especifica si las contraseñas se pueden usar para autenticarse con el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fba48-124">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="fba48-125">*SecureId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-125">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-126">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="fba48-126">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="fba48-127">*Habilitado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-127">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-128">Especifica si esta CAP de RD está habilitada.</span><span class="sxs-lookup"><span data-stu-id="fba48-128">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="fba48-129">*DeviceRedirectionType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-129">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-130">Especifica los tipos de dispositivos que se redirigirán.</span><span class="sxs-lookup"><span data-stu-id="fba48-130">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="fba48-131">0</span><span class="sxs-lookup"><span data-stu-id="fba48-131">0</span></span>
</dt> <dd>

<span data-ttu-id="fba48-132">Se redirigirán todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fba48-132">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="fba48-133">1</span><span class="sxs-lookup"><span data-stu-id="fba48-133">1</span></span>
</dt> <dd>

<span data-ttu-id="fba48-134">No se redirigirá ningún dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fba48-134">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="fba48-135">2</span><span class="sxs-lookup"><span data-stu-id="fba48-135">2</span></span>
</dt> <dd>

<span data-ttu-id="fba48-136">Los dispositivos especificados no se redirigirán.</span><span class="sxs-lookup"><span data-stu-id="fba48-136">Specified devices will not be redirected.</span></span> <span data-ttu-id="fba48-137">Los parámetros *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled* y *PlugAndPlayDevicesDisabled* controlan qué dispositivos no se redirigirán.</span><span class="sxs-lookup"><span data-stu-id="fba48-137">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fba48-138">*DiskDrivesDisabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-138">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-139">Especifica si se va a deshabilitar la redirección de la unidad de disco si el parámetro *DeviceRedirectionType* es "2".</span><span class="sxs-lookup"><span data-stu-id="fba48-139">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="fba48-140">*PrintersDisabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-140">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-141">Especifica si se va a deshabilitar la redirección de impresora si el parámetro *DeviceRedirectionType* es "2".</span><span class="sxs-lookup"><span data-stu-id="fba48-141">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="fba48-142">*SerialPortsDisabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-142">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-143">Especifica si se va a deshabilitar la redirección de puertos serie si el parámetro *DeviceRedirectionType* es "2".</span><span class="sxs-lookup"><span data-stu-id="fba48-143">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="fba48-144">*ClipboardDisabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-144">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-145">Especifica si se va a deshabilitar la redirección del portapapeles si el parámetro *DeviceRedirectionType* es "2".</span><span class="sxs-lookup"><span data-stu-id="fba48-145">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="fba48-146">*PlugAndPlayDevicesDisabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-146">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-147">Especifica si se va a deshabilitar la redirección de dispositivos Plug and Play si el parámetro *DeviceRedirectionType* es "2".</span><span class="sxs-lookup"><span data-stu-id="fba48-147">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="fba48-148">*IdleTimeout* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-148">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-149">Valor de tiempo de espera de inactividad en minutos</span><span class="sxs-lookup"><span data-stu-id="fba48-149">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="fba48-150">*SessionTimeout* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-150">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-151">Valor de tiempo de espera de sesión en minutos</span><span class="sxs-lookup"><span data-stu-id="fba48-151">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="fba48-152">*SessionTimeoutAction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-152">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-153">Acción de tiempo de espera de sesión en minutos</span><span class="sxs-lookup"><span data-stu-id="fba48-153">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="fba48-154">*AllowOnlySDRServers* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-154">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-155">Si las conexiones solo se permiten a los servidores SDR TS</span><span class="sxs-lookup"><span data-stu-id="fba48-155">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="fba48-156">*CookieAuthentication* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba48-156">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba48-157">Indica si se puede usar la autenticación de cookies para conectarse al servidor de puerta de enlace de TS</span><span class="sxs-lookup"><span data-stu-id="fba48-157">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba48-158">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fba48-158">Return value</span></span>

<span data-ttu-id="fba48-159">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="fba48-159">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fba48-160">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="fba48-160">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fba48-161">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fba48-161">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fba48-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fba48-162">Remarks</span></span>

<span data-ttu-id="fba48-163">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="fba48-163">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fba48-164">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fba48-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fba48-165">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fba48-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fba48-166">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="fba48-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fba48-167">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fba48-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fba48-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fba48-168">Requirements</span></span>



| <span data-ttu-id="fba48-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="fba48-169">Requirement</span></span> | <span data-ttu-id="fba48-170">Value</span><span class="sxs-lookup"><span data-stu-id="fba48-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fba48-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fba48-171">Minimum supported client</span></span><br/> | <span data-ttu-id="fba48-172">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fba48-172">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fba48-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fba48-173">Minimum supported server</span></span><br/> | <span data-ttu-id="fba48-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fba48-174">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fba48-175">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fba48-175">Namespace</span></span><br/>                | <span data-ttu-id="fba48-176">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fba48-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fba48-177">MOF</span><span class="sxs-lookup"><span data-stu-id="fba48-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fba48-178"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fba48-178"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fba48-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fba48-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fba48-180"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fba48-180"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fba48-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="fba48-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba48-182">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="fba48-182">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

