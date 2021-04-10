---
description: La \_ clase WMI de Asociación de subdirectorios de Win32 relaciona un directorio (carpeta) y uno de sus subdirectorios (subcarpetas).
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Win32_SubDirectory (clase)
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153345"
---
# <a name="win32_subdirectory-class"></a>\_Clase de subdirectorio Win32

La [clase WMI](../wmisdk/retrieving-a-class.md) de Asociación de **\_ subdirectorios de Win32** relaciona un directorio (carpeta) y uno de sus subdirectorios (subcarpetas).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a>Miembros

La clase de **\_ subdirectorio Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ subdirectorio Win32** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ directorio Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| directorio Win32 de WMI \_ ")
</dt> </dl>

Referencia a la instancia de que representa las propiedades del directorio primario (carpeta) en esta asociación.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ directorio Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| directorio Win32 de WMI \_ ")
</dt> </dl>

Referencia a la instancia de que representa la parte de subdirectorio (subcarpeta) de la asociación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase de **\_ subdirectorio Win32** se deriva [**del \_ componente CIM**](cim-component.md).

Para devolver una colección de subcarpetas de una carpeta, cree una consulta de asociación que establezca *ResultRole* en *PartComponent*. Esto indica que todos los elementos de la colección devuelta deben desempeñar el rol de un elemento PartComponent, o subcarpeta, del objeto Folder. Para devolver la carpeta principal de una carpeta, establezca *ResultRole* en *GroupComponent*.

La clase de **\_ subdirectorio Win32** solo funciona en el nivel de sistema de archivos inmediatamente superior o inmediatamente inferior a la carpeta especificada.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de VBScript se devuelve una lista de todas las subcarpetas de la carpeta C: \\ scripts.


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
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Componente CIM**](cim-component.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
