---
description: Esta asociación indica que una subclase del dispositivo lógico (por ejemplo, un volumen de almacenamiento) está conectada a través de un controlador de protocolo específico.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Msvm_ProtocolControllerForUnit (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1470192fc4f10e60bdfef013146483b47cbfa7f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687267"
---
# <a name="msvm_protocolcontrollerforunit-class"></a>MSVM \_ ProtocolControllerForUnit (clase)

Esta asociación indica que una subclase del dispositivo lógico (por ejemplo, un volumen de almacenamiento) está conectada a través de un controlador de protocolo específico. En muchas situaciones (por ejemplo, el enmascaramiento de LUN de almacenamiento), es posible que haya muchas de estas asociaciones utilizadas para relacionar los distintos objetos. Por lo tanto, se han definido subclases para optimizar la enumeración de las asociaciones.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ ProtocolControllerForUnit** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ProtocolControllerForUnit** tiene estas propiedades.

<dl> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La prioridad dada para acceder al dispositivo a través de este controlador. La ruta de acceso de prioridad más alta tendrá el valor más bajo para este parámetro. Esta clase se hereda de **\_ ProtocolControllerForDevice CIM**.

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el controlador está activamente realizando comandos o accediendo al dispositivo (2) o no (3). Además, se puede definir el valor 0 (desconocido). Esta información es necesaria cuando un dispositivo lógico puede ser comando por varios controladores de protocolo o tener acceso a ellos a través de ellos. Esta clase se hereda de **\_ ProtocolControllerForDevice CIM**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Activo** (2)
</dt> <dt>

<span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inactivo** (3)
</dt> </dl>

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El controlador de protocolo. Esta clase se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El dispositivo controlado. Esta clase se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**DeviceAccess**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los derechos de acceso concedidos al dispositivo a través de este controlador. Esta clase se hereda de **\_ ProtocolControllerForUnit CIM**.



| Value                                                                               | Significado                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>        | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>        | Lectura/Escritura<br/>      |
| <dl> <dt>3</dt> </dl>        | Solo lectura<br/>       |
| <dl> <dt>4</dt> </dl>        | Sin acceso.<br/>      |
| <dl> <dt>5.. 15999</dt> </dl> | DMTF reservado<br/>   |
| <dl> <dt>16000..</dt> </dl>  | Proveedor reservado<br/> |



 

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La dirección del dispositivo asociado en el contexto del controlador antecedente. Esta clase se hereda de **\_ ProtocolControllerForDevice CIM**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ ProtocolControllerForUnit** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_PROTOCOLCONTROLLERFORUNIT CIM**](cim-protocolcontrollerforunit.md)
</dt> <dt>

[**\_PROTOCOLCONTROLLERFORUNIT CIM**](/previous-versions//cc150672(v=vs.85))
</dt> <dt>

[Clases de almacenamiento](storage-classes.md)
</dt> </dl>

 

