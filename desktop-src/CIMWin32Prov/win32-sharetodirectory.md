---
description: La clase WMI de asociación ShareToDirectory de Win32 relaciona un recurso compartido en el sistema del equipo y el directorio al \_ que está asignado.
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Win32_ShareToDirectory clase
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
ms.openlocfilehash: d041209dcdbd1d9a39d08acb75180ec9cf292f01934c21762418571d44a32460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917545"
---
# <a name="win32_sharetodirectory-class"></a>Clase ShareToDirectory de Win32 \_

La clase [WMI](../wmisdk/retrieving-a-class.md) de asociación **\_ ShareToDirectory de Win32** relaciona un recurso compartido en el sistema del equipo y el directorio al que está asignado.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

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

Tipo de datos: **Recurso compartido \_ win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Recurso \| compartido win32 de \_ WMI")
</dt> </dl>

Referencia a la instancia de que representa las propiedades de un recurso compartido disponible a través del directorio .

</dd> <dt>

**SharedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **Directorio CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| \_ Directory")
</dt> </dl>

Referencia a la instancia de que representa las propiedades del directorio que se ha asignado a un recurso compartido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
