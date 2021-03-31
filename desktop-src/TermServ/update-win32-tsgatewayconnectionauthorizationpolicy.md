---
title: Método Update de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Actualiza la Directiva de autorización de conexión Escritorio remoto actual (RD \ 160; CAP).
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- Método Update Servicios de Escritorio remoto
- Método Update Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Servicios de Escritorio remoto de clase Win32_TSGatewayConnectionAuthorizationPolicy, método Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b982030170e954342dc5ff99754dcb89afd0e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079446"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="b5a3f-106">Método Update de la \_ clase Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="b5a3f-106">Update method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="b5a3f-107">Actualiza la Directiva de autorización de conexión Escritorio remoto actual (CAP de RD).</span><span class="sxs-lookup"><span data-stu-id="b5a3f-107">Updates the current Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a3f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5a3f-108">Syntax</span></span>


```mof
uint32 Update(
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



## <a name="parameters"></a><span data-ttu-id="b5a3f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5a3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5a3f-110">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-111">Nombre de la CAP de RD.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-111">Name of the RD CAP.</span></span> <span data-ttu-id="b5a3f-112">El nombre debe tener 64 caracteres o menos, único (se omite el caso) y no puede contener los siguientes caracteres reservados:</span><span class="sxs-lookup"><span data-stu-id="b5a3f-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="b5a3f-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="b5a3f-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="b5a3f-114">\*\[Pestaña\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-114">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-115">*UserGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-115">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-116">Lista de nombres de grupos de usuarios separados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-116">List of semicolon-separated user group names.</span></span> <span data-ttu-id="b5a3f-117">Los nombres tienen el formato *dominio \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-117">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="b5a3f-118">Si el usuario pertenece a uno de estos grupos de usuarios, se le permitirá el acceso al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-118">If the user belongs to any one of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-119">*ComputerGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-120">Lista de nombres de grupos de máquinas separados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-120">List of semicolon-separated machine group names.</span></span> <span data-ttu-id="b5a3f-121">Este valor puede estar vacío.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-121">This value can be empty.</span></span> <span data-ttu-id="b5a3f-122">Los nombres tienen el formato *dominio \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-122">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="b5a3f-123">Si se especifica un valor, el equipo cliente debe pertenecer a uno de estos grupos de equipos para que el usuario tenga acceso al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-123">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-124">*Tarjeta inteligente* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-124">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-125">Especifica si las tarjetas inteligentes se pueden usar para autenticarse con el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-125">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-126">*Contraseña* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-126">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-127">Especifica si las contraseñas se pueden usar para autenticarse con el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-127">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-128">*SecureId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-128">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-129">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-129">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-130">*Habilitado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-130">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-131">Especifica si esta CAP de RD está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-131">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-132">*DeviceRedirectionType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-132">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-133">Especifica los tipos de dispositivos que se redirigirán.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-133">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="b5a3f-134">0</span><span class="sxs-lookup"><span data-stu-id="b5a3f-134">0</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-135">Se redirigirán todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-135">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-136">1</span><span class="sxs-lookup"><span data-stu-id="b5a3f-136">1</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-137">No se redirigirá ningún dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-137">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-138">2</span><span class="sxs-lookup"><span data-stu-id="b5a3f-138">2</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-139">Los dispositivos especificados no se redirigirán.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-139">Specified devices will not be redirected.</span></span> <span data-ttu-id="b5a3f-140">Los parámetros *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled* y *PlugAndPlayDevicesDisabled* controlan qué dispositivos no se redirigirán.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-140">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b5a3f-141">*DiskDrivesDisabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-141">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-142">Especifica si se va a deshabilitar la redirección de la unidad de disco si el parámetro *DeviceRedirectionType* es "2".</span><span class="sxs-lookup"><span data-stu-id="b5a3f-142">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-143">*PrintersDisabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-143">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-144">Especifica si se va a deshabilitar la redirección de impresora si el parámetro *DeviceRedirectionType* es "2".</span><span class="sxs-lookup"><span data-stu-id="b5a3f-144">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-145">*SerialPortsDisabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-145">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-146">Especifica si se va a deshabilitar la redirección de puertos serie si el parámetro *DeviceRedirectionType* es "2".</span><span class="sxs-lookup"><span data-stu-id="b5a3f-146">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-147">*ClipboardDisabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-147">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-148">Especifica si se va a deshabilitar la redirección del portapapeles si el parámetro *DeviceRedirectionType* es "2".</span><span class="sxs-lookup"><span data-stu-id="b5a3f-148">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-149">*PlugAndPlayDevicesDisabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-149">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-150">Especifica si se va a deshabilitar la redirección de dispositivos Plug and Play si el parámetro *DeviceRedirectionType* es "2".</span><span class="sxs-lookup"><span data-stu-id="b5a3f-150">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-151">*IdleTimeout* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-151">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-152">Valor de tiempo de espera de inactividad en minutos</span><span class="sxs-lookup"><span data-stu-id="b5a3f-152">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-153">*SessionTimeout* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-153">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-154">Valor de tiempo de espera de sesión en minutos</span><span class="sxs-lookup"><span data-stu-id="b5a3f-154">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-155">*SessionTimeoutAction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-155">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-156">Acción de tiempo de espera de sesión en minutos</span><span class="sxs-lookup"><span data-stu-id="b5a3f-156">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-157">*AllowOnlySDRServers* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-157">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-158">Si las conexiones solo se permiten a los servidores SDR TS</span><span class="sxs-lookup"><span data-stu-id="b5a3f-158">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="b5a3f-159">*CookieAuthentication* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5a3f-159">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a3f-160">Indica si se puede usar la autenticación de cookies para conectarse al servidor de puerta de enlace de TS</span><span class="sxs-lookup"><span data-stu-id="b5a3f-160">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5a3f-161">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5a3f-161">Return value</span></span>

<span data-ttu-id="b5a3f-162">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-162">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b5a3f-163">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-163">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b5a3f-164">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b5a3f-164">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5a3f-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5a3f-165">Remarks</span></span>

<span data-ttu-id="b5a3f-166">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-166">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b5a3f-167">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b5a3f-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b5a3f-168">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b5a3f-169">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="b5a3f-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b5a3f-170">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b5a3f-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a3f-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5a3f-171">Requirements</span></span>



| <span data-ttu-id="b5a3f-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5a3f-172">Requirement</span></span> | <span data-ttu-id="b5a3f-173">Value</span><span class="sxs-lookup"><span data-stu-id="b5a3f-173">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a3f-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5a3f-174">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a3f-175">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b5a3f-175">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b5a3f-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5a3f-176">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a3f-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5a3f-177">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b5a3f-178">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b5a3f-178">Namespace</span></span><br/>                | <span data-ttu-id="b5a3f-179">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b5a3f-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b5a3f-180">MOF</span><span class="sxs-lookup"><span data-stu-id="b5a3f-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5a3f-181"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5a3f-181"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5a3f-182">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5a3f-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5a3f-183"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5a3f-183"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b5a3f-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5a3f-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a3f-185">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="b5a3f-185">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

