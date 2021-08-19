---
description: Asocia un dispositivo de almacenamiento al controlador de almacenamiento que posee el dispositivo.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Msvm_ControlledBy clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b08cf97c54363009e839ea78fe139c6c8a1bdd81cac07182d019d3d00857dee4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130605"
---
# <a name="msvm_controlledby-class"></a>Clase Msvm \_ ControlledBy

Asocia un dispositivo de almacenamiento al controlador de almacenamiento que posee el dispositivo. Esta asociación se usa con ide y disquetes.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ ControlledBy** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ ControlledBy** tiene estas propiedades.

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Accesibilidad del dispositivo a través del controlador antecedente. Esta propiedad se hereda de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)y siempre se establece en 2 (lectura/escritura).

</dd> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Prioridad dada a los accesos del dispositivo a través de este controlador. La ruta de acceso de prioridad más alta tendrá el valor más bajo. Esta propiedad se hereda de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)y siempre se establece en 0.

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el controlador está comandando activamente o accediendo al dispositivo. Esta propiedad se hereda de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)y siempre se establece en 1 (activo).

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Controlador CIM \_**](/windows/desktop/CIMWin32Prov/cim-controller)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al controlador. Esta propiedad se hereda de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ Cim LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al dispositivo controlado. Esta propiedad se hereda de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección del dispositivo asociado en el contexto del controlador antecedente. Esta propiedad se hereda de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)y siempre se establece en 0.

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)y siempre se establece en 0.

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), pero no se usa.

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), pero no se usa.

</dd> <dt>

**TimeOfDeviceReset**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), pero no se usa.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase Msvm \_ ControlledBy** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dt>

[**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[Storage Clases](storage-classes.md)
</dt> </dl>

 

