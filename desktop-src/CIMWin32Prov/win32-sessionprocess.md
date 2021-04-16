---
description: La \_ clase WMI SessionProcess Association de Win32 representa una asociación entre una sesión de inicio de sesión y los procesos asociados a esa sesión.
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Win32_SessionProcess (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4090da88e8f5d31b0940b0c7d217a930a364b63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659355"
---
# <a name="win32_sessionprocess-class"></a>\_Clase Win32 SessionProcess

La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SessionProcess** Association de Win32 representa una asociación entre una sesión de inicio de sesión y los procesos asociados a esa sesión.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ SessionProcess de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SessionProcess de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ LogonSession**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidar**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**clave**](../wmisdk/key-qualifier.md)
</dt> </dl>

[**\_ LogonSession de Win32**](win32-logonsessionmappeddisk.md) que representa la sesión relacionada con el proceso.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ proceso Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidar**](../wmisdk/standard-qualifiers.md) ("dependiente"), [**clave**](../wmisdk/key-qualifier.md)
</dt> </dl>

[**\_ Proceso de Win32**](win32-processor.md) que representa el proceso asociado a la sesión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**Win32 \_ SessionProcess** devuelve todas las sesiones para el administrador cuando se inicia sesión con privilegios elevados o cuando se ejecuta de forma remota. Se trata de una extensión del comportamiento de la clase.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ SessionResource**](win32-sessionresource.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
