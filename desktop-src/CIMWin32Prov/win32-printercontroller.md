---
description: La \_ clase WMI PrinterController Association de Win32 relaciona una impresora y el dispositivo local al que está conectada la impresora. Tenga en cuenta que esta clase solo devuelve instancias para las impresoras locales.
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Win32_PrinterController (clase)
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
ms.openlocfilehash: 1ee38b827aed2dfffe1e7ef4f5049b16eee50791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907255"
---
# <a name="win32_printercontroller-class"></a>\_Clase Win32 PrinterController

La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterController** Association de Win32 relaciona una impresora y el dispositivo local al que está conectada la impresora. Tenga en cuenta que esta clase solo devuelve instancias para las impresoras locales.

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

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado del controlador acceso al dispositivo. Esta información es necesaria cuando se puede realizar el comando de un dispositivo lógico, o bien a través de varios controladores.

Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


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

Tipo de datos **: \_ controlador CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Referencia a la instancia del [**\_ controlador CIM**](cim-controller.md) que representa el dispositivo local asociado a esta impresora.

Esta propiedad se hereda de [**la \_ dependencia CIM**](cim-dependency.md).

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ impresora Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Referencia a la instancia de la [**\_ impresora de Win32**](win32-printer.md) que representa la impresora asociada al dispositivo local.

Esta propiedad se hereda de [**la \_ dependencia CIM**](cim-dependency.md).

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ancho de datos en uso entre dispositivos (cuando son posibles varios anchos de datos de bus o conexión). El ancho de los datos se especifica en bits. Si no se negocia el ancho de los datos, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).

Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Velocidad de uso entre dispositivos (cuando se pueden realizar varias velocidades de conexión o bus). La velocidad se especifica en bits por segundo. Si no se negocian las velocidades de conexión o de bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).

Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de restablecimientos fuertes emitidos por el controlador.

Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de restablecimientos flexibles emitidos por el controlador.

Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ PrinterController de Win32** se deriva de [**\_ ControlledBy de CIM**](cim-controlledby.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ printer. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
