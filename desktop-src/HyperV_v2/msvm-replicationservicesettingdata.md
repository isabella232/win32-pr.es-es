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
# <a name="msvm_replicationservicesettingdata-class"></a>MSVM \_ ReplicationServiceSettingData (clase)

Representa la configuración para el servicio de replicación en un host de recuperación. Las propiedades de esta clase no se pueden modificar directamente. El cliente debe llamar al método [**MSVM \_ ReplicationService. ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) para modificar cualquiera de estas propiedades.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

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

## <a name="members"></a>Miembros

La clase **MSVM \_ ReplicationServiceSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ReplicationServiceSettingData** tiene estas propiedades.

<dl> <dt>

**AllowedAuthenticationType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Definir los modos de autenticación permitidos para conectarse al servidor host de recuperación.

<dt>

0
</dt> <dd>

Sin definir.

</dd> <dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Autenticación Kerberos** (1)


</dt> <dd>

Autenticación Kerberos.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticación basada en certificados** (2)


</dt> <dd>

Autenticación basada en certificados.

</dd> <dt>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Autenticación basada en certificados y autenticación Kerberos** (3)


</dt> <dd>

Autenticación basada en certificados y autenticación integrada.

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del servicio de replicación".

</dd> <dt>

**CertificateThumbPrint**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Huella digital del certificado que se usará cuando **AuthenticationType** sea autenticación basada en certificados.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "datos de configuración de replicación de máquina virtual".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del servicio de replicación".

</dd> <dt>

**HttpPort**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de puerto del servidor de recuperación que se va a usar al aceptar una conexión no segura para la replicación. El valor predeterminado es 80.

</dd> <dt>

**HttpsPort**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de puerto del servidor de recuperación que se va a usar al aceptar una conexión segura para la replicación. El valor predeterminado es 443.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**MonitoringInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Intervalo, en segundos, en el que se deben restablecer las estadísticas de replicación. El intervalo predeterminado es de 12 horas (43200 segundos). El valor válido mínimo es 60 minutos (3600 segundos) y el valor máximo válido es de 7 días (604800 segundos).

</dd> <dt>

**MonitoringStartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La hora de inicio de la supervisión de la replicación, en UTC. El valor predeterminado es 9:00 A.M., hora local, representada en UTC. Los elementos de fecha del objeto **DateTime** deben ser cero.

</dd> <dt>

**RecoveryServerEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si el host de Hyper-V está habilitado como servidor de recuperación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SettingData de CIM \_**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md)
</dt> </dl>

 

