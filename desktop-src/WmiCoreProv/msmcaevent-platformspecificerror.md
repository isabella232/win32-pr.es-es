---
description: Indica un error específico de la plataforma de la arquitectura de comprobación de la máquina (MCA). Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: 409641d5-3451-4d26-88d1-bfd0e55db257
title: MSMCAEvent_PlatformSpecificError (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PlatformSpecificError
- MSMCAEvent_PlatformSpecificError.Active
- MSMCAEvent_PlatformSpecificError.AdditionalErrors
- MSMCAEvent_PlatformSpecificError.Cpu
- MSMCAEvent_PlatformSpecificError.ErrorSeverity
- MSMCAEvent_PlatformSpecificError.InstanceName
- MSMCAEvent_PlatformSpecificError.OEM_COMPONENT_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_BUS_SPECIFIC_DATA
- MSMCAEvent_PlatformSpecificError.PLATFORM_ERROR_STATUS
- MSMCAEvent_PlatformSpecificError.PLATFORM_REQUESTOR_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_RESPONDER_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_TARGET_ID
- MSMCAEvent_PlatformSpecificError.RawRecord
- MSMCAEvent_PlatformSpecificError.RecordId
- MSMCAEvent_PlatformSpecificError.Size
- MSMCAEvent_PlatformSpecificError.Type
- MSMCAEvent_PlatformSpecificError.VALIDATION_BITS
- MSMCAEvent_PlatformSpecificError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 51993c8c41206dac8f4c944d24fa59ae7b689f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497435"
---
# <a name="msmcaevent_platformspecificerror-class"></a>MSMCAEvent \_ PlatformSpecificError (clase)

La clase **MSMCAEvent \_ PlatformSpecificError** indica un error específico de la plataforma de la arquitectura de comprobación de equipo (MCA). Esta clase solo está disponible en sistemas Windows de 64 bits.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAEvent_PlatformSpecificError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   OEM_COMPONENT_ID;
  uint64  PLATFORM_BUS_SPECIFIC_DATA;
  uint64  PLATFORM_ERROR_STATUS;
  uint64  PLATFORM_REQUESTOR_ID;
  uint64  PLATFORM_RESPONDER_ID;
  uint64  PLATFORM_TARGET_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Miembros

La clase **MSMCAEvent \_ PlatformSpecificError** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSMCAEvent \_ PlatformSpecificError** tiene estas propiedades.

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

Número de errores adicionales en el registro.

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

**\_identificador del componente OEM \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador único del componente que informa del error.

</dd> <dt>

**\_ \_ datos específicos de Platform bus \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Datos específicos del bus de OEM.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_Estado de error de plataforma \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado de error de plataforma genérica.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**identificador del solicitante de plataforma \_ \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador del solicitante en el momento del evento.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_identificador del respondedor de plataforma \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador del respondedor en el momento del evento.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_identificador de destino de la plataforma \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de destino en el momento del evento.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

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

</dd> <dt>

**BITS de validación \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Bits de validación que se usan para indicar la validez de los campos siguientes.



| Value                                                                                                                                         | Significado                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <dt>**1 0x1**</dt> </dl>          | **Plataforma \_ de El \_ Estado de error** es válido.<br/>            |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <dt>**2 0X2**</dt> </dl>          | **Plataforma \_ de El \_ \_ identificador del solicitante de errores** es válido.<br/>     |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <dt>**4 0x4**</dt> </dl>          | **Plataforma \_ de El \_ \_ identificador del respondedor de errores** es válido.<br/>     |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <dt>**8 0x8**</dt> </dl>          | **Plataforma \_ de El \_ \_ ID** . de destino del error es válido.<br/>        |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <dt>**16 0x10**</dt> </dl>    | **Plataforma \_ de Los \_ \_ datos específicos del error** son válidos.<br/>    |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <dt>**32 0x20**</dt> </dl>    | **Plataforma \_ de El \_ \_ ID** . de OEM del error es válido.<br/>           |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <dt>**64 0x40**</dt> </dl>    | **Plataforma \_ de ERROR \_ el \_ \_ struct de datos OEM** es válido.<br/> |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <dt>**128 0x80**</dt> </dl> | **Plataforma \_ de ERROR: la \_ \_ ruta de \_ acceso del dispositivo OEM** es válida.<br/> |



 

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **MSMCAEvent \_ PlatformSpecificError** se deriva de [**WMIEvent**](wmievent.md).

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

 

