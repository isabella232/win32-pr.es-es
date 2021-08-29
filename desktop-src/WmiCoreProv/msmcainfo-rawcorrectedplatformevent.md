---
description: Contiene un evento de plataforma corregido (CPE). Esta clase solo está disponible en sistemas de 64 Windows bits.
ms.assetid: b24a390e-293d-4dd4-b747-33c298a5d45f
title: MSMCAInfo_RawCorrectedPlatformEvent clase
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
ms.openlocfilehash: 9da5da0cbbde9f7319482e5f8574f62ac311535d277e08f3f7884134b1fa3475
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097415"
---
# <a name="msmcainfo_rawcorrectedplatformevent-class"></a>Clase RawCorrectedPlatformEvent de MSMCAInfo \_

La **clase \_ RawCorrectedPlatformEvent de MSMCAInfo** contiene un evento de plataforma corregido (CPE). Esta clase solo está disponible en sistemas de 64 Windows bits.

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

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

La **clase \_ RawCorrectedPlatformEvent de MSMCAInfo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ RawCorrectedPlatformEvent de MSMCAInfo** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

TRUE, si esta instancia de la clase está activa; de lo contrario, **FALSE**.

</dd> <dt>

**Recuento**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de registros de error.

</dd> <dt>

**Registros**
</dt> <dd> <dl> <dt>

Tipo de datos: **Matriz de entrada MSMCAInfo \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de registros de errores de MCA. La propiedad Count especifica el número de registros de error de MCA en la **matriz.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase MSMCAInfo \_ RawCorrectedPlatformEvent** se deriva de [**WMIEvent**](wmievent.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

 




