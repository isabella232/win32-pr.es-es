---
description: La \_ clase WMI ShareToDirectory Association de Win32 relaciona un recurso compartido en el sistema del equipo y el directorio al que está asignado.
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Win32_ShareToDirectory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShareToDirectory
- Win32_ShareToDirectory.Share
- Win32_ShareToDirectory.SharedElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f02e5e1ce125a2c8495327a08c14c94ac9f48567
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807016"
---
# <a name="win32_sharetodirectory-class"></a>\_Clase Win32 ShareToDirectory

La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ ShareToDirectory** Association de Win32 relaciona un recurso compartido en el sistema del equipo y el directorio al que está asignado.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{8502C511-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ShareToDirectory
{
  Win32_Share   REF Share;
  CIM_Directory REF SharedElement;
};
```

## <a name="members"></a>Miembros

La **clase \_ ShareToDirectory de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ShareToDirectory de Win32** tiene estas propiedades.

<dl> <dt>

**Compartir**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ recurso compartido de Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ share")
</dt> </dl>

Referencia a la instancia de que representa las propiedades de un recurso compartido disponible a través del directorio.

</dd> <dt>

**SharedElement**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ directorio CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| directorio CIM CIM \_ ")
</dt> </dl>

Referencia a la instancia de que representa las propiedades del directorio que se ha asignado a un recurso compartido.

</dd> </dl>

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

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
