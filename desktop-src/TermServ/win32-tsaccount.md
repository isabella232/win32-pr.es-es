---
title: Win32_TSAccount (clase)
description: Permite la eliminación de una cuenta que existe en el \_ terminal Win32 y la modificación de los permisos existentes.
ms.assetid: fd4d8a0f-685b-4619-84f1-faefbabd04ba
ms.tgt_platform: multiple
keywords:
- Win32_TSAccount clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSAccount de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSAccount
- Win32_TSAccount.Caption
- Win32_TSAccount.Description
- Win32_TSAccount.InstallDate
- Win32_TSAccount.Name
- Win32_TSAccount.Status
- Win32_TSAccount.TerminalName
- Win32_TSAccount.AccountName
- Win32_TSAccount.AuditFail
- Win32_TSAccount.AuditSuccess
- Win32_TSAccount.PermissionsAllowed
- Win32_TSAccount.PermissionsDenied
- Win32_TSAccount.SID
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fed32943cf89728081e2443dfffe2e3762298d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686155"
---
# <a name="win32_tsaccount-class"></a><span data-ttu-id="73b8a-105">\_Clase Win32 TSAccount</span><span class="sxs-lookup"><span data-stu-id="73b8a-105">Win32\_TSAccount class</span></span>

<span data-ttu-id="73b8a-106">La clase WMI **\_ TSAccount de Win32** permite la eliminación de una cuenta que existe en el [**\_ terminal Win32**](win32-terminal.md) y la modificación de los permisos existentes.</span><span class="sxs-lookup"><span data-stu-id="73b8a-106">The **Win32\_TSAccount** WMI class allows deletion of an account that exists on the [**Win32\_Terminal**](win32-terminal.md) and modification of existing permissions.</span></span>

<span data-ttu-id="73b8a-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="73b8a-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="73b8a-108">Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="73b8a-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="73b8a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73b8a-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSACCOUNT_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSAccount : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   AccountName;
  uint32   AuditFail;
  uint32   AuditSuccess;
  uint32   PermissionsAllowed;
  uint32   PermissionsDenied;
  string   SID;
};
```

## <a name="members"></a><span data-ttu-id="73b8a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="73b8a-110">Members</span></span>

<span data-ttu-id="73b8a-111">La **clase \_ TSAccount de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="73b8a-111">The **Win32\_TSAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="73b8a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="73b8a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="73b8a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73b8a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="73b8a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="73b8a-114">Methods</span></span>

<span data-ttu-id="73b8a-115">La clase **Win32 \_ TSAccount** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="73b8a-115">The **Win32\_TSAccount** class has these methods.</span></span>



| <span data-ttu-id="73b8a-116">Método</span><span class="sxs-lookup"><span data-stu-id="73b8a-116">Method</span></span>                                                                   | <span data-ttu-id="73b8a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="73b8a-117">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73b8a-118">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="73b8a-118">**Delete**</span></span>](win32-tsaccount-delete.md)                                 | <span data-ttu-id="73b8a-119">Elimina la cuenta de usuario, grupo o equipo especificada.</span><span class="sxs-lookup"><span data-stu-id="73b8a-119">Deletes the specified user, group, or computer account.</span></span><br/>                           |
| [<span data-ttu-id="73b8a-120">**ModifyAuditPermissions**</span><span class="sxs-lookup"><span data-stu-id="73b8a-120">**ModifyAuditPermissions**</span></span>](win32-tsaccount-modifyauditpermissions.md) | <span data-ttu-id="73b8a-121">Cambia la granularidad del conjunto de permisos de auditoría de la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="73b8a-121">Changes the granularity of the set of audit permissions of the specified account.</span></span><br/> |
| [<span data-ttu-id="73b8a-122">**ModifyPermissions**</span><span class="sxs-lookup"><span data-stu-id="73b8a-122">**ModifyPermissions**</span></span>](win32-tsaccount-modifypermissions.md)           | <span data-ttu-id="73b8a-123">Establece un conjunto de permisos más granular en la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="73b8a-123">Sets a more granular permission set to the specified account.</span></span><br/>                     |



 

### <a name="properties"></a><span data-ttu-id="73b8a-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73b8a-124">Properties</span></span>

<span data-ttu-id="73b8a-125">La **clase \_ TSAccount de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="73b8a-125">The **Win32\_TSAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73b8a-126">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="73b8a-126">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b8a-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="73b8a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73b8a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-129">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="73b8a-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="73b8a-130">Nombre actual de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="73b8a-130">The current name of the account.</span></span> <span data-ttu-id="73b8a-131">Se incluye el nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="73b8a-131">The domain name is included.</span></span>

</dd> <dt>

<span data-ttu-id="73b8a-132">**AuditFail**</span><span class="sxs-lookup"><span data-stu-id="73b8a-132">**AuditFail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b8a-133">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73b8a-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73b8a-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73b8a-135">Especifica los [permisos de servicios de host de sesión escritorio remoto](terminal-services-permissions.md) que se auditan para una condición de error.</span><span class="sxs-lookup"><span data-stu-id="73b8a-135">Specifies the [Remote Desktop Session Host Services Permissions](terminal-services-permissions.md) that are audited for a failure condition.</span></span> <span data-ttu-id="73b8a-136">El valor de esta propiedad es una máscara de máscara, que se puede establecer en uno o varios de los valores de la propiedad **PermissionsAllowed** .</span><span class="sxs-lookup"><span data-stu-id="73b8a-136">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="73b8a-137">**Estación \_ de CONSULTA = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="73b8a-137">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="73b8a-138">**Estación \_ de SET = 0X2** (1)</span><span class="sxs-lookup"><span data-stu-id="73b8a-138">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="73b8a-139">**Estación \_ de LOGOFF = 0x4** (2)</span><span class="sxs-lookup"><span data-stu-id="73b8a-139">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="73b8a-140">**Estación \_ de \| Derechos de estándar virtual \_ \_ necesarios = 0xF008** (3)</span><span class="sxs-lookup"><span data-stu-id="73b8a-140">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="73b8a-141">**Estación \_ de SHADOW = 0x10** (4)</span><span class="sxs-lookup"><span data-stu-id="73b8a-141">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="73b8a-142">**Estación \_ de LOGON = 0x20** (5)</span><span class="sxs-lookup"><span data-stu-id="73b8a-142">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="73b8a-143">**Estación \_ de MSG = 0x80** (6)</span><span class="sxs-lookup"><span data-stu-id="73b8a-143">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="73b8a-144">**Estación \_ de CONNECT = 0x100** (7)</span><span class="sxs-lookup"><span data-stu-id="73b8a-144">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="73b8a-145">**Estación \_ de DISCONNECT = 0x200** (8)</span><span class="sxs-lookup"><span data-stu-id="73b8a-145">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="73b8a-146">**AuditSuccess**</span><span class="sxs-lookup"><span data-stu-id="73b8a-146">**AuditSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b8a-147">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73b8a-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73b8a-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73b8a-149">Especifica los permisos específicos del servidor host de sesión de escritorio remoto que se auditan para una condición de éxito.</span><span class="sxs-lookup"><span data-stu-id="73b8a-149">Specifies the RD Session Host server-specific permissions that are audited for a success condition.</span></span> <span data-ttu-id="73b8a-150">El valor de esta propiedad es una máscara de máscara, que se puede establecer en uno o varios de los valores de la propiedad **PermissionsAllowed** .</span><span class="sxs-lookup"><span data-stu-id="73b8a-150">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="73b8a-151">**Estación \_ de CONSULTA = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="73b8a-151">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="73b8a-152">**Estación \_ de SET = 0X2** (1)</span><span class="sxs-lookup"><span data-stu-id="73b8a-152">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_logoff_0x4winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_LOGOFF_0X4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="73b8a-153">**Estación \_ de LOGOFF = 0x4WINSTATION \_ \| derechos de estándar virtual \_ \_ necesarios = 0xF008** (2)</span><span class="sxs-lookup"><span data-stu-id="73b8a-153">**WINSTATION\_LOGOFF=0x4WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="73b8a-154">**Estación \_ de SHADOW = 0x10** (3)</span><span class="sxs-lookup"><span data-stu-id="73b8a-154">**WINSTATION\_SHADOW=0x10** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="73b8a-155">**Estación \_ de LOGON = 0x20** (4)</span><span class="sxs-lookup"><span data-stu-id="73b8a-155">**WINSTATION\_LOGON=0x20** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="73b8a-156">**Estación \_ de MSG = 0x80** (5)</span><span class="sxs-lookup"><span data-stu-id="73b8a-156">**WINSTATION\_MSG=0x80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="73b8a-157">**Estación \_ de CONNECT = 0x100** (6)</span><span class="sxs-lookup"><span data-stu-id="73b8a-157">**WINSTATION\_CONNECT=0x100** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="73b8a-158">**Estación \_ de DISCONNECT = 0x200** (7)</span><span class="sxs-lookup"><span data-stu-id="73b8a-158">**WINSTATION\_DISCONNECT=0x200** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="73b8a-159">**Caption**</span><span class="sxs-lookup"><span data-stu-id="73b8a-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b8a-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="73b8a-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73b8a-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-162">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="73b8a-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="73b8a-163">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="73b8a-163">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="73b8a-164">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73b8a-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73b8a-165">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="73b8a-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b8a-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="73b8a-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73b8a-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73b8a-168">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="73b8a-168">Description of the object.</span></span>

<span data-ttu-id="73b8a-169">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73b8a-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73b8a-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="73b8a-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b8a-171">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="73b8a-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73b8a-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-173">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="73b8a-173">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="73b8a-174">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="73b8a-174">The date the object was installed.</span></span> <span data-ttu-id="73b8a-175">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="73b8a-175">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="73b8a-176">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73b8a-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73b8a-177">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="73b8a-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b8a-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="73b8a-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73b8a-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73b8a-180">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="73b8a-180">The name of the object.</span></span>

<span data-ttu-id="73b8a-181">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73b8a-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73b8a-182">**PermissionsAllowed**</span><span class="sxs-lookup"><span data-stu-id="73b8a-182">**PermissionsAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b8a-183">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73b8a-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73b8a-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73b8a-185">Especifica el [servicios de escritorio remoto permisos](terminal-services-permissions.md) permitidos para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="73b8a-185">Specifies the [Remote Desktop Services Permissions](terminal-services-permissions.md) allowed for the account.</span></span> <span data-ttu-id="73b8a-186">El valor de esta propiedad es una máscara de máscara, que se puede establecer en uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="73b8a-186">The value of this property is a bitmask, which can be set to one or more of the following values.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="73b8a-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**Estación \_ de CONSULTA = 0x1** (1)</span><span class="sxs-lookup"><span data-stu-id="73b8a-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**WINSTATION\_QUERY=0x1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="73b8a-188">Permiso para consultar información acerca de una sesión.</span><span class="sxs-lookup"><span data-stu-id="73b8a-188">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="73b8a-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**Estación \_ de CONJUNTO** (2)</span><span class="sxs-lookup"><span data-stu-id="73b8a-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (2)</span></span>


</dt> <dd>

<span data-ttu-id="73b8a-190">Permiso para modificar los parámetros de conexión.</span><span class="sxs-lookup"><span data-stu-id="73b8a-190">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="73b8a-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**Estación \_ de RESTABLECER** (64)</span><span class="sxs-lookup"><span data-stu-id="73b8a-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (64)</span></span>


</dt> <dd>

<span data-ttu-id="73b8a-192">Permiso para restablecer o finalizar una sesión o una conexión.</span><span class="sxs-lookup"><span data-stu-id="73b8a-192">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="73b8a-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**Estación \_ de Se \| \_ \_ requieren derechos de estándar virtual** (983048)</span><span class="sxs-lookup"><span data-stu-id="73b8a-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (983048)</span></span>


</dt> <dd>

<span data-ttu-id="73b8a-194">Permiso para usar canales virtuales.</span><span class="sxs-lookup"><span data-stu-id="73b8a-194">Permission to use virtual channels.</span></span> <span data-ttu-id="73b8a-195">Los canales virtuales proporcionan acceso desde un programa de servidor a los dispositivos cliente.</span><span class="sxs-lookup"><span data-stu-id="73b8a-195">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="73b8a-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**Estación \_ de SOMBRA** (16)</span><span class="sxs-lookup"><span data-stu-id="73b8a-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (16)</span></span>


</dt> <dd>

<span data-ttu-id="73b8a-197">Permiso para sombra o control remoto de la sesión de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="73b8a-197">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="73b8a-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**Estación \_ de Inicio de sesión** (32)</span><span class="sxs-lookup"><span data-stu-id="73b8a-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (32)</span></span>


</dt> <dd>

<span data-ttu-id="73b8a-199">Permiso para iniciar sesión en una sesión en el servidor.</span><span class="sxs-lookup"><span data-stu-id="73b8a-199">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="73b8a-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**Estación \_ de CERRAR sesión** (4)</span><span class="sxs-lookup"><span data-stu-id="73b8a-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (4)</span></span>


</dt> <dd>

<span data-ttu-id="73b8a-201">Permiso para cerrar la sesión de un usuario.</span><span class="sxs-lookup"><span data-stu-id="73b8a-201">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="73b8a-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**Estación \_ de MENSAJE** (128)</span><span class="sxs-lookup"><span data-stu-id="73b8a-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (128)</span></span>


</dt> <dd>

<span data-ttu-id="73b8a-203">Permiso para enviar un mensaje a la sesión de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="73b8a-203">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="73b8a-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**Estación \_ de CONECTAR** (256)</span><span class="sxs-lookup"><span data-stu-id="73b8a-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (256)</span></span>


</dt> <dd>

<span data-ttu-id="73b8a-205">Permiso para conectarse a otra sesión.</span><span class="sxs-lookup"><span data-stu-id="73b8a-205">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="73b8a-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**Estación \_ de DESCONECTAR** (512)</span><span class="sxs-lookup"><span data-stu-id="73b8a-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (512)</span></span>


</dt> <dd>

<span data-ttu-id="73b8a-207">Permiso para desconectar una sesión.</span><span class="sxs-lookup"><span data-stu-id="73b8a-207">Permission to disconnect a session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="73b8a-208">**PermissionsDenied**</span><span class="sxs-lookup"><span data-stu-id="73b8a-208">**PermissionsDenied**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b8a-209">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73b8a-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73b8a-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73b8a-211">Especifica los permisos específicos del servidor host de sesión de escritorio remoto no permitidos para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="73b8a-211">Specifies the RD Session Host server-specific permissions disallowed for the account.</span></span> <span data-ttu-id="73b8a-212">El valor de esta propiedad es una máscara de máscara, que se puede establecer en uno o varios de los valores de la propiedad **PermissionsAllowed** .</span><span class="sxs-lookup"><span data-stu-id="73b8a-212">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="73b8a-213">**Estación \_ de CONSULTA = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="73b8a-213">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="73b8a-214">**Estación \_ de SET = 0X2** (1)</span><span class="sxs-lookup"><span data-stu-id="73b8a-214">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="73b8a-215">**Estación \_ de LOGOFF = 0x4** (2)</span><span class="sxs-lookup"><span data-stu-id="73b8a-215">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="73b8a-216">**Estación \_ de \| Derechos de estándar virtual \_ \_ necesarios = 0xF008** (3)</span><span class="sxs-lookup"><span data-stu-id="73b8a-216">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="73b8a-217">**Estación \_ de SHADOW = 0x10** (4)</span><span class="sxs-lookup"><span data-stu-id="73b8a-217">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="73b8a-218">**Estación \_ de LOGON = 0x20** (5)</span><span class="sxs-lookup"><span data-stu-id="73b8a-218">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="73b8a-219">**Estación \_ de MSG = 0x80** (6)</span><span class="sxs-lookup"><span data-stu-id="73b8a-219">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="73b8a-220">**Estación \_ de CONNECT = 0x100** (7)</span><span class="sxs-lookup"><span data-stu-id="73b8a-220">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="73b8a-221">**Estación \_ de DISCONNECT = 0x200** (8)</span><span class="sxs-lookup"><span data-stu-id="73b8a-221">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="73b8a-222">**SID**</span><span class="sxs-lookup"><span data-stu-id="73b8a-222">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b8a-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="73b8a-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73b8a-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73b8a-225">Especifica los [identificadores de seguridad](/windows/desktop/SecAuthZ/security-identifiers) de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="73b8a-225">Specifies the [Security Identifiers](/windows/desktop/SecAuthZ/security-identifiers) of the account.</span></span>

</dd> <dt>

<span data-ttu-id="73b8a-226">**Estado**</span><span class="sxs-lookup"><span data-stu-id="73b8a-226">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b8a-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="73b8a-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73b8a-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-229">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="73b8a-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="73b8a-230">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="73b8a-230">Current status of the object.</span></span> <span data-ttu-id="73b8a-231">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="73b8a-231">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="73b8a-232">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="73b8a-232">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="73b8a-233">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="73b8a-233">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="73b8a-234">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="73b8a-234">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="73b8a-235">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="73b8a-235">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="73b8a-236">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73b8a-236">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="73b8a-237">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="73b8a-237">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="73b8a-238">("Error")</span><span class="sxs-lookup"><span data-stu-id="73b8a-238">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="73b8a-239">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="73b8a-239">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="73b8a-240">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="73b8a-240">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="73b8a-241">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="73b8a-241">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="73b8a-242">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="73b8a-242">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="73b8a-243">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="73b8a-243">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="73b8a-244">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="73b8a-244">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="73b8a-245">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="73b8a-245">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b8a-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="73b8a-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73b8a-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73b8a-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73b8a-248">Nombre del terminal.</span><span class="sxs-lookup"><span data-stu-id="73b8a-248">The name of the terminal.</span></span>

<span data-ttu-id="73b8a-249">Esta propiedad se hereda de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="73b8a-249">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73b8a-250">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73b8a-250">Remarks</span></span>

<span data-ttu-id="73b8a-251">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="73b8a-251">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="73b8a-252">En el caso de las llamadas de C/C++, esto sería un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="73b8a-252">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="73b8a-253">En el caso de las llamadas de Visual Basic y scripting, esto sería un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="73b8a-253">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="73b8a-254">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="73b8a-254">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="73b8a-255">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="73b8a-255">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="73b8a-256">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="73b8a-256">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="73b8a-257">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="73b8a-257">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="73b8a-258">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="73b8a-258">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="73b8a-259">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73b8a-259">Requirements</span></span>



| <span data-ttu-id="73b8a-260">Requisito</span><span class="sxs-lookup"><span data-stu-id="73b8a-260">Requirement</span></span> | <span data-ttu-id="73b8a-261">Value</span><span class="sxs-lookup"><span data-stu-id="73b8a-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73b8a-262">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73b8a-262">Minimum supported client</span></span><br/> | <span data-ttu-id="73b8a-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73b8a-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73b8a-264">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73b8a-264">Minimum supported server</span></span><br/> | <span data-ttu-id="73b8a-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73b8a-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73b8a-266">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="73b8a-266">Namespace</span></span><br/>                | <span data-ttu-id="73b8a-267">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="73b8a-267">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="73b8a-268">MOF</span><span class="sxs-lookup"><span data-stu-id="73b8a-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73b8a-269"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73b8a-269"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="73b8a-270">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="73b8a-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73b8a-271"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73b8a-271"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73b8a-272">Vea también</span><span class="sxs-lookup"><span data-stu-id="73b8a-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73b8a-273">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="73b8a-273">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

