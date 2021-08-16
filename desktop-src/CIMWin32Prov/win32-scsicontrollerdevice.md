---
description: La clase WMI de asociación SCSIControllerDevice de Win32 relaciona un controlador pequeño de interfaz del sistema informático (SCSI) y el dispositivo lógico \_ (unidad de disco) conectado a él.
ms.assetid: 0334829c-3625-4acf-8ef3-da934c51e9bf
ms.tgt_platform: multiple
title: Win32_SCSIControllerDevice clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIControllerDevice
- Win32_SCSIControllerDevice.NegotiatedDataWidth
- Win32_SCSIControllerDevice.NegotiatedSpeed
- Win32_SCSIControllerDevice.AccessState
- Win32_SCSIControllerDevice.NumberOfHardResets
- Win32_SCSIControllerDevice.NumberOfSoftResets
- Win32_SCSIControllerDevice.Antecedent
- Win32_SCSIControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f703d5a290245b1596801f78c005c565faa45296c3582e4feaad5dc4011787b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117834176"
---
# <a name="win32_scsicontrollerdevice-class"></a>Clase \_ SCSIControllerDevice de Win32

La clase [WMI](../wmisdk/retrieving-a-class.md) de asociación **\_ SCSIControllerDevice de Win32** relaciona un controlador pequeño de interfaz del sistema informático (SCSI) y el dispositivo lógico (unidad de disco) conectado a él.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{CC0F48D2-C847-11d2-911E-0060081A46FD}"), AMENDMENT]
class Win32_SCSIControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_SCSIController REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ SCSIControllerDevice de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SCSIControllerDevice de Win32** tiene estas propiedades.

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el controlador está comandoando activamente o accediendo al dispositivo. Esta información es necesaria cuando varios controladores pueden usar o acceder a un dispositivo lógico.

Esta propiedad se hereda de [**CIM \_ ControlledBy**](cim-controlledby.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

**Activo** (1)


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

**Inactivo** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ SCSIController**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| Win32 \_ SCSIController")
</dt> </dl>

La [**referencia anterior a \_ SCSIController de Win32**](win32-scsicontroller.md) representa la controladora SCSI asociada a este dispositivo.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| \_ LogicalDevice")
</dt> </dl>

La [**referencia dependiente del \_ dispositivo**](cim-logicaldevice.md) lógico CIM representa el dispositivo lógico conectado a la controladora SCSI.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits")
</dt> </dl>

Cuando son posibles varios anchos de datos de conexión o bus, esta propiedad define el que se usa entre los dispositivos. El ancho de los datos se especifica en bits. Si no se negocia el ancho de los datos, o si esta información no está disponible o no es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).

Esta propiedad se hereda de [**CIM \_ DeviceConnection.**](cim-deviceconnection.md)

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")
</dt> </dl>

Cuando son posibles varias velocidades de conexión o bus, esta propiedad define la que se usa entre los dispositivos. La velocidad se especifica en bits por segundo. Si no se negocian las velocidades de conexión o bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](../wmisdk/creating-a-wmi-script.md)

Esta propiedad se hereda de [**CIM \_ DeviceConnection.**](cim-deviceconnection.md)

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de restablecimientos de seguridad emitidos por el controlador. Un restablecimiento de seguridad devuelve el dispositivo a su estado de inicialización o arranque. Se pierden toda la información y los datos internos del estado del dispositivo.

Esta propiedad se hereda de [**CIM \_ ControlledBy**](cim-controlledby.md).

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de restablecimientos de programación emitidos por el controlador. Un restablecimiento de programación no borra completamente el estado y los datos actuales del dispositivo. La semántica exacta depende del dispositivo y de los protocolos y mecanismos que se usan para comunicarse con él.

Esta propiedad se hereda de [**CIM \_ ControlledBy**](cim-controlledby.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ SCSIControllerDevice de Win32** se deriva de [**CIM \_ ControlledBy**](cim-controlledby.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
