---
description: Representa el estado configurado de la configuración de seguridad para .
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Msvm_SecuritySettingData clase
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
ms.openlocfilehash: 22bc30db51b103f50eaa4deed7ca6f479c5f94600fbb15ef2a6f4bb36595d159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148157"
---
# <a name="msvm_securitysettingdata-class"></a>Clase \_ SecuritySettingData de Msvm

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

La **clase \_ SecuritySettingData de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SecuritySettingData de Msvm** tiene estas propiedades.

<dl> <dt>

**DataProtectionRequested**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorios**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para solicitar protección de datos para una máquina virtual; de lo contrario, **false**. El valor predeterminado es **false**.

</dd> <dt>

**EncryptStateAndVmMigrationTraffic**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorios**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para tener cifrado el estado y el tráfico de migración de una máquina virtual; de lo contrario, **false**. El valor predeterminado de una máquina virtual recién creada es **false.**

</dd> <dt>

**KsdEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorios**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para habilitar un dispositivo de almacenamiento de claves (KSD) para esta máquina virtual; de lo contrario, **false**. Una máquina virtual recién creada tiene un KSD de deshabilitación.

</dd> <dt>

**ShieldingRequested**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorios**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para solicitar el blindaje de una máquina virtual; de lo contrario, **false**. Una máquina virtual recién creada tiene un estado inicial de blindaje solicitado de **false.**

</dd> <dt>

**TpmEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorios**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para habilitar un nódulo de plataforma de confianza (TPM) para esta máquina virtual; de lo contrario, **false**. Una máquina virtual recién creada tiene un TPM de deshabilitación.

</dd> <dt>

**VirtualizationBasedSecurityOptOut**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorios**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para no ofrecer una seguridad basada en virtualización de máquinas virtuales; de lo contrario, **false**. La configuración predeterminada para el estado de exclusión de una máquina virtual recién creada es **false.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

