---
title: Win32_TSLogonSetting (clase)
description: Define la configuración para la \_ clase de terminal Win32 relacionada con el inicio de sesión de cliente.
ms.assetid: a2ccb419-da1a-44d1-8a7a-4d0266fc1be8
ms.tgt_platform: multiple
keywords:
- Win32_TSLogonSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLogonSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting
- Win32_TSLogonSetting.Caption
- Win32_TSLogonSetting.Description
- Win32_TSLogonSetting.InstallDate
- Win32_TSLogonSetting.Name
- Win32_TSLogonSetting.Status
- Win32_TSLogonSetting.TerminalName
- Win32_TSLogonSetting.ClientLogonInfoPolicy
- Win32_TSLogonSetting.Domain
- Win32_TSLogonSetting.Password
- Win32_TSLogonSetting.PolicySourceDomain
- Win32_TSLogonSetting.PolicySourcePromptForPassword
- Win32_TSLogonSetting.PolicySourceUserName
- Win32_TSLogonSetting.PromptForPassword
- Win32_TSLogonSetting.UserName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e656f3913bb7320253dc9dbca6710f37e0cbdded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422462"
---
# <a name="win32_tslogonsetting-class"></a><span data-ttu-id="97106-105">\_Clase Win32 TSLogonSetting</span><span class="sxs-lookup"><span data-stu-id="97106-105">Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="97106-106">La clase WMI **\_ TSLogonSetting de Win32** define los valores de configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) relacionada con el inicio de sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="97106-106">The **Win32\_TSLogonSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to client logon.</span></span>

<span data-ttu-id="97106-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="97106-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="97106-108">Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="97106-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="97106-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97106-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSLOGONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSLogonSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientLogonInfoPolicy;
  string   Domain;
  string   Password;
  uint32   PolicySourceDomain;
  uint32   PolicySourcePromptForPassword;
  uint32   PolicySourceUserName;
  uint32   PromptForPassword;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="97106-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="97106-110">Members</span></span>

<span data-ttu-id="97106-111">La **clase \_ TSLogonSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="97106-111">The **Win32\_TSLogonSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="97106-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="97106-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="97106-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97106-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="97106-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="97106-114">Methods</span></span>

<span data-ttu-id="97106-115">La clase **Win32 \_ TSLogonSetting** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="97106-115">The **Win32\_TSLogonSetting** class has these methods.</span></span>



| <span data-ttu-id="97106-116">Método</span><span class="sxs-lookup"><span data-stu-id="97106-116">Method</span></span>                                                                    | <span data-ttu-id="97106-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="97106-117">Description</span></span>                                                                    |
|:--------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="97106-118">**ExplicitLogon**</span><span class="sxs-lookup"><span data-stu-id="97106-118">**ExplicitLogon**</span></span>](win32-tslogonsetting-explicitlogon.md)               | <span data-ttu-id="97106-119">Establece el nombre de usuario, la contraseña y las credenciales de autenticación de dominio.</span><span class="sxs-lookup"><span data-stu-id="97106-119">Sets the UserName, Password, and Domain authentication credentials.</span></span><br/> |
| [<span data-ttu-id="97106-120">**SetPromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="97106-120">**SetPromptForPassword**</span></span>](win32-tslogonsetting-setpromptforpassword.md) | <span data-ttu-id="97106-121">Establece la propiedad **PromptForPassword** .</span><span class="sxs-lookup"><span data-stu-id="97106-121">Sets the **PromptForPassword** property.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="97106-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97106-122">Properties</span></span>

<span data-ttu-id="97106-123">La **clase \_ TSLogonSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="97106-123">The **Win32\_TSLogonSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97106-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="97106-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97106-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97106-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97106-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97106-127">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="97106-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="97106-128">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="97106-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="97106-129">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97106-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97106-130">**ClientLogonInfoPolicy**</span><span class="sxs-lookup"><span data-stu-id="97106-130">**ClientLogonInfoPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-131">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97106-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97106-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="97106-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="97106-133">La Directiva que el servidor usa para determinar la configuración de conexión.</span><span class="sxs-lookup"><span data-stu-id="97106-133">The policy the server uses to determine connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="97106-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuario** (0)</span><span class="sxs-lookup"><span data-stu-id="97106-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="97106-135">La configuración de conexión de usuario individual está en vigor.</span><span class="sxs-lookup"><span data-stu-id="97106-135">Individual user connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="97106-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Invalidación de servidor** (1)</span><span class="sxs-lookup"><span data-stu-id="97106-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="97106-137">El servidor invalida la configuración de conexión de usuario individual.</span><span class="sxs-lookup"><span data-stu-id="97106-137">Individual user connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="97106-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="97106-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97106-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97106-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97106-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97106-141">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="97106-141">Description of the object.</span></span>

<span data-ttu-id="97106-142">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97106-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97106-143">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="97106-143">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97106-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97106-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97106-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97106-146">Credencial de autenticación de inicio de sesión de dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="97106-146">The user's domain logon authentication credential.</span></span> <span data-ttu-id="97106-147">Este es el dominio en el que reside el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="97106-147">This is the domain in which the user's computer resides.</span></span> <span data-ttu-id="97106-148">Esta propiedad no puede tener más de 17 caracteres.</span><span class="sxs-lookup"><span data-stu-id="97106-148">This property cannot be longer than 17 characters.</span></span>

</dd> <dt>

<span data-ttu-id="97106-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="97106-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-150">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="97106-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="97106-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97106-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97106-152">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="97106-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="97106-153">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="97106-153">The date the object was installed.</span></span> <span data-ttu-id="97106-154">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="97106-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="97106-155">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97106-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97106-156">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="97106-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97106-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97106-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97106-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97106-159">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="97106-159">The name of the object.</span></span>

<span data-ttu-id="97106-160">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97106-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97106-161">**Contraseña**</span><span class="sxs-lookup"><span data-stu-id="97106-161">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97106-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97106-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97106-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97106-164">La credencial de autenticación de inicio de sesión de contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="97106-164">The user's password logon authentication credential.</span></span> <span data-ttu-id="97106-165">Esta propiedad no puede tener más de 14 caracteres.</span><span class="sxs-lookup"><span data-stu-id="97106-165">This property cannot be longer than 14 characters.</span></span> <span data-ttu-id="97106-166">Se recomienda establecer el nivel de seguridad en privacidad de paquete (wbemAuthenticationLevelPktPrivacy = 6) si consulta esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="97106-166">It is recommended that you set the security level to packet privacy (wbemAuthenticationLevelPktPrivacy = 6) if you query this property.</span></span> <span data-ttu-id="97106-167">Esto se debe a que la contraseña no se cifra en la conexión sin este nivel de seguridad.</span><span class="sxs-lookup"><span data-stu-id="97106-167">This is because the password is not encrypted on the wire without this level of security.</span></span> <span data-ttu-id="97106-168">Para obtener más información acerca de cómo establecer los niveles de seguridad, vea [establecer la seguridad de procesos de aplicación cliente](/windows/desktop/WmiSdk/setting-client-application-process-security) en la documentación del SDK de WMI.</span><span class="sxs-lookup"><span data-stu-id="97106-168">For more information about setting security levels, see [Setting Client Application Process Security](/windows/desktop/WmiSdk/setting-client-application-process-security) in the WMI SDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="97106-169">**PolicySourceDomain**</span><span class="sxs-lookup"><span data-stu-id="97106-169">**PolicySourceDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-170">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97106-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97106-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97106-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97106-172">Indica si la propiedad de **dominio** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="97106-172">Indicates whether the **Domain** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="97106-173">0</span><span class="sxs-lookup"><span data-stu-id="97106-173">0</span></span>
</dt> <dd>

<span data-ttu-id="97106-174">Servidor</span><span class="sxs-lookup"><span data-stu-id="97106-174">Server</span></span>

</dd> <dt>

<span data-ttu-id="97106-175">1</span><span class="sxs-lookup"><span data-stu-id="97106-175">1</span></span>
</dt> <dd>

<span data-ttu-id="97106-176">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="97106-176">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="97106-177">2</span><span class="sxs-lookup"><span data-stu-id="97106-177">2</span></span>
</dt> <dd>

<span data-ttu-id="97106-178">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="97106-178">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="97106-179">**PolicySourcePromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="97106-179">**PolicySourcePromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-180">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97106-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97106-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97106-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97106-182">Indica si la propiedad **PromptForPassword** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="97106-182">Indicates whether the **PromptForPassword** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="97106-183">0</span><span class="sxs-lookup"><span data-stu-id="97106-183">0</span></span>
</dt> <dd>

<span data-ttu-id="97106-184">Servidor</span><span class="sxs-lookup"><span data-stu-id="97106-184">Server</span></span>

</dd> <dt>

<span data-ttu-id="97106-185">1</span><span class="sxs-lookup"><span data-stu-id="97106-185">1</span></span>
</dt> <dd>

<span data-ttu-id="97106-186">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="97106-186">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="97106-187">2</span><span class="sxs-lookup"><span data-stu-id="97106-187">2</span></span>
</dt> <dd>

<span data-ttu-id="97106-188">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="97106-188">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="97106-189">**PolicySourceUserName**</span><span class="sxs-lookup"><span data-stu-id="97106-189">**PolicySourceUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-190">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97106-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97106-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97106-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97106-192">Indica si la propiedad de **nombre de usuario** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="97106-192">Indicates whether the **UserName** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="97106-193">0</span><span class="sxs-lookup"><span data-stu-id="97106-193">0</span></span>
</dt> <dd>

<span data-ttu-id="97106-194">Servidor</span><span class="sxs-lookup"><span data-stu-id="97106-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="97106-195">1</span><span class="sxs-lookup"><span data-stu-id="97106-195">1</span></span>
</dt> <dd>

<span data-ttu-id="97106-196">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="97106-196">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="97106-197">2</span><span class="sxs-lookup"><span data-stu-id="97106-197">2</span></span>
</dt> <dd>

<span data-ttu-id="97106-198">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="97106-198">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="97106-199">**PromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="97106-199">**PromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-200">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97106-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97106-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97106-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97106-202">Especifica si al usuario se le solicita siempre una contraseña mientras inicia sesión en el servidor.</span><span class="sxs-lookup"><span data-stu-id="97106-202">Specifies whether the user is always prompted for a password while logging into the server.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="97106-203"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="97106-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="97106-204">No se solicita una contraseña al usuario.</span><span class="sxs-lookup"><span data-stu-id="97106-204">The user is not prompted for a password.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="97106-205"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="97106-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="97106-206">Al usuario se le solicitará una contraseña.</span><span class="sxs-lookup"><span data-stu-id="97106-206">The user is prompted for a password.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="97106-207">**Estado**</span><span class="sxs-lookup"><span data-stu-id="97106-207">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97106-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97106-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97106-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97106-210">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="97106-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="97106-211">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="97106-211">Current status of the object.</span></span> <span data-ttu-id="97106-212">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="97106-212">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="97106-213">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="97106-213">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="97106-214">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="97106-214">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="97106-215">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="97106-215">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="97106-216">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="97106-216">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="97106-217">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97106-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="97106-218">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="97106-218">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="97106-219">("Error")</span><span class="sxs-lookup"><span data-stu-id="97106-219">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="97106-220">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="97106-220">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="97106-221">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="97106-221">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="97106-222">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="97106-222">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="97106-223">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="97106-223">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="97106-224">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="97106-224">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="97106-225">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="97106-225">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="97106-226">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="97106-226">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97106-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97106-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97106-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97106-229">Nombre del terminal.</span><span class="sxs-lookup"><span data-stu-id="97106-229">The name of the terminal.</span></span>

<span data-ttu-id="97106-230">Esta propiedad se hereda de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="97106-230">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="97106-231">**UserName**</span><span class="sxs-lookup"><span data-stu-id="97106-231">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97106-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97106-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97106-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97106-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97106-234">La credencial de autenticación de inicio de sesión del nombre de usuario del usuario.</span><span class="sxs-lookup"><span data-stu-id="97106-234">The user's user name logon authentication credential.</span></span> <span data-ttu-id="97106-235">Esta propiedad no puede tener más de 20 caracteres.</span><span class="sxs-lookup"><span data-stu-id="97106-235">This property cannot be longer than 20 characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97106-236">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97106-236">Remarks</span></span>

<span data-ttu-id="97106-237">Tenga en cuenta que Winstations asociado a la sesión de consola no puede tener acceso a los métodos y las propiedades de esta clase.</span><span class="sxs-lookup"><span data-stu-id="97106-237">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="97106-238">Si se realiza un intento de hacerlo especificando "Console" como el valor de la propiedad TerminalName, los métodos de este objeto devuelven **WBEM \_ E \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="97106-238">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="97106-239">Este código de error se devuelve si una estación de ventana intenta llamar a métodos de este objeto para agregar o modificar las propiedades de seguridad de las cuentas LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="97106-239">This error code is returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="97106-240">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="97106-240">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="97106-241">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="97106-241">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="97106-242">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="97106-242">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="97106-243">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="97106-243">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="97106-244">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="97106-244">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="97106-245">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="97106-245">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="97106-246">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="97106-246">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="97106-247">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="97106-247">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="97106-248">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97106-248">Requirements</span></span>



| <span data-ttu-id="97106-249">Requisito</span><span class="sxs-lookup"><span data-stu-id="97106-249">Requirement</span></span> | <span data-ttu-id="97106-250">Value</span><span class="sxs-lookup"><span data-stu-id="97106-250">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97106-251">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97106-251">Minimum supported client</span></span><br/> | <span data-ttu-id="97106-252">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97106-252">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97106-253">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97106-253">Minimum supported server</span></span><br/> | <span data-ttu-id="97106-254">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97106-254">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97106-255">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="97106-255">Namespace</span></span><br/>                | <span data-ttu-id="97106-256">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="97106-256">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="97106-257">MOF</span><span class="sxs-lookup"><span data-stu-id="97106-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97106-258"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97106-258"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="97106-259">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="97106-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97106-260"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97106-260"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97106-261">Vea también</span><span class="sxs-lookup"><span data-stu-id="97106-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97106-262">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="97106-262">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="97106-263">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="97106-263">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

