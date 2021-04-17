---
description: La \_ clase WMI DiskDriveToDiskPartition Association de Win32 relaciona una unidad de disco y una partición existente.
ms.assetid: 82953097-ebfb-42b8-84b4-fb4ed19f3525
ms.tgt_platform: multiple
title: Win32_DiskDriveToDiskPartition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDriveToDiskPartition
- Win32_DiskDriveToDiskPartition.Antecedent
- Win32_DiskDriveToDiskPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2bd5472bd4ad92ddde47f7d6a492916006a80cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659676"
---
# <a name="win32_diskdrivetodiskpartition-class"></a>\_Clase Win32 DiskDriveToDiskPartition

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DiskDriveToDiskPartition** Association de Win32 relaciona una unidad de disco y una partición existente.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDriveToDiskPartition : CIM_MediaPresent
{
  Win32_DiskDrive     REF Antecedent;
  Win32_DiskPartition REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ DiskDriveToDiskPartition de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ DiskDriveToDiskPartition de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ DiskDrive**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskDrive")
</dt> </dl>

Referencia a la instancia de que representa las propiedades de la unidad de disco en la que existe la partición.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ DiskPartition**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskPartition")
</dt> </dl>

Referencia a la instancia de que representa la partición de disco que reside en la unidad de disco.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ DiskDriveToDiskPartition de Win32** se deriva de [**\_ MediaPresent de CIM**](cim-mediapresent.md).

Para obtener una explicación sobre cómo usar esta clase, consulte los artículos de blog [uso de PowerShell para asignar unidades de disco y particiones](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) , y de [cómo se pueden poner en correlación unidades lógicas y discos físicos](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) .

## <a name="examples"></a>Ejemplos

En el ejemplo de PowerShell [usar PowerShell para recopilar información de puntos de montaje y de disco, partición o punto de montaje](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) se usa **Win32 \_ DiskDriveToDiskPartition** para devolver información acerca de los discos locales, las particiones y los puntos de montaje.

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

[**\_MEDIAPRESENT CIM**](cim-mediapresent.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[Tareas de WMI: discos y sistemas de archivos](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

