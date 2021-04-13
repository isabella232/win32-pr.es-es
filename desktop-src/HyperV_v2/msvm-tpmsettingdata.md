---
description: Representa el estado configurado del dispositivo TPM.
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Msvm_TPMSettingData (clase)
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
ms.openlocfilehash: 8a14f50f01212129ed34cc7e45ee28facbdb991f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543582"
---
# <a name="msvm_tpmsettingdata-class"></a>MSVM \_ TPMSettingData (clase)

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

La clase **MSVM \_ TPMSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ TPMSettingData** tiene estas propiedades.

<dl> <dt>

**DataProtector**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para establecer una directiva que proteja los datos de una máquina virtual; en caso contrario, **false**. Un TPM recién creado está deshabilitado, por lo que el estado inicial de protección de datos es **false**.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Estados habilitado y deshabilitado de un elemento. El valor predeterminado es **Disabled**.

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

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**
</dt> </dl>

El protector de clave del cliente del servicio de protección de host.

</dd> <dt>

**LastKnownGoodKeyProtector**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**
</dt> </dl>

El último protector de clave válida conocida cifró correctamente el estado del dispositivo de TPM en el último arranque de la máquina virtual.

Esta propiedad es de solo lectura para el cliente WMI y solo la puede modificar el dispositivo TPM de la máquina virtual.

</dd> <dt>

**Blindada**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para definir una directiva que blinda una máquina virtual; en caso contrario, **false**. Un TPM recién creado está deshabilitado, por lo que el estado de blindaje inicial es **false**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Fin de compatibilidad de cliente<br/>    | Windows 10<br/>                                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

