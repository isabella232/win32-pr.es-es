---
description: Win32 \_ DCOMApplicationSetting&\# 8194; La clase WMI representa la configuración de una aplicación DCOM.
ms.assetid: afa23faa-bf4d-4f54-9ee9-227956ff3292
ms.tgt_platform: multiple
title: Win32_DCOMApplicationSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting
- Win32_DCOMApplicationSetting.Caption
- Win32_DCOMApplicationSetting.Description
- Win32_DCOMApplicationSetting.SettingID
- Win32_DCOMApplicationSetting.AppID
- Win32_DCOMApplicationSetting.AuthenticationLevel
- Win32_DCOMApplicationSetting.CustomSurrogate
- Win32_DCOMApplicationSetting.EnableAtStorageActivation
- Win32_DCOMApplicationSetting.LocalService
- Win32_DCOMApplicationSetting.RemoteServerName
- Win32_DCOMApplicationSetting.RunAsUser
- Win32_DCOMApplicationSetting.ServiceParameters
- Win32_DCOMApplicationSetting.UseSurrogate
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 085304c5319811ba87979124613c7d8e83fd7479
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659747"
---
# <a name="win32_dcomapplicationsetting-class"></a><span data-ttu-id="e373a-103">\_Clase Win32 DCOMApplicationSetting</span><span class="sxs-lookup"><span data-stu-id="e373a-103">Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="e373a-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DCOMApplicationSetting de Win32** representa la configuración de una aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="e373a-104">The **Win32\_DCOMApplicationSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a DCOM application.</span></span> <span data-ttu-id="e373a-105">Contiene las opciones de configuración de DCOM asociadas a la clave **AppID** en el registro.</span><span class="sxs-lookup"><span data-stu-id="e373a-105">It contains DCOM configuration options associated with the **AppID** key in the registry.</span></span> <span data-ttu-id="e373a-106">Estas opciones son válidas en los componentes agrupados lógicamente en la clase de aplicación especificada.</span><span class="sxs-lookup"><span data-stu-id="e373a-106">These options are valid on the components logically grouped under the given application class.</span></span>

<span data-ttu-id="e373a-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e373a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e373a-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e373a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e373a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e373a-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A561-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplicationSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  uint32  AuthenticationLevel;
  string  CustomSurrogate;
  boolean EnableAtStorageActivation;
  string  LocalService;
  string  RemoteServerName;
  string  RunAsUser;
  string  ServiceParameters;
  boolean UseSurrogate;
};
```

## <a name="members"></a><span data-ttu-id="e373a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="e373a-110">Members</span></span>

<span data-ttu-id="e373a-111">La **clase \_ DCOMApplicationSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e373a-111">The **Win32\_DCOMApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="e373a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e373a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="e373a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e373a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e373a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="e373a-114">Methods</span></span>

<span data-ttu-id="e373a-115">La clase **Win32 \_ DCOMApplicationSetting** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e373a-115">The **Win32\_DCOMApplicationSetting** class has these methods.</span></span>



| <span data-ttu-id="e373a-116">Método</span><span class="sxs-lookup"><span data-stu-id="e373a-116">Method</span></span>                                                                                                                        | <span data-ttu-id="e373a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e373a-117">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e373a-118">**GetAccessSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e373a-118">**GetAccessSecurityDescriptor**</span></span>](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="e373a-119">Obtiene el descriptor de seguridad que controla quién tiene permiso para obtener acceso a una aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="e373a-119">Gets the security descriptor that controls who is allowed to access a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="e373a-120">**GetConfigurationSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e373a-120">**GetConfigurationSecurityDescriptor**</span></span>](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="e373a-121">Obtiene el descriptor de seguridad que controla quién tiene permiso para configurar una aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="e373a-121">Gets the security descriptor that controls who is allowed to configure a DCOM application.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="e373a-122">**GetLaunchSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e373a-122">**GetLaunchSecurityDescriptor**</span></span>](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | <span data-ttu-id="e373a-123">Obtiene el descriptor de seguridad que controla quién tiene permiso para iniciar una aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="e373a-123">Gets the security descriptor that controls who is allowed to launch a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="e373a-124">**SetAccessSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e373a-124">**SetAccessSecurityDescriptor**</span></span>](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="e373a-125">Actualiza el descriptor de seguridad de acceso de la aplicación DCOM con un nuevo descriptor de seguridad definido por una instancia de la clase de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="e373a-125">Updates the access security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |
| [<span data-ttu-id="e373a-126">**SetConfigurationSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e373a-126">**SetConfigurationSecurityDescriptor**</span></span>](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="e373a-127">Actualiza el descriptor de seguridad de configuración de la aplicación DCOM con un nuevo descriptor de seguridad definido por una instancia de la clase de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="e373a-127">Updates the configuration security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/> |
| [<span data-ttu-id="e373a-128">**SetLaunchSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e373a-128">**SetLaunchSecurityDescriptor**</span></span>](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="e373a-129">Actualiza el descriptor de seguridad de inicio de la aplicación DCOM con un nuevo descriptor de seguridad definido por una instancia de la clase de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="e373a-129">Updates the launch security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="e373a-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e373a-130">Properties</span></span>

<span data-ttu-id="e373a-131">La **clase \_ DCOMApplicationSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e373a-131">The **Win32\_DCOMApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e373a-132">**AppID**</span><span class="sxs-lookup"><span data-stu-id="e373a-132">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e373a-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e373a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e373a-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e373a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e373a-135">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="e373a-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="e373a-136">Identificador único global (GUID) para esta aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="e373a-136">Globally unique identifier (GUID) for this DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="e373a-137">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="e373a-137">**AuthenticationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e373a-138">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e373a-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e373a-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e373a-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e373a-140">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ AuthenticationLevel \] ")</span><span class="sxs-lookup"><span data-stu-id="e373a-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[AuthenticationLevel\]")</span></span>
</dt> </dl>

<span data-ttu-id="e373a-141">Nivel mínimo de autenticación del cliente requerido por este servidor COM.</span><span class="sxs-lookup"><span data-stu-id="e373a-141">Minimum client authentication level required by this COM server.</span></span> <span data-ttu-id="e373a-142">Si **es null**, se usan los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="e373a-142">If **NULL**, the default values are used.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="e373a-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** (1)</span><span class="sxs-lookup"><span data-stu-id="e373a-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e373a-144">Ninguno (no se realiza ninguna autenticación)</span><span class="sxs-lookup"><span data-stu-id="e373a-144">None (no authentication is performed)</span></span>

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span data-ttu-id="e373a-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Conectar** (2)</span><span class="sxs-lookup"><span data-stu-id="e373a-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Connect** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e373a-146">Connect (solo se realiza la autenticación cuando el cliente establece una relación con la aplicación)</span><span class="sxs-lookup"><span data-stu-id="e373a-146">Connect (authentication is performed only when the client establishes a relationship with the application)</span></span>

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span data-ttu-id="e373a-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**Llamar a** (3)</span><span class="sxs-lookup"><span data-stu-id="e373a-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**Call** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e373a-148">Call (la autenticación se realiza solo al principio de cada llamada cuando la aplicación recibe la solicitud)</span><span class="sxs-lookup"><span data-stu-id="e373a-148">Call (authentication is performed only at the beginning of each call when the application receives the request)</span></span>

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span data-ttu-id="e373a-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Paquete** (4)</span><span class="sxs-lookup"><span data-stu-id="e373a-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Packet** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e373a-150">Paquete (la autenticación se realiza en todos los datos recibidos del cliente)</span><span class="sxs-lookup"><span data-stu-id="e373a-150">Packet (authentication is performed on all of the data received from the client)</span></span>

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span data-ttu-id="e373a-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)</span><span class="sxs-lookup"><span data-stu-id="e373a-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e373a-152">PacketIntegrity (todos los datos transferidos entre el cliente y la aplicación se autentican y comprueban)</span><span class="sxs-lookup"><span data-stu-id="e373a-152">PacketIntegrity (all of the data transferred between the client and the application is authenticated and verified)</span></span>

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span data-ttu-id="e373a-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)</span><span class="sxs-lookup"><span data-stu-id="e373a-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e373a-154">PacketPrivacy (se usan las propiedades de los otros niveles de autenticación y se cifran todos los datos)</span><span class="sxs-lookup"><span data-stu-id="e373a-154">PacketPrivacy (the properties of the other authentication levels are used and all of the data is encrypted)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e373a-155">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e373a-155">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e373a-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e373a-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e373a-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e373a-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e373a-158">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e373a-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e373a-159">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="e373a-159">Short textual description of the current object.</span></span>

<span data-ttu-id="e373a-160">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e373a-160">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e373a-161">**CustomSurrogate**</span><span class="sxs-lookup"><span data-stu-id="e373a-161">**CustomSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e373a-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e373a-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e373a-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e373a-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e373a-164">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")</span><span class="sxs-lookup"><span data-stu-id="e373a-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="e373a-165">Nombre del suplente personalizado en el que se activa la aplicación DCOM en proceso.</span><span class="sxs-lookup"><span data-stu-id="e373a-165">Name of the custom surrogate in which the in-process DCOM application is activated.</span></span> <span data-ttu-id="e373a-166">Si este valor es **null** y la clave **UseSurrogate** es **true**, el sistema proporciona un proceso suplente.</span><span class="sxs-lookup"><span data-stu-id="e373a-166">If this value is **NULL** and the **UseSurrogate** key is **TRUE**, then the system provides a surrogate process.</span></span>

</dd> <dt>

<span data-ttu-id="e373a-167">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e373a-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e373a-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e373a-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e373a-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e373a-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e373a-170">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="e373a-170">Textual description of the current object.</span></span>

<span data-ttu-id="e373a-171">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e373a-171">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e373a-172">**EnableAtStorageActivation**</span><span class="sxs-lookup"><span data-stu-id="e373a-172">**EnableAtStorageActivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e373a-173">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e373a-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e373a-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e373a-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e373a-175">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ ActivateAtStorage \] ")</span><span class="sxs-lookup"><span data-stu-id="e373a-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ActivateAtStorage\]")</span></span>
</dt> </dl>

<span data-ttu-id="e373a-176">La aplicación DCOM recupera el estado guardado de la aplicación o comienza en el estado en el que la aplicación se inicializa por primera vez.</span><span class="sxs-lookup"><span data-stu-id="e373a-176">DCOM application retrieves the saved state of the application or begins from the state in which the application is first initialized.</span></span>

</dd> <dt>

<span data-ttu-id="e373a-177">**LocalService (Servicio local)**</span><span class="sxs-lookup"><span data-stu-id="e373a-177">**LocalService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e373a-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e373a-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e373a-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e373a-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e373a-180">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ LocalService \] ")</span><span class="sxs-lookup"><span data-stu-id="e373a-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[LocalService\]")</span></span>
</dt> </dl>

<span data-ttu-id="e373a-181">Nombre de los servicios proporcionados por la aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="e373a-181">Name for the services provided by the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="e373a-182">**RemoteServerName**</span><span class="sxs-lookup"><span data-stu-id="e373a-182">**RemoteServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e373a-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e373a-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e373a-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e373a-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e373a-185">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ RemoteServerName \] ")</span><span class="sxs-lookup"><span data-stu-id="e373a-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RemoteServerName\]")</span></span>
</dt> </dl>

<span data-ttu-id="e373a-186">Nombre del servidor remoto en el que se activa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e373a-186">Name of the remote server where the application is activated.</span></span>

</dd> <dt>

<span data-ttu-id="e373a-187">**Como_usuario**</span><span class="sxs-lookup"><span data-stu-id="e373a-187">**RunAsUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e373a-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e373a-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e373a-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e373a-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e373a-190">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ runas \] ")</span><span class="sxs-lookup"><span data-stu-id="e373a-190">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RunAs\]")</span></span>
</dt> </dl>

<span data-ttu-id="e373a-191">Cuenta de usuario específica en la que se ejecutará la aplicación durante la activación.</span><span class="sxs-lookup"><span data-stu-id="e373a-191">Specific user account under which the application is to be run on activation.</span></span>

</dd> <dt>

<span data-ttu-id="e373a-192">**ServiceParameters**</span><span class="sxs-lookup"><span data-stu-id="e373a-192">**ServiceParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e373a-193">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e373a-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e373a-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e373a-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e373a-195">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ ServiceParameters \] ")</span><span class="sxs-lookup"><span data-stu-id="e373a-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ServiceParameters\]")</span></span>
</dt> </dl>

<span data-ttu-id="e373a-196">Parámetros de línea de comandos pasados a la aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="e373a-196">Command-line parameters passed to the DCOM application.</span></span> <span data-ttu-id="e373a-197">Esto solo es válido si la aplicación se escribe como un servicio basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="e373a-197">This is valid only if the application is written as a Windows-based service.</span></span>

</dd> <dt>

<span data-ttu-id="e373a-198">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="e373a-198">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e373a-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e373a-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e373a-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e373a-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e373a-201">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e373a-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e373a-202">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="e373a-202">Identifier by which the current object is known.</span></span>

<span data-ttu-id="e373a-203">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e373a-203">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e373a-204">**UseSurrogate**</span><span class="sxs-lookup"><span data-stu-id="e373a-204">**UseSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e373a-205">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e373a-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e373a-206">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e373a-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e373a-207">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")</span><span class="sxs-lookup"><span data-stu-id="e373a-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="e373a-208">La aplicación DCOM se puede activar como un servidor fuera de proceso mediante el uso de un archivo ejecutable suplente.</span><span class="sxs-lookup"><span data-stu-id="e373a-208">DCOM application can be activated as an out-of-process server by use of a surrogate executable file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e373a-209">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e373a-209">Remarks</span></span>

<span data-ttu-id="e373a-210">La clase **Win32 \_ DCOMApplicationSetting** se deriva de [**\_ comsetting de Win32**](win32-comsetting.md).</span><span class="sxs-lookup"><span data-stu-id="e373a-210">The **Win32\_DCOMApplicationSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e373a-211">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e373a-211">Requirements</span></span>



| <span data-ttu-id="e373a-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="e373a-212">Requirement</span></span> | <span data-ttu-id="e373a-213">Value</span><span class="sxs-lookup"><span data-stu-id="e373a-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e373a-214">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e373a-214">Minimum supported client</span></span><br/> | <span data-ttu-id="e373a-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e373a-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e373a-216">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e373a-216">Minimum supported server</span></span><br/> | <span data-ttu-id="e373a-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e373a-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e373a-218">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e373a-218">Namespace</span></span><br/>                | <span data-ttu-id="e373a-219">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e373a-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e373a-220">MOF</span><span class="sxs-lookup"><span data-stu-id="e373a-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e373a-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e373a-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e373a-222">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e373a-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e373a-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e373a-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e373a-224">Vea también</span><span class="sxs-lookup"><span data-stu-id="e373a-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e373a-225">**Establecimiento de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="e373a-225">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="e373a-226">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e373a-226">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e373a-227">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="e373a-227">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="e373a-228">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="e373a-228">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="e373a-229">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="e373a-229">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

