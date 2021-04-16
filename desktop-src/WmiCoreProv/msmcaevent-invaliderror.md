---
description: Indica un error no válido de arquitectura de comprobación de equipo (MCA). Un error de MCA no válido identifica un formato de error que no se ajusta a las especificaciones de Windows. Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: 476ea558-2e0e-480f-b4ba-8d73fdef3308
title: MSMCAEvent_InvalidError (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_InvalidError
- MSMCAEvent_InvalidError.Active
- MSMCAEvent_InvalidError.AdditionalErrors
- MSMCAEvent_InvalidError.Cpu
- MSMCAEvent_InvalidError.ErrorSeverity
- MSMCAEvent_InvalidError.InstanceName
- MSMCAEvent_InvalidError.RawRecord
- MSMCAEvent_InvalidError.RecordId
- MSMCAEvent_InvalidError.Size
- MSMCAEvent_InvalidError.Type
- MSMCAEvent_InvalidError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: abd12cfa7280a1b2f6a718b47b17d4ddf121cc25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696366"
---
# <a name="msmcaevent_invaliderror-class"></a>MSMCAEvent \_ InvalidError (clase)

La clase **MSMCAEvent \_ InvalidError** indica un error no válido de arquitectura de comprobación de equipo (MCA). Un error de MCA no válido identifica un formato de error que no se ajusta a las especificaciones de Windows. Esta clase solo está disponible en sistemas Windows de 64 bits.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAEvent_InvalidError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Miembros

La clase **MSMCAEvent \_ InvalidError** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSMCAEvent \_ InvalidError** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si esta instancia de la clase está activa; en caso contrario, **false**.

</dd> <dt>

**AdditionalErrors**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de errores adicionales en el registro de MCA.

</dd> <dt>

**CPU**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

CPU que ha detectado el error. Esta propiedad solo se aplica a un sistema de varios procesadores en el que el primer procesador tiene asignado el número 0, el segundo procesador tiene asignado el número 1 y así sucesivamente.

</dd> <dt>

**ErrorSeverity**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nivel de gravedad del error comunicado.



| Value                                                                                                | Significado                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0,1**</dt> </dl> | Recuperable<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Crítico<br/>       |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Corregible<br/> |



 

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificador único de esta instancia de la clase.

</dd> <dt>

**LogToEventlog**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es 0 (cero), este evento no se registra en el registro de eventos del sistema.

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de bytes que contiene el registro de errores sin procesar tal y como se presenta en Windows por la capa de abstracción del sistema (SAL). La propiedad **size** especifica el número de elementos de la matriz.

</dd> <dt>

**RecordId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de registro del registro de errores para este error.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Tamaño**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño del registro de errores sin procesar.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de mensaje de registro de eventos. Estos mensajes se corresponden con los códigos de mensaje de registro de eventos utilizados para insertar mensajes de registro de eventos del proveedor de consumidores del registro de eventos de Windows cuando recibe uno de los eventos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **MSMCAEvent \_ InvalidError** se deriva de [**WMIEvent**](wmievent.md).

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

 

