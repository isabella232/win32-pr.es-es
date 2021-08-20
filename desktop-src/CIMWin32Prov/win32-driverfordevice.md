---
description: La clase WMI de asociación DriverForDevice de Win32 relaciona una instancia \_ de impresora con una instancia de controlador de impresora.
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Win32_DriverForDevice clase
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
ms.openlocfilehash: f55025c84b8ab7e7114f5a1746d84f8fbdb6b0a7dfe952abfe84efb980430881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546325"
---
# <a name="win32_driverfordevice-class"></a>Clase DriverForDevice de Win32 \_

La **clase WMI de asociación \_ DriverForDevice** [de](/windows/desktop/WmiSdk/retrieving-a-class) Win32 relaciona una instancia de impresora con una instancia de controlador de impresora.

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

Tipo de datos: **Impresora Win32 \_**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Referencia a la [**instancia de \_ Impresora Win32**](win32-printer.md) que representa la impresora.

Esta propiedad se hereda de la [**dependencia \_ CIM**](cim-dependency.md).

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ PrinterDriver**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la [**instancia de Win32 \_ PrinterDriver**](win32-printerdriver.md) que representa el controlador de impresora para la impresora.

Esta propiedad se hereda de la [**dependencia \_ CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ DriverForDevice de Win32** se deriva de [**la dependencia \_ CIM**](cim-dependency.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

