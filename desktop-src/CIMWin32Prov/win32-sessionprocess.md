---
description: La clase WMI de asociación SessionProcess de Win32 representa una asociación entre una sesión de inicio de sesión \_ y los procesos asociados a esa sesión.
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Win32_SessionProcess clase
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
ms.openlocfilehash: f31473cf1efa0310669523f0481b58d8b54036f738a69191f19a0a52d804eb05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118416820"
---
# <a name="win32_sessionprocess-class"></a>Clase SessionProcess de Win32 \_

La clase WMI **de asociación \_ SessionProcess** [de](../wmisdk/retrieving-a-class.md) Win32 representa una asociación entre una sesión de inicio de sesión y los procesos asociados a esa sesión.

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

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedente"), [**Key**](../wmisdk/key-qualifier.md)
</dt> </dl>

Una [**\_ LogonSession de Win32**](win32-logonsessionmappeddisk.md) que representa la sesión que está relacionada con el proceso.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Proceso win32 \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**Key**](../wmisdk/key-qualifier.md)
</dt> </dl>

Proceso [**win32 \_ que**](win32-processor.md) representa el proceso asociado a la sesión.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**Win32 \_ SessionProcess** devuelve toda la sesión del administrador cuando se inicia sesión con privilegios elevados o cuando se ejecuta de forma remota. Se trata de una extensión para el comportamiento de la clase .

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

[**SessionResource de Win32 \_**](win32-sessionresource.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
