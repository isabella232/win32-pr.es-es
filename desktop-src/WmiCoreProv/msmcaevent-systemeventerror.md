---
description: Indica que se ha producido un evento del sistema De interfaz de administración de plataforma inteligente (IPMI). El error se escribe en el registro de eventos del sistema SMBIOS (SEL). Esta clase solo está disponible en sistemas de 64 Windows bits.
ms.assetid: 1964f850-ac55-4639-9205-2eb0996dbaae
title: MSMCAEvent_SystemEventError clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SystemEventError
- MSMCAEvent_SystemEventError.Active
- MSMCAEvent_SystemEventError.AdditionalErrors
- MSMCAEvent_SystemEventError.Cpu
- MSMCAEvent_SystemEventError.ErrorSeverity
- MSMCAEvent_SystemEventError.InstanceName
- MSMCAEvent_SystemEventError.RawRecord
- MSMCAEvent_SystemEventError.RecordId
- MSMCAEvent_SystemEventError.SEL_DATA1
- MSMCAEvent_SystemEventError.SEL_DATA2
- MSMCAEvent_SystemEventError.SEL_DATA3
- MSMCAEvent_SystemEventError.SEL_EVENT_DIR_TYPE
- MSMCAEvent_SystemEventError.SEL_EVM_REV
- MSMCAEvent_SystemEventError.SEL_GENERATOR_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_TYPE
- MSMCAEvent_SystemEventError.SEL_SENSOR_NUM
- MSMCAEvent_SystemEventError.SEL_SENSOR_TYPE
- MSMCAEvent_SystemEventError.SEL_TIME_STAMP
- MSMCAEvent_SystemEventError.Size
- MSMCAEvent_SystemEventError.Type
- MSMCAEvent_SystemEventError.VALIDATION_BITS
- MSMCAEvent_SystemEventError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f20f95fb5e1b1bf07b0f70c25d54122642b13569
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170530"
---
# <a name="msmcaevent_systemeventerror-class"></a>Clase SystemEventError de MSMCAEvent \_

La **clase \_ SystemEventError de MSMCAEvent** indica que se ha producido un evento del sistema Intelligent Platform Management Interface (IPMI). El error se escribe en el registro de eventos del sistema SMBIOS (SEL). Esta clase solo está disponible en sistemas de 64 Windows bits.

La sintaxis siguiente se simplifica a Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAEvent_SystemEventError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint8   SEL_DATA1;
  uint8   SEL_DATA2;
  uint8   SEL_DATA3;
  uint8   SEL_EVENT_DIR_TYPE;
  uint8   SEL_EVM_REV;
  uint16  SEL_GENERATOR_ID;
  uint16  SEL_RECORD_ID;
  uint8   SEL_RECORD_TYPE;
  uint8   SEL_SENSOR_NUM;
  uint8   SEL_SENSOR_TYPE;
  uint64  SEL_TIME_STAMP;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Members

La **clase \_ SystemEventError de MSMCAEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemEventError de MSMCAEvent** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**TRUE**, si esta instancia de la clase está activa; de lo contrario, **FALSE**.

</dd> <dt>

**AdditionalErrors**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de errores adicionales en el registro.

</dd> <dt>

**Cpu**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

CPU que informó del error. Esta propiedad solo se aplica a un sistema de varios procesadores en el que al primer procesador se le asigna el número 0, al segundo procesador se le asigna el número 1, y así sucesivamente.

</dd> <dt>

**ErrorSeverity**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nivel de gravedad del error notificado.



| Value                                                                                                | Significado                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Recuperable<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Grave<br/>       |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Corregible<br/> |



 

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

**LogToEventlog**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es 0 (cero), este evento no se registra en el registro de eventos del sistema.

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de bytes que contiene el registro de error sin formato. Número de elementos de la matriz que especifica **la** propiedad Size.

</dd> <dt>

**RecordId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de registro del registro de errores para este error.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**SEL \_ DATA1**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Campo de datos de evento 1.

</dd> <dt>

**SEL \_ DATA2**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Campo de datos de evento 2.

</dd> <dt>

**SEL \_ DATA3**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Campo de datos de evento 3.

</dd> <dt>

**TIPO DE \_ DIRECTORIO DE \_ EVENTOS \_ SEL**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de directorio de eventos.

</dd> <dt>

**SEL \_ EVM \_ REV**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dar formato a la versión del mensaje de error.

</dd> <dt>

**IDENTIFICADOR DEL GENERADOR DE SEL \_ \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de software, si el evento se generó por software.

</dd> <dt>

**IDENTIFICADOR DE REGISTRO DE SEL \_ \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de registro usado para el acceso al registro de eventos del sistema SMBIOS (SEL).

</dd> <dt>

**TIPO DE REGISTRO SEL \_ \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de registro.

</dd> <dt>

**SEL \_ SENSOR \_ NUM**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de sensor que generó el evento.

</dd> <dt>

**TIPO DE SENSOR SEL \_ \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Código de tipo de sensor del sensor que generó el evento.

</dd> <dt>

**MARCA DE TIEMPO DE SEL \_ \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marca de tiempo del registro de eventos.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Tamaño**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño del registro de errores sin procesar.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de mensaje del registro de eventos. Estos mensajes corresponden a los códigos de mensaje del registro de eventos usados para insertar mensajes del registro de eventos por parte del proveedor de consumidor del registro de eventos Windows cuando recibe uno de los eventos.

</dd> <dt>

**BITS DE \_ VALIDACIÓN**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Bits de validación usados para indicar la validez de los campos posteriores.



| Value                                                                                                                                            | Significado                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <dt>**1 0x1**</dt> </dl>             | **SEL \_ El \_ id. de REGISTRO** es válido.<br/>    |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <dt>**2 0x2**</dt> </dl>             | **SEL \_ RECORD \_ TYPE** es válido.<br/>  |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <dt>**4 0x4**</dt> </dl>             | **SEL \_ El \_ identificador del GENERADOR** es válido.<br/> |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <dt>**8 0x8**</dt> </dl>             | **SEL \_ EVM \_ REV** es válido.<br/>      |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <dt>**16 0x10**</dt> </dl>       | **SEL \_ EL \_ TIPO DE SENSOR** es válido.<br/>  |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <dt>**32 0x20**</dt> </dl>       | **SEL \_ SENSOR \_ NUM** es válido.<br/>   |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <dt>**64 0x40**</dt> </dl>       | **SEL \_ EVENT \_ DIR** es válido.<br/>    |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <dt>**128 0x80**</dt> </dl>    | **SEL \_ EVENT \_ DATA1** es válido.<br/>  |
| <span id="256_0x100"></span><span id="256_0X100"></span><dl> <dt>**256 0x100**</dt> </dl> | **SEL \_ EVENT \_ DATA2** es válido.<br/>  |
| <span id="512_0x200"></span><span id="512_0X200"></span><dl> <dt>**512 0x200**</dt> </dl> | **SEL \_ EVENT \_ DATA3** es válido.<br/>  |



 

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ SystemEventError de MSMCAEvent** se deriva de [**WMIEvent**](wmievent.md).

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

 

