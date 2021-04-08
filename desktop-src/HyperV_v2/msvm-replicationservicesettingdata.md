---
description: Representa la configuración para el servicio de replicación en un host de recuperación. Las propiedades de esta clase no se pueden modificar directamente. El cliente debe llamar al \_ método MSVM ReplicationService. ModifyServiceSettings para modificar cualquiera de estas propiedades.
ms.assetid: a0c0b45a-3578-412a-910e-cd4b3ff0e262
title: Msvm_ReplicationServiceSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationServiceSettingData
- Msvm_ReplicationServiceSettingData.InstanceID
- Msvm_ReplicationServiceSettingData.Caption
- Msvm_ReplicationServiceSettingData.Description
- Msvm_ReplicationServiceSettingData.ElementName
- Msvm_ReplicationServiceSettingData.RecoveryServerEnabled
- Msvm_ReplicationServiceSettingData.AllowedAuthenticationType
- Msvm_ReplicationServiceSettingData.CertificateThumbPrint
- Msvm_ReplicationServiceSettingData.HttpsPort
- Msvm_ReplicationServiceSettingData.HttpPort
- Msvm_ReplicationServiceSettingData.MonitoringStartTime
- Msvm_ReplicationServiceSettingData.MonitoringInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e2886529ab74fed52ec0c6077bfa3d9222fca55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910738"
---
# <a name="msvm_replicationservicesettingdata-class"></a><span data-ttu-id="f6182-105">MSVM \_ ReplicationServiceSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="f6182-105">Msvm\_ReplicationServiceSettingData class</span></span>

<span data-ttu-id="f6182-106">Representa la configuración para el servicio de replicación en un host de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f6182-106">Represents the settings for the replication service on a recovery host.</span></span> <span data-ttu-id="f6182-107">Las propiedades de esta clase no se pueden modificar directamente.</span><span class="sxs-lookup"><span data-stu-id="f6182-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="f6182-108">El cliente debe llamar al método [**MSVM \_ ReplicationService. ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) para modificar cualquiera de estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f6182-108">The client must call the [**Msvm\_ReplicationService.ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="f6182-109">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f6182-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6182-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6182-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Replication Service Settings";
  string   Description = "Virtual Machine Replication Service Settings Data";
  string   ElementName = "Replication Service Settings";
  boolean  RecoveryServerEnabled = False;
  uint16   AllowedAuthenticationType = 0;
  string   CertificateThumbPrint;
  uint16   HttpsPort = 443;
  uint16   HttpPort = 80;
  datetime MonitoringStartTime;
  uint32   MonitoringInterval = 43200;
};
```

## <a name="members"></a><span data-ttu-id="f6182-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6182-111">Members</span></span>

<span data-ttu-id="f6182-112">La clase **MSVM \_ ReplicationServiceSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f6182-112">The **Msvm\_ReplicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f6182-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6182-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6182-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6182-114">Properties</span></span>

<span data-ttu-id="f6182-115">La clase **MSVM \_ ReplicationServiceSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f6182-115">The **Msvm\_ReplicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6182-116">**AllowedAuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="f6182-116">**AllowedAuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6182-117">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6182-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6182-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6182-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6182-119">Definir los modos de autenticación permitidos para conectarse al servidor host de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f6182-119">Define authentication modes allowed for connecting to recovery host server.</span></span>

<dt>

<span data-ttu-id="f6182-120">0</span><span class="sxs-lookup"><span data-stu-id="f6182-120">0</span></span>
</dt> <dd>

<span data-ttu-id="f6182-121">Sin definir.</span><span class="sxs-lookup"><span data-stu-id="f6182-121">Not defined.</span></span>

</dd> <dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="f6182-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Autenticación Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="f6182-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f6182-123">Autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="f6182-123">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="f6182-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticación basada en certificados** (2)</span><span class="sxs-lookup"><span data-stu-id="f6182-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f6182-125">Autenticación basada en certificados.</span><span class="sxs-lookup"><span data-stu-id="f6182-125">Certificate based authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="f6182-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Autenticación basada en certificados y autenticación Kerberos** (3)</span><span class="sxs-lookup"><span data-stu-id="f6182-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Certificate based authentication and kerberos authentication** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f6182-127">Autenticación basada en certificados y autenticación integrada.</span><span class="sxs-lookup"><span data-stu-id="f6182-127">Both certificate based authentication and integrated authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6182-128">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f6182-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6182-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6182-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6182-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6182-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6182-131">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="f6182-131">A short description of the object.</span></span> <span data-ttu-id="f6182-132">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del servicio de replicación".</span><span class="sxs-lookup"><span data-stu-id="f6182-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="f6182-133">**CertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="f6182-133">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6182-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6182-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6182-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6182-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6182-136">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="f6182-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="f6182-137">Huella digital del certificado que se usará cuando **AuthenticationType** sea autenticación basada en certificados.</span><span class="sxs-lookup"><span data-stu-id="f6182-137">Certificate thumbprint to use when **AuthenticationType** is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="f6182-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f6182-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6182-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6182-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6182-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6182-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6182-141">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="f6182-141">A description of the object.</span></span> <span data-ttu-id="f6182-142">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "datos de configuración de replicación de máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="f6182-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="f6182-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f6182-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6182-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6182-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6182-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6182-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6182-146">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="f6182-146">A display name for the object.</span></span> <span data-ttu-id="f6182-147">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del servicio de replicación".</span><span class="sxs-lookup"><span data-stu-id="f6182-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="f6182-148">**HttpPort**</span><span class="sxs-lookup"><span data-stu-id="f6182-148">**HttpPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6182-149">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6182-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6182-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6182-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6182-151">Número de puerto del servidor de recuperación que se va a usar al aceptar una conexión no segura para la replicación.</span><span class="sxs-lookup"><span data-stu-id="f6182-151">Recovery server port number to use when accepting a nonsecure connection for replication.</span></span> <span data-ttu-id="f6182-152">El valor predeterminado es 80.</span><span class="sxs-lookup"><span data-stu-id="f6182-152">The default value is 80.</span></span>

</dd> <dt>

<span data-ttu-id="f6182-153">**HttpsPort**</span><span class="sxs-lookup"><span data-stu-id="f6182-153">**HttpsPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6182-154">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6182-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6182-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6182-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6182-156">Número de puerto del servidor de recuperación que se va a usar al aceptar una conexión segura para la replicación.</span><span class="sxs-lookup"><span data-stu-id="f6182-156">Recovery server port number to use when accepting secure connection for replication.</span></span> <span data-ttu-id="f6182-157">El valor predeterminado es 443.</span><span class="sxs-lookup"><span data-stu-id="f6182-157">The default value is 443.</span></span>

</dd> <dt>

<span data-ttu-id="f6182-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f6182-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6182-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6182-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6182-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6182-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6182-161">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="f6182-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f6182-162">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="f6182-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f6182-163">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6182-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6182-164">**MonitoringInterval**</span><span class="sxs-lookup"><span data-stu-id="f6182-164">**MonitoringInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6182-165">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6182-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6182-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6182-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6182-167">Intervalo, en segundos, en el que se deben restablecer las estadísticas de replicación.</span><span class="sxs-lookup"><span data-stu-id="f6182-167">The interval, in seconds, at which replication statistics should be reset.</span></span> <span data-ttu-id="f6182-168">El intervalo predeterminado es de 12 horas (43200 segundos).</span><span class="sxs-lookup"><span data-stu-id="f6182-168">The default interval is 12 hours (43200 seconds).</span></span> <span data-ttu-id="f6182-169">El valor válido mínimo es 60 minutos (3600 segundos) y el valor máximo válido es de 7 días (604800 segundos).</span><span class="sxs-lookup"><span data-stu-id="f6182-169">The minimum valid value is 60 minutes (3600 seconds), and the maximum valid value is 7 days (604800 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="f6182-170">**MonitoringStartTime**</span><span class="sxs-lookup"><span data-stu-id="f6182-170">**MonitoringStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6182-171">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f6182-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f6182-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6182-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6182-173">La hora de inicio de la supervisión de la replicación, en UTC.</span><span class="sxs-lookup"><span data-stu-id="f6182-173">The start time for replication monitoring, in UTC.</span></span> <span data-ttu-id="f6182-174">El valor predeterminado es 9:00 A.M., hora local, representada en UTC.</span><span class="sxs-lookup"><span data-stu-id="f6182-174">The default value is 9:00 A.M., local time, represented in UTC.</span></span> <span data-ttu-id="f6182-175">Los elementos de fecha del objeto **DateTime** deben ser cero.</span><span class="sxs-lookup"><span data-stu-id="f6182-175">The date elements of the **datetime** object must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f6182-176">**RecoveryServerEnabled**</span><span class="sxs-lookup"><span data-stu-id="f6182-176">**RecoveryServerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6182-177">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f6182-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6182-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6182-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6182-179">Especifica si el host de Hyper-V está habilitado como servidor de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f6182-179">Specifies whether the Hyper-V host is enabled as a recovery server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6182-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6182-180">Requirements</span></span>



| <span data-ttu-id="f6182-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6182-181">Requirement</span></span> | <span data-ttu-id="f6182-182">Value</span><span class="sxs-lookup"><span data-stu-id="f6182-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6182-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6182-183">Minimum supported client</span></span><br/> | <span data-ttu-id="f6182-184">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6182-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f6182-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6182-185">Minimum supported server</span></span><br/> | <span data-ttu-id="f6182-186">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6182-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6182-187">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6182-187">Namespace</span></span><br/>                | <span data-ttu-id="f6182-188">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f6182-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f6182-189">MOF</span><span class="sxs-lookup"><span data-stu-id="f6182-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6182-190"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6182-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6182-191">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6182-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6182-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6182-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f6182-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6182-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6182-194">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f6182-194">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="f6182-195">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="f6182-195">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)
</dt> </dl>

 

