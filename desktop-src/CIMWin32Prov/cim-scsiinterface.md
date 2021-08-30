---
description: Representa una relación ControlledBy de CIM que indica a qué dispositivos se accede a través de \_ un controlador SCSI y las características de acceso.
ms.assetid: a036dbf9-f9ce-4c85-9184-fefcbe4583ba
ms.tgt_platform: multiple
title: CIM_SCSIInterface clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIInterface
- CIM_SCSIInterface.NegotiatedDataWidth
- CIM_SCSIInterface.NegotiatedSpeed
- CIM_SCSIInterface.AccessState
- CIM_SCSIInterface.NumberOfHardResets
- CIM_SCSIInterface.NumberOfSoftResets
- CIM_SCSIInterface.Dependent
- CIM_SCSIInterface.Antecedent
- CIM_SCSIInterface.SCSIRetries
- CIM_SCSIInterface.SCSITimeouts
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f9015c68504eaeda9bf4ea89e306aaa4c0efe2808f5cf419bfcccbe93207ead7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920015"
---
# <a name="cim_scsiinterface-class"></a>Cim \_ SCSIInterface (clase)

La **clase \_ CIM SCSIInterface** representa una relación [**\_ ControlledBy**](cim-controlledby.md) de CIM que indica a qué dispositivos se accede a través de un controlador SCSI y las características de acceso.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{7CE7448E-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SCSIInterface : CIM_ControlledBy
{
  uint32                 NegotiatedDataWidth;
  uint64                 NegotiatedSpeed;
  uint16                 AccessState;
  uint32                 NumberOfHardResets;
  uint32                 NumberOfSoftResets;
  CIM_LogicalDevice  REF Dependent;
  CIM_SCSIController REF Antecedent;
  uint32                 SCSIRetries;
  uint32                 SCSITimeouts;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM SCSIInterface** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM SCSIInterface** tiene estas propiedades.

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el controlador está comandando activamente o accediendo al dispositivo. Esta información es necesaria cuando varios controladores pueden usar o acceder a un dispositivo lógico.

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

Tipo de datos: **CIM \_ SCSIController**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

[**\_ SCSIController CIM**](cim-scsicontroller.md) que describe el controlador SCSI.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Un [**\_ dispositivo lógico CIM**](cim-logicaldevice.md) que describe el dispositivo lógico.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Cuando son posibles varios anchos de datos de conexión o bus, esta propiedad define el que se usa entre los dispositivos. El ancho de datos se especifica en bits. Si no se negocia el ancho de datos o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).

Esta propiedad se hereda de [**CIM \_ DeviceConnection.**](cim-deviceconnection.md)

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")
</dt> </dl>

Cuando son posibles varias velocidades de conexión o bus, esta propiedad define la que se usa entre los dispositivos. La velocidad se especifica en bits por segundo. Si no se negocian las velocidades de conexión o bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Esta propiedad se hereda de [**CIM \_ DeviceConnection.**](cim-deviceconnection.md)

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de restablecimientos de seguridad emitidos por el controlador. Un restablecimiento duro devuelve el dispositivo a su estado de inicialización o arranque. Se pierden toda la información y los datos internos del estado del dispositivo.

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

</dd> <dt>

**SCSIRetries**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de reintentos SCSI que se han producido desde el último restablecimiento duro o flexible relacionado con el dispositivo controlado. La hora del último restablecimiento se indica en la **propiedad TimeOfDeviceReset,** heredada de la [**asociación \_ ControlledBy de CIM.**](cim-controlledby.md)

</dd> <dt>

**SCSITimeouts**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de tiempos de espera SCSI que se produjeron desde el último restablecimiento duro o flexible relacionado con el dispositivo controlado. La hora del último restablecimiento se indica en la **propiedad TimeOfDeviceReset,** heredada de la [**asociación \_ ControlledBy de CIM.**](cim-controlledby.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ CIM SCSIInterface** se deriva de [**CIM \_ ControlledBy**](cim-controlledby.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> </dl>

 

