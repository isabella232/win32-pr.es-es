---
description: Representa el estado configurado de la configuración de seguridad para.
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Msvm_SecuritySettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7125e06ad4ce33e70a8cf84b24933e7390e7a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687629"
---
# <a name="msvm_securitysettingdata-class"></a>MSVM \_ SecuritySettingData (clase)

Representa el estado configurado de la configuración de seguridad de una máquina virtual.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ SecuritySettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ SecuritySettingData** tiene estas propiedades.

<dl> <dt>

**DataProtectionRequested**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para solicitar protección de datos para una máquina virtual; en caso contrario, **false**. El valor predeterminado es **false**.

</dd> <dt>

**EncryptStateAndVmMigrationTraffic**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para que el estado y el tráfico de migración de una máquina virtual estén cifrados; en caso contrario, **false**. El valor predeterminado de una máquina virtual recién creada es **falso**.

</dd> <dt>

**KsdEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para habilitar un dispositivo de almacenamiento de claves (KSD) para esta máquina virtual; en caso contrario, **false**. Una máquina virtual recién creada tiene deshabilitada la KSD.

</dd> <dt>

**ShieldingRequested**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para solicitar el blindaje de una máquina virtual; en caso contrario, **false**. Una máquina virtual recién creada tiene un estado de blindaje solicitado de **falso**.

</dd> <dt>

**TpmEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para habilitar un Nodule de plataforma segura (TPM) para esta máquina virtual; en caso contrario, **false**. Una máquina virtual recién creada tiene deshabilitado TPM.

</dd> <dt>

**VirtualizationBasedSecurityOptOut**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para no ofrecer una seguridad basada en la virtualización de máquinas virtuales; en caso contrario, **false**. La configuración predeterminada para el estado de cancelación de una máquina virtual recién creada es **false**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SettingData de CIM \_**](cim-settingdata.md)
</dt> </dl>

 

