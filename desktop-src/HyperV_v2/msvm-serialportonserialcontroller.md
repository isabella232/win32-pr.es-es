---
description: Asocia un puerto serie a un controlador serie.
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Msvm_SerialPortOnSerialController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 357192bfb3dc4e901dd40a0cb6d7884152c3afc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908191"
---
# <a name="msvm_serialportonserialcontroller-class"></a>MSVM \_ SerialPortOnSerialController (clase)

Asocia un puerto serie a un controlador serie.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ SerialPortOnSerialController** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ SerialPortOnSerialController** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Controlador serie al que está conectado el puerto. Esta propiedad se hereda de [**\_ PortOnDevice CIM**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Puerto del controlador serie. Esta propiedad se hereda de [**\_ PortOnDevice CIM**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ SerialPortOnSerialController** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_PORTONDEVICE CIM**](cim-portondevice.md)
</dt> <dt>

[**\_PORTONDEVICE CIM**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[Clases de dispositivos serie](serial-devices-classes.md)
</dt> </dl>

 

