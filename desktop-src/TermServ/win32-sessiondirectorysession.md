---
title: Win32_SessionDirectorySession (clase)
description: Proporciona propiedades para ver las propiedades de una sesión de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectorySession clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionDirectorySession de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba8fdbdffc764c3bdcc1a8f5bc53aa479f318d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422058"
---
# <a name="win32_sessiondirectorysession-class"></a><span data-ttu-id="8c1ca-105">\_Clase Win32 SessionDirectorySession</span><span class="sxs-lookup"><span data-stu-id="8c1ca-105">Win32\_SessionDirectorySession class</span></span>

<span data-ttu-id="8c1ca-106">Proporciona propiedades para ver las propiedades de una sesión de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="8c1ca-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) session.</span></span>

> [!Note]  
> <span data-ttu-id="8c1ca-107">En Windows Server 2008 R2, el nombre de Terminal Services agente de sesión (agente de sesiones de TS) se cambió al agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="8c1ca-108">Estas propiedades se aplican a todos los sistemas operativos compatibles a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8c1ca-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c1ca-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a><span data-ttu-id="8c1ca-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c1ca-110">Members</span></span>

<span data-ttu-id="8c1ca-111">La **clase \_ SessionDirectorySession de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8c1ca-111">The **Win32\_SessionDirectorySession** class has these types of members:</span></span>

-   [<span data-ttu-id="8c1ca-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c1ca-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c1ca-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c1ca-113">Properties</span></span>

<span data-ttu-id="8c1ca-114">La **clase \_ SessionDirectorySession de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-114">The **Win32\_SessionDirectorySession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c1ca-115">**ApplicationType**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-115">**ApplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c1ca-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c1ca-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c1ca-118">Aplicación iniciada con esta sesión.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-118">Application started with this session.</span></span> <span data-ttu-id="8c1ca-119">Es igual que la propiedad **StartProgram** de [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="8c1ca-119">This is the same as the **StartProgram** property of [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c1ca-120">**ColorDepth**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-120">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c1ca-121">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c1ca-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c1ca-123">Profundidad de color de la sesión, medida en bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-123">Color depth of the session, measured in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="8c1ca-124">**CreateTime**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-124">**CreateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c1ca-125">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-125">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c1ca-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c1ca-127">Fecha y hora en que se creó la sesión.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-127">Date and time the session was created.</span></span> <span data-ttu-id="8c1ca-128">Este valor no se restablece cuando una sesión se desconecta y se vuelve a conectar.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-128">This value is not reset when a session is disconnected and reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="8c1ca-129">**DisconnectTime**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-129">**DisconnectTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c1ca-130">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-130">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c1ca-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c1ca-132">Fecha y hora en que se desconectó la sesión (si es aplicable).</span><span class="sxs-lookup"><span data-stu-id="8c1ca-132">Date and time the session was disconnected (if applicable).</span></span>

</dd> <dt>

<span data-ttu-id="8c1ca-133">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-133">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c1ca-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c1ca-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c1ca-136">Nombre de dominio del usuario que inició sesión en esta sesión.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-136">Domain name of the user logged on to this session.</span></span>

</dd> <dt>

<span data-ttu-id="8c1ca-137">**ResolutionHeight**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-137">**ResolutionHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c1ca-138">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c1ca-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c1ca-140">Alto de la sesión, en píxeles, para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-140">Height of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="8c1ca-141">**ResolutionWidth**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-141">**ResolutionWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c1ca-142">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c1ca-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c1ca-144">Ancho de la sesión, en píxeles, para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-144">Width of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="8c1ca-145">**ServerIPAddress**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-145">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c1ca-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c1ca-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c1ca-148">Dirección IP del servidor de agente de conexión a escritorio remoto para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-148">IP address of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="8c1ca-149">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-149">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c1ca-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c1ca-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-152">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c1ca-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8c1ca-153">Nombre del servidor de agente de conexión a escritorio remoto para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-153">Name of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="8c1ca-154">**SessionID**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-154">**SessionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c1ca-155">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c1ca-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-157">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c1ca-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8c1ca-158">IDENTIFICADOR de sesión para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-158">Session ID for this session.</span></span>

</dd> <dt>

<span data-ttu-id="8c1ca-159">**SqlConnectionString**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-159">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c1ca-160">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c1ca-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c1ca-162">Estado de esta sesión.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-162">State of this session.</span></span>

<dt>

<span data-ttu-id="8c1ca-163">0</span><span class="sxs-lookup"><span data-stu-id="8c1ca-163">0</span></span>
</dt> <dd>

<span data-ttu-id="8c1ca-164">La sesión está activa.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-164">The session is active.</span></span>

</dd> <dt>

<span data-ttu-id="8c1ca-165">1</span><span class="sxs-lookup"><span data-stu-id="8c1ca-165">1</span></span>
</dt> <dd>

<span data-ttu-id="8c1ca-166">La sesión está desconectada.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-166">The session is disconnected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c1ca-167">**TSProtocol**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-167">**TSProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c1ca-168">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c1ca-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c1ca-170">Protocolo para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-170">Protocol for this session.</span></span>

<dt>

<span data-ttu-id="8c1ca-171">0</span><span class="sxs-lookup"><span data-stu-id="8c1ca-171">0</span></span>
</dt> <dd>

<span data-ttu-id="8c1ca-172">Esta sesión se está ejecutando en una consola física.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-172">This session is running on a physical console.</span></span>

</dd> <dt>

<span data-ttu-id="8c1ca-173">1</span><span class="sxs-lookup"><span data-stu-id="8c1ca-173">1</span></span>
</dt> <dd>

<span data-ttu-id="8c1ca-174">Para esta sesión se utiliza un protocolo de terceros propietario.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-174">A proprietary third-party protocol is used for this session.</span></span>

</dd> <dt>

<span data-ttu-id="8c1ca-175">2</span><span class="sxs-lookup"><span data-stu-id="8c1ca-175">2</span></span>
</dt> <dd>

<span data-ttu-id="8c1ca-176">Protocolo de escritorio remoto (RDP) se usa para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-176">Remote Desktop Protocol (RDP) is used for this session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c1ca-177">**UserName**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-177">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c1ca-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c1ca-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c1ca-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c1ca-180">Nombre de usuario del usuario que inició sesión en esta sesión.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-180">User name of the user logged on to this session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c1ca-181">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c1ca-181">Remarks</span></span>

<span data-ttu-id="8c1ca-182">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8c1ca-182">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8c1ca-183">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-183">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8c1ca-184">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="8c1ca-184">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8c1ca-185">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8c1ca-185">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c1ca-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c1ca-186">Requirements</span></span>



| <span data-ttu-id="8c1ca-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c1ca-187">Requirement</span></span> | <span data-ttu-id="8c1ca-188">Value</span><span class="sxs-lookup"><span data-stu-id="8c1ca-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c1ca-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c1ca-189">Minimum supported client</span></span><br/> | <span data-ttu-id="8c1ca-190">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8c1ca-190">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8c1ca-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c1ca-191">Minimum supported server</span></span><br/> | <span data-ttu-id="8c1ca-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c1ca-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8c1ca-193">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c1ca-193">Namespace</span></span><br/>                | <span data-ttu-id="8c1ca-194">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="8c1ca-194">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="8c1ca-195">MOF</span><span class="sxs-lookup"><span data-stu-id="8c1ca-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c1ca-196"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c1ca-196"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c1ca-197">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c1ca-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c1ca-198"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c1ca-198"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c1ca-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c1ca-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c1ca-200">**Win32 \_ SessionDirectoryCluster**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-200">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="8c1ca-201">**Win32 \_ SessionDirectoryServer**</span><span class="sxs-lookup"><span data-stu-id="8c1ca-201">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> </dl>

 

