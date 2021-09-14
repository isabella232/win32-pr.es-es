---
description: Especifica los registros de arquitectura de comprobación de máquina (MCA) sin procesar. Esta clase solo está disponible en sistemas de 64 Windows bits.
ms.assetid: d465ba8d-14b2-4911-ae19-19ebeb32126e
title: MSMCAInfo_RawMCAData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAData
- MSMCAInfo_RawMCAData.Active
- MSMCAInfo_RawMCAData.Count
- MSMCAInfo_RawMCAData.InstanceName
- MSMCAInfo_RawMCAData.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 6cafc16ddbc91181cc2114def07a193941988228
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073107"
---
# <a name="msmcainfo_rawmcadata-class"></a>Clase RawMCAData de MSMCAInfo \_

**MSMCAInfo \_ RawMCAData especifica** los registros de arquitectura de comprobación de máquina (MCA) sin procesar. Esta clase solo está disponible en sistemas de 64 Windows bits.

La sintaxis siguiente se simplifica a Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAInfo_RawMCAData : MSMCAInfo
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Members

La **clase \_ RawMCAData MSMCAInfo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ RawMCAData MSMCAInfo** tiene estas propiedades.

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

Tipo de datos: **matriz de entrada MSMCAInfo \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de registros de errores de MCA. La propiedad Count especifica el número de registros de error de MCA en **la matriz.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ RawMCAData de MSMCAInfo** se deriva de [**MSMCAInfo**](msmcainfo.md).

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

[**MSMCAInfo**](msmcainfo.md)
</dt> </dl>

 

