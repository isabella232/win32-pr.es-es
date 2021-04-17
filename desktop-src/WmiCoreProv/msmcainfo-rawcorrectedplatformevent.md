---
description: Contiene un evento de plataforma corregido (CPE). Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: b24a390e-293d-4dd4-b747-33c298a5d45f
title: MSMCAInfo_RawCorrectedPlatformEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCorrectedPlatformEvent
- MSMCAInfo_RawCorrectedPlatformEvent.Active
- MSMCAInfo_RawCorrectedPlatformEvent.Count
- MSMCAInfo_RawCorrectedPlatformEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 906587ca9ee153eb93542c3e749e8164e6a5ee7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716705"
---
# <a name="msmcainfo_rawcorrectedplatformevent-class"></a>MSMCAInfo \_ RawCorrectedPlatformEvent (clase)

La clase **MSMCAInfo \_ RawCorrectedPlatformEvent** contiene un evento de plataforma corregido (CPE). Esta clase solo está disponible en sistemas Windows de 64 bits.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAInfo_RawCorrectedPlatformEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Miembros

La clase **MSMCAInfo \_ RawCorrectedPlatformEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSMCAInfo \_ RawCorrectedPlatformEvent** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

TRUE si esta instancia de la clase está activa; en caso contrario, **false**.

</dd> <dt>

**Recuento**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de registros de error.

</dd> <dt>

**Registros**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **\_ entrada MSMCAInfo**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de registros de error de MCA. La propiedad **Count** especifica el número de registros de error de MCA en la matriz.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **MSMCAInfo \_ RawCorrectedPlatformEvent** se deriva de [**WMIEvent**](wmievent.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                         |
| Espacio de nombres<br/>                | \\WMI raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases MSMCA](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

 




