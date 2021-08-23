---
description: Indica una entrada de información de MCA, comprobación de máquina corregida (CMC) o error de plataforma corregido (CPE). Esta clase solo está disponible en sistemas de 64 Windows bits.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: MSMCAInfo_Entry clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 8f6146d629678c1ee209738095fea901f0edb865bccb9aff2d4eeab02d18e773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640914"
---
# <a name="msmcainfo_entry-class"></a>Clase Entry de MSMCAInfo \_

La clase Entry de **MSMCAInfo \_** indica una entrada de información de MCA, comprobación de máquina corregida (CMC) o error de plataforma corregido (CPE). Esta clase solo está disponible en sistemas de 64 Windows bits.

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a>Miembros

La **clase Entry \_ de MSMCAInfo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Entry de MSMCAInfo** tiene estas propiedades.

<dl> <dt>

**Datos**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de enteros que contiene un registro de error MCA completo según lo notificado por la capa de abstracción del sistema (SAL). La SAL está codificada en la ROM a la que llama el sistema operativo para realizar operaciones dependientes de la plataforma. Es similar al BIOS en una plataforma x86.

</dd> <dt>

**Duración**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de bytes en el registro de errores.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ Entry de MSMCAInfo** se deriva de [**MSMCAInfo**](msmcainfo.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases MSMCA](msmca-classes.md)
</dt> <dt>

[**MSMCAInfo**](msmcainfo.md)
</dt> </dl>

 

 




