---
description: La clase WMI de asociación PrinterDriverDll de Win32 relaciona una impresora \_ local y su archivo de controlador.
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Win32_PrinterDriverDll clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriverDll
- Win32_PrinterDriverDll.Antecedent
- Win32_PrinterDriverDll.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 884c52e388da62529a2aceb49c68ca888f18e0fd7701e05d951880774c3ed035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971865"
---
# <a name="win32_printerdriverdll-class"></a>Clase \_ PrinterDriverDll de Win32

La clase WMI **de asociación \_ PrinterDriverDll** [de](../wmisdk/retrieving-a-class.md) Win32 relaciona una impresora local y su archivo de controlador.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ PrinterDriverDll de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PrinterDriverDll de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ DataFile**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Referencia a la [**instancia \_ de Cim DataFile**](cim-datafile.md) que representa el archivo de controlador para esta Windows basada en datos.

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

Referencia a la [**instancia de \_ Impresora Win32.**](win32-printer.md)

Esta propiedad se hereda de la [**dependencia \_ CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ PrinterDriverDll de Win32** se deriva de [**la dependencia \_ CIM**](cim-dependency.md).

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

[**Dependencia \_ cim**](cim-dependency.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
