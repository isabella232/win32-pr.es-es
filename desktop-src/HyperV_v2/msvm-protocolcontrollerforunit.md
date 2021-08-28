---
description: Esta asociación indica que una subclase de dispositivo lógico (por ejemplo, un volumen de almacenamiento) está conectada a través de un controlador de protocolo específico.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Msvm_ProtocolControllerForUnit clase
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
ms.openlocfilehash: 73b8478e561d53212e0439219622595751ad954e13d0d086fabdbf57a483039d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086635"
---
# <a name="msvm_protocolcontrollerforunit-class"></a>Clase Msvm \_ ProtocolControllerForUnit

Esta asociación indica que una subclase de dispositivo lógico (por ejemplo, un volumen de almacenamiento) está conectada a través de un controlador de protocolo específico. En muchas situaciones (por ejemplo, el enmascaramiento de LUN de almacenamiento), puede haber muchas de estas asociaciones usadas para relacionarse con objetos diferentes. Por lo tanto, se han definido subclases para optimizar la enumeración de las asociaciones.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

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

La **clase Msvm \_ ProtocolControllerForUnit** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ ProtocolControllerForUnit** tiene estas propiedades.

<dl> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Prioridad dada a los accesos del dispositivo a través de este controlador. La ruta de acceso de prioridad más alta tendrá el valor más bajo para este parámetro. Esta clase se hereda de **CIM \_ ProtocolControllerForDevice**.

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el controlador está comandoando activamente o accediendo al dispositivo (2) o no (3). Además, se puede definir el valor 0 (desconocido). Esta información es necesaria cuando varios controladores de protocolo pueden usar o acceder a un dispositivo lógico. Esta clase se hereda de **CIM \_ ProtocolControllerForDevice**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Activo** (2)
</dt> <dt>

<span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inactivo** (3 )
</dt> </dl>

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Controlador de protocolo. Esta clase se hereda de la [**dependencia \_ CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El dispositivo controlado. Esta clase se hereda de la [**dependencia \_ CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**DeviceAccess**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Derechos de acceso concedidos al dispositivo a través de este controlador. Esta clase se hereda de **CIM \_ ProtocolControllerForUnit.**



| Value                                                                               | Significado                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>        | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>        | Lectura/Escritura<br/>      |
| <dl> <dt>3</dt> </dl>        | Solo lectura<br/>       |
| <dl> <dt>4</dt> </dl>        | Sin acceso.<br/>      |
| <dl> <dt>5..15999</dt> </dl> | DMTF reservado<br/>   |
| <dl> <dt>16000..</dt> </dl>  | Proveedor reservado<br/> |



 

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección del dispositivo asociado en el contexto del controlador antecedente. Esta clase se hereda de **CIM \_ ProtocolControllerForDevice**.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ Msvm ProtocolControllerForUnit** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ ProtocolControllerForUnit**](cim-protocolcontrollerforunit.md)
</dt> <dt>

[**CIM \_ ProtocolControllerForUnit**](/previous-versions//cc150672(v=vs.85))
</dt> <dt>

[Storage Clases](storage-classes.md)
</dt> </dl>

 

