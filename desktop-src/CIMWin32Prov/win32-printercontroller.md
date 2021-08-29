---
description: La clase WMI de asociación PrinterController de Win32 relaciona una impresora y el dispositivo local al que \_ está conectada la impresora. Tenga en cuenta que esta clase solo devuelve instancias para impresoras locales.
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Win32_PrinterController clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterController
- Win32_PrinterController.AccessState
- Win32_PrinterController.Antecedent
- Win32_PrinterController.Dependent
- Win32_PrinterController.NegotiatedDataWidth
- Win32_PrinterController.NegotiatedSpeed
- Win32_PrinterController.NumberOfHardResets
- Win32_PrinterController.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f987ee23b3dd7b65ec391e88200e59c86055e49a5cda23be4c529500359e789c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759525"
---
# <a name="win32_printercontroller-class"></a>Clase PrinterController de Win32 \_

La clase WMI **de asociación \_ PrinterController** [de](../wmisdk/retrieving-a-class.md) Win32 relaciona una impresora y el dispositivo local al que está conectada la impresora. Tenga en cuenta que esta clase solo devuelve instancias para impresoras locales.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_PrinterController : CIM_ControlledBy
{
  uint16             AccessState;
  CIM_Controller REF Antecedent;
  Win32_Printer  REF Dependent;
  uint32             NegotiatedDataWidth;
  uint64             NegotiatedSpeed;
  uint32             NumberOfHardResets;
  uint32             NumberOfSoftResets;
};
```

## <a name="members"></a>Miembros

La **clase \_ PrinterController de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PrinterController de Win32** tiene estas propiedades.

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado del acceso del controlador al dispositivo. Esta información es necesaria cuando varios controladores pueden usar o acceder a un dispositivo lógico.

Esta propiedad se hereda de [**CIM \_ ControlledBy**](cim-controlledby.md).

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Unknown

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Active

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Inactivo

</dd> </dl>

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Controlador CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Referencia a la instancia [**del \_ controlador CIM**](cim-controller.md) que representa el dispositivo local asociado a esta impresora.

Esta propiedad se hereda de la [**dependencia \_ CIM**](cim-dependency.md).

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Impresora Win32 \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Referencia a la [**instancia de impresora Win32 \_**](win32-printer.md) que representa la impresora asociada al dispositivo local.

Esta propiedad se hereda de la [**dependencia \_ CIM**](cim-dependency.md).

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ancho de datos en uso entre dispositivos (cuando se pueden usar varios anchos de datos de bus o conexión). El ancho de los datos se especifica en bits. Si no se negocia el ancho de los datos, o si esta información no está disponible o no es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).

Esta propiedad se hereda de [**CIM \_ DeviceConnection.**](cim-deviceconnection.md)

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Velocidad en uso entre dispositivos (cuando son posibles varias velocidades de conexión o bus). La velocidad se especifica en bits por segundo. Si no se negocian las velocidades de conexión o bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).

Esta propiedad se hereda de [**CIM \_ DeviceConnection.**](cim-deviceconnection.md)

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](../wmisdk/creating-a-wmi-script.md)

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de restablecimientos de seguridad emitidos por el controlador.

Esta propiedad se hereda de [**CIM \_ ControlledBy**](cim-controlledby.md).

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de restablecimientos de programación emitidos por el controlador.

Esta propiedad se hereda de [**CIM \_ ControlledBy**](cim-controlledby.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ PrinterController de Win32** se deriva de [**CIM \_ ControlledBy**](cim-controlledby.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
