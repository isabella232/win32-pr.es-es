---
description: La clase WMI de asociación SubDirectory de Win32 relaciona un directorio (carpeta) y uno de sus \_ subdirectorios (subcarpetas).
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Win32_SubDirectory clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubDirectory
- Win32_SubDirectory.GroupComponent
- Win32_SubDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 046de6ad1e09874351b37d58f7277126e39e990a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061475"
---
# <a name="win32_subdirectory-class"></a>Clase SubDirectory de Win32 \_

La **clase WMI de asociación \_ SubDirectory** [de](../wmisdk/retrieving-a-class.md) Win32 relaciona un directorio (carpeta) y uno de sus subdirectorios (subcarpetas).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a>Members

La **clase \_ SubDirectory de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SubDirectory de Win32** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Directorio Win32 \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Wmi \| Win32 \_ Directory")
</dt> </dl>

Referencia a la instancia de que representa las propiedades del directorio primario (carpeta) de esta asociación.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Directorio Win32 \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Directory")
</dt> </dl>

Referencia a la instancia de que representa la parte del subdirectorio (subcarpeta) de la asociación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ SubDirectory de Win32** se deriva del [**componente CIM \_**](cim-component.md).

Para devolver una colección de subcarpetas para una carpeta, cree una consulta de asociación que establece *ResultRole* en *PartComponent.* Esto indica que todos los elementos de la colección devuelta deben desempeñar el rol de partcomponente, o subcarpeta, del objeto de carpeta. Para devolver la carpeta primaria de una carpeta, establezca *ResultRole* en *GroupComponent.*

La **clase \_ SubDirectory de Win32** solo funciona en el nivel del sistema de archivos inmediatamente por encima o inmediatamente debajo de la carpeta especificada.

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de VBScript devuelve una lista de todas las subcarpetas dentro de la carpeta C: \\ Scripts.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSubfolders = objWMIService.ExecQuery _
 ("ASSOCIATORS OF {Win32_Directory.Name='c:\scripts'} " _
 & "WHERE AssocClass = Win32_Subdirectory " _
 & "ResultRole = PartComponent")
For Each objFolder in colSubfolders
 Wscript.Echo objFolder.Name
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Componente \_ CIM**](cim-component.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
