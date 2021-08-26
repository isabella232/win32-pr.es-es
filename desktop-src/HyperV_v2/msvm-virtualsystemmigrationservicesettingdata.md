---
description: Representa la configuración del servicio de migración del sistema virtual en un host.
ms.assetid: 56711134-9a4a-49bd-8a0e-ce679b959adf
title: Msvm_VirtualSystemMigrationServiceSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingData
- Msvm_VirtualSystemMigrationServiceSettingData.InstanceID
- Msvm_VirtualSystemMigrationServiceSettingData.Caption
- Msvm_VirtualSystemMigrationServiceSettingData.Description
- Msvm_VirtualSystemMigrationServiceSettingData.ElementName
- Msvm_VirtualSystemMigrationServiceSettingData.EnableVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveStorageMigration
- Msvm_VirtualSystemMigrationServiceSettingData.AuthenticationType
- Msvm_VirtualSystemMigrationServiceSettingData.EnableCompression
- Msvm_VirtualSystemMigrationServiceSettingData.EnableSmbTransport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9ab3feab1f34d0f44ce5cd0618915d8575af9e463a9ec772961c185e946ac094
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963505"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a>Clase Msvm \_ VirtualSystemMigrationServiceSettingData

Representa la configuración del servicio de migración del sistema virtual en un host. Las propiedades de esta clase no se pueden modificar directamente. El cliente debe llamar al **método Msvm \_ VirtualSystemMigrationService.ModifyServiceSettings** para modificar cualquiera de estas propiedades.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  boolean EnableVirtualSystemMigration;
  uint32  MaximumActiveVirtualSystemMigration;
  uint32  MaximumActiveStorageMigration;
  uint32  AuthenticationType;
  boolean EnableCompression = True;
  boolean EnableSmbTransport = False;
};
```

## <a name="members"></a>Miembros

La **clase \_ VirtualSystemMigrationServiceSettingData de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ VirtualSystemMigrationServiceSettingData** tiene estas propiedades.

<dl> <dt>

**AuthenticationType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el mecanismo de autenticación utilizado para las conexiones de red de migración de sistema virtual. Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) de la clase [**\_ Msvm VirtualSystemMigrationService.**](msvm-virtualsystemmigrationservice.md)

<dt>

<span id="CredSSP"></span><span id="credssp"></span><span id="CREDSSP"></span>

**CredSSP** (0)


</dt> <dd></dd> <dt>

<span id="Kerberos"></span><span id="kerberos"></span><span id="KERBEROS"></span>

**Kerberos** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de la [**clase \_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**EnableCompression**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si la compresión del tráfico de migración en vivo está habilitada o deshabilitada. True indica habilitado.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**EnableSmbTransport**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si el uso de SMB como tipo de transporte para transferir el estado de la máquina virtual entre los hosts de Hyper-V durante la migración del sistema virtual está habilitado o deshabilitado. **True** indica habilitado. Se consigue un mayor rendimiento si las NIC RDMA están configuradas para el transporte SMB durante la migración en vivo de la máquina virtual. Si **el valor enableSmbTransport** es true, se omite el valor de **EnableCompression.**

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**EnableVirtualSystemMigration**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si la migración del sistema virtual está habilitada o deshabilitada. Storage la migración siempre está habilitada. Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) de la clase [**\_ Msvm VirtualSystemMigrationService.**](msvm-virtualsystemmigrationservice.md)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**MaximumActiveStorageMigration**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el número máximo de migraciones de almacenamiento activas permitidas. Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) de la clase [**\_ Msvm VirtualSystemMigrationService.**](msvm-virtualsystemmigrationservice.md)

</dd> <dt>

**MaximumActiveVirtualSystemMigration**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el número máximo de migraciones activas del sistema virtual permitidas. Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) de la clase [**\_ Msvm VirtualSystemMigrationService.**](msvm-virtualsystemmigrationservice.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

