---
description: La \_ clase WMI DriverForDevice Association de Win32 relaciona una instancia de impresora con una instancia del controlador de impresora.
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Win32_DriverForDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5fb384eed80c6a614af448477c50be3204d3080
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659673"
---
# <a name="win32_driverfordevice-class"></a>\_Clase Win32 DriverForDevice

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DriverForDevice** Association de Win32 relaciona una instancia de impresora con una instancia del controlador de impresora.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ DriverForDevice de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ DriverForDevice de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ impresora Win32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Referencia a la instancia de la [**\_ impresora Win32**](win32-printer.md) que representa la impresora.

Esta propiedad se hereda de [**la \_ dependencia CIM**](cim-dependency.md).

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ PrinterDriver**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la instancia de [**Win32 \_ PrinterDriver**](win32-printerdriver.md) que representa el controlador de impresora para la impresora.

Esta propiedad se hereda de [**la \_ dependencia CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ DriverForDevice de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).

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

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

