---
description: Representa el estado configurado del dispositivo TPM.
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Msvm_TPMSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TPMSettingData
- Msvm_TPMSettingData.Shielded
- Msvm_TPMSettingData.DataProtected
- Msvm_TPMSettingData.EnabledState
- Msvm_TPMSettingData.KeyProtector
- Msvm_TPMSettingData.LastKnownGoodKeyProtector
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f25cd57e1f3cd6ebf015009af176b3bcc68c1d271836c5bb548b9358e9007086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899125"
---
# <a name="msvm_tpmsettingdata-class"></a>Clase Msvm \_ TPMSettingData

Representa el estado configurado del dispositivo TPM.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TPMSettingData : CIM_ResourceAllocationSettingData
{
  boolean Shielded = FALSE;
  boolean DataProtected = FALSE;
  uint16  EnabledState = 3;
  uint8   KeyProtector[];
  uint8   LastKnownGoodKeyProtector[];
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ TPMSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ TPMSettingData** tiene estas propiedades.

<dl> <dt>

**DataProtected**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **requeridos**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para establecer una directiva para proteger los datos de una máquina virtual; de lo contrario, **false**. Un TPM recién creado está deshabilitado, por lo que el estado de protección de datos inicial es **false.**

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **requeridos**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Estados habilitados y deshabilitados de un elemento. El valor predeterminado es **Disabled.**

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**KeyProtector**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**
</dt> </dl>

Protector de clave del cliente del Servicio de protección de host.

</dd> <dt>

**LastKnownGoodKeyProtector**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**
</dt> </dl>

El último protector de clave correcto conocido ha cifrado correctamente el estado del dispositivo tpm en el último arranque de la máquina virtual.

Esta propiedad es de solo lectura para el cliente WMI y solo puede ser modificada por el dispositivo TPM de máquina virtual.

</dd> <dt>

**Blindada**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **requeridos**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para definir una directiva que blinda una máquina virtual; de lo contrario, **false**. Un TPM recién creado está deshabilitado, por lo que el estado de blindaje inicial es **false.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Fin de compatibilidad de cliente<br/>    | Windows 10<br/>                                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

