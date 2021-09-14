---
description: Indica un error de BIOS del sistema de machine check architecture (MCA). Esta clase solo está disponible en sistemas de 64 Windows bits.
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: MSMCAEvent_SMBIOSError clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SMBIOSError
- MSMCAEvent_SMBIOSError.Active
- MSMCAEvent_SMBIOSError.AdditionalErrors
- MSMCAEvent_SMBIOSError.Cpu
- MSMCAEvent_SMBIOSError.ErrorSeverity
- MSMCAEvent_SMBIOSError.InstanceName
- MSMCAEvent_SMBIOSError.RawRecord
- MSMCAEvent_SMBIOSError.RecordId
- MSMCAEvent_SMBIOSError.Size
- MSMCAEvent_SMBIOSError.SMBIOS_EVENT_TYPE
- MSMCAEvent_SMBIOSError.Type
- MSMCAEvent_SMBIOSError.VALIDATION_BITS
- MSMCAEvent_SMBIOSError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 709d480e8865c5d5bde2a9f5e8de45f138e66548
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889228"
---
# <a name="msmcaevent_smbioserror-class"></a>Clase MSMCAEvent \_ SMBIOSError

La **clase \_ SMBIOSError de MSMCAEvent** indica un error de BIOS del sistema machine check architecture (MCA). Esta clase solo está disponible en sistemas de 64 Windows bits.

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAEvent_SMBIOSError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint8   SMBIOS_EVENT_TYPE;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Members

La **clase MSMCAEvent \_ SMBIOSError** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase MSMCAEvent \_ SMBIOSError** tiene estas propiedades.

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

**Tamaño**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño del registro de errores sin procesar.

</dd> <dt>

**TIPO DE \_ EVENTO \_ SMBIOS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de evento.



| Value                                                                                                  | Significado                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl>   | Reservado.<br/>                                                                                                        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl>   | Error de memoria ECC de un solo bit.<br/>                                                                                     |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>   | Error de memoria ECC de varios bits.<br/>                                                                                   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>   | Error de memoria de paridad.<br/>                                                                                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>   | Tiempo de espera del bus.<br/>                                                                                                    |
| <span id="5"></span><dl> <dt>**5**</dt> </dl>   | Comprobación del canal de E/S.<br/>                                                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl>   | Software NMI.<br/>                                                                                                    |
| <span id="7"></span><dl> <dt>**7**</dt> </dl>   | Cambiar el tamaño de la memoria posterior.<br/>                                                                                              |
| <span id="8"></span><dl> <dt>**8**</dt> </dl>   | Error POST.<br/>                                                                                                      |
| <span id="9"></span><dl> <dt>**9**</dt> </dl>   | Error de paridad de PCI.<br/>                                                                                                |
| <span id="10"></span><dl> <dt>**10**</dt> </dl> | Error del sistema PCI.<br/>                                                                                                |
| <span id="11"></span><dl> <dt>**11**</dt> </dl> | Error de CPU.<br/>                                                                                                     |
| <span id="12"></span><dl> <dt>**12**</dt> </dl> | Tiempo de espera del temporizador a prueba de errores de EISA.<br/>                                                                                    |
| <span id="13"></span><dl> <dt>**13**</dt> </dl> | Registro de memoria corregida deshabilitada.<br/>                                                                                 |
| <span id="14"></span><dl> <dt>**14**</dt> </dl> | Registro deshabilitado para un tipo de evento específico. Demasiados errores del mismo tipo recibidos en un breve período de tiempo.<br/> |
| <span id="15"></span><dl> <dt>**15**</dt> </dl> | Reservado.<br/>                                                                                                        |
| <span id="16"></span><dl> <dt>**16**</dt> </dl> | Se superó el límite del sistema (por ejemplo, se superó el umbral de voltaje o temperatura).<br/>                                  |
| <span id="17"></span><dl> <dt>**17**</dt> </dl> | El temporizador de hardware asincrónico expiró y emitió un restablecimiento del sistema.<br/>                                                   |
| <span id="18"></span><dl> <dt>**18**</dt> </dl> | Información de configuración del sistema.<br/>                                                                                |
| <span id="19"></span><dl> <dt>**19**</dt> </dl> | Información de disco duro.<br/>                                                                                           |
| <span id="20"></span><dl> <dt>**20**</dt> </dl> | Sistema reconfigurado.<br/>                                                                                             |
| <span id="21"></span><dl> <dt>**21**</dt> </dl> | Error complejo de CPU no correcible.<br/>                                                                                 |
| <span id="22"></span><dl> <dt>**22**</dt> </dl> | Restablecimiento o borrado del área de registro.<br/>                                                                                       |
| <span id="23"></span><dl> <dt>**23**</dt> </dl> | Arranque del sistema. Si se implementa, se garantiza que esta entrada de registro es la primera escrita en cualquier arranque del sistema.<br/>        |



 

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

Bits de validación usados para indicar la validez de los campos subsiguientes. Un valor de 1 (0x1) significa que **el evento SMBIOS \_** es válido.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase MSMCAEvent \_ SMBIOSError** se deriva de [**WMIEvent**](wmievent.md).

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

 

