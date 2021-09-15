---
description: Contiene un evento Corrected Machine Check (CMC). Esta clase solo está disponible en sistemas de 64 Windows bits.
ms.assetid: e12efbf7-7d53-415a-bc48-90d33e4ce16d
title: MSMCAInfo_RawCMCEvent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCMCEvent
- MSMCAInfo_RawCMCEvent.Active
- MSMCAInfo_RawCMCEvent.Count
- MSMCAInfo_RawCMCEvent.InstanceName
- MSMCAInfo_RawCMCEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 1bb60d5fbcf004b924a91e640d8cd8a8c5ad3c25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568112"
---
# <a name="msmcainfo_rawcmcevent-class"></a>Clase RawCMCEvent de MSMCAInfo \_

La **clase \_ RawCMCEvent de MSMCAInfo** contiene un evento Corrected Machine Check (CMC). Esta clase solo está disponible en sistemas de 64 Windows bits.

La sintaxis siguiente se simplifica a Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAInfo_RawCMCEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Members

La **clase \_ RawCMCEvent de MSMCAInfo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ RawCMCEvent MSMCAInfo** tiene estas propiedades.

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

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificador único de esta instancia de la clase .

</dd> <dt>

**Registros**
</dt> <dd> <dl> <dt>

Tipo de datos: **Matriz de entrada MSMCAInfo \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de registros de errores de arquitectura de comprobación de máquinas (MCA). La propiedad Count especifica el número de registros de error de MCA en la **matriz.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ RawCMCEvent de MSMCAInfo** se deriva de [**WMIEvent**](wmievent.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases MSMCA](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

