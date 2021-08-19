---
description: Representa un error de bus PCI de arquitectura de comprobación de máquina (MCA). Esta clase solo está disponible para equipos que se ejecutan en un sistema operativo de 64 Windows bits.
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: MSMCAEvent_PCIBusError clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIBusError
- MSMCAEvent_PCIBusError.Active
- MSMCAEvent_PCIBusError.AdditionalErrors
- MSMCAEvent_PCIBusError.Cpu
- MSMCAEvent_PCIBusError.ErrorSeverity
- MSMCAEvent_PCIBusError.InstanceName
- MSMCAEvent_PCIBusError.PCI_BUS_ADDRESS
- MSMCAEvent_PCIBusError.PCI_BUS_CMD
- MSMCAEvent_PCIBusError.PCI_BUS_DATA
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_STATUS
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_TYPE
- MSMCAEvent_PCIBusError.PCI_BUS_ID_BusNumber
- MSMCAEvent_PCIBusError.PCI_BUS_ID_SegmentNumber
- MSMCAEvent_PCIBusError.PCI_BUS_REQUESTOR_ID
- MSMCAEvent_PCIBusError.PCI_BUS_RESPONDER_ID
- MSMCAEvent_PCIBusError.RawRecord
- MSMCAEvent_PCIBusError.RecordId
- MSMCAEvent_PCIBusError.Size
- MSMCAEvent_PCIBusError.Type
- MSMCAEvent_PCIBusError.VALIDATION_BITS
- MSMCAEvent_PCIBusError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 4b3ae66c684ab6a0e2573e2c82d6087a3405ce3d8bef5704bb392337699daaea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051283"
---
# <a name="msmcaevent_pcibuserror-class"></a>Clase PCIBusError de MSMCAEvent \_

La **clase \_ PCIBusError de MSMCAEvent representa** un error de bus PCI de machine check architecture (MCA). Esta clase solo está disponible para equipos que se ejecutan en un sistema operativo de 64 Windows bits.

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAEvent_PCIBusError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_BUS_ADDRESS;
  uint64  PCI_BUS_CMD;
  uint64  PCI_BUS_DATA;
  uint64  PCI_BUS_ERROR_STATUS;
  uint16  PCI_BUS_ERROR_TYPE;
  uint8   PCI_BUS_ID_BusNumber;
  uint8   PCI_BUS_ID_SegmentNumber;
  uint64  PCI_BUS_REQUESTOR_ID;
  uint64  PCI_BUS_RESPONDER_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Miembros

La **clase MSMCAEvent \_ PCIBusError** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase MSMCAEvent \_ PCIBusError** tiene estas propiedades.

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



| Valor                                                                                                | Significado                |
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

**DIRECCIÓN DE PCI \_ \_ BUS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Memoria o dirección de E/S en el bus PCI en el momento del evento.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**PCI \_ BUS \_ CMD**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Comando u operación de bus en el momento del evento.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**DATOS DE PCI \_ \_ BUS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Datos en el bus PCI en el momento del evento.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**ESTADO DE ERROR DE PCI \_ BUS \_ \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado del bus en el momento del error.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**TIPO DE ERROR DE PCI \_ \_ \_ BUS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de error de bus PCI.



| Valor                                                                                                | Significado                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Error desconocido o específico del sistema oem.<br/>            |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Error de paridad de datos.<br/>                               |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Error del sistema.<br/>                                    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Anulación maestra.<br/>                                    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Tiempo de espera de bus o ningún dispositivo presente (NO DEVSEL \# ).<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Error de paridad de datos maestros.<br/>                        |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Error de paridad de direcciones.<br/>                            |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Error de paridad de comandos.<br/>                            |



 

</dd> <dt>

**PCI \_ BUS \_ ID \_ BusNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador designado para el bus PCI que encontró el error.

</dd> <dt>

**Id. de PCI \_ BUS \_ \_ SegmentNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de segmento designado para el bus PCI que encontró el error.

</dd> <dt>

**IDENTIFICADOR DEL SOLICITANTE DE PCI \_ \_ \_ BUS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador del solicitante de PCI Bus en el momento del evento.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**ID. \_ DE RESPONDEDOR DE PCI \_ \_ BUS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador del respondedor de BUS PCI en el momento del evento.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de bytes que contiene el registro de errores sin procesar presentado a Windows por la capa de abstracción del sistema (SAL). La propiedad Size especifica el número de elementos de la **matriz.**

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



| Valores                                                                                  | Significado                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>      | EL ESTADO DE ERROR DE PCI \_ BUS \_ es \_ válido.<br/>     |
| <dl> <dt>2 (0x2)</dt> </dl>      | EL TIPO DE ERROR DE PCI \_ BUS \_ es \_ válido.<br/>       |
| <dl> <dt>4 (0x4)</dt> </dl>      | El identificador de PCI \_ BUS \_ es válido.<br/>                |
| <dl> <dt>8 (0x8)</dt> </dl>      | PCI \_ BUS ADDRESS es \_ válido.<br/>           |
| <dl> <dt>16 (0x10)</dt> </dl>    | PCI \_ BUS DATA es \_ válido.<br/>              |
| <dl> <dt>32 (0x20)</dt> </dl>    | CMD de PCI \_ BUS \_ es válido.<br/>               |
| <dl> <dt>64 (0x40)</dt> </dl>    | El identificador del SOLICITANTE de PCI \_ BUS \_ es \_ válido.<br/>     |
| <dl> <dt>128 (0x80)</dt> </dl>   | El identificador del RESPONDEDOR de PCI \_ BUS es \_ \_ válido.<br/>     |
| <dl> <dt>256 (0x100)</dt> </dl>  | El identificador de DESTINO de PCI \_ BUS \_ es \_ válido.<br/>        |
| <dl> <dt>512 (0x200)</dt> </dl>  | El \_ identificador de OEM de PCI BUS es \_ \_ válido.<br/>           |
| <dl> <dt>1024 (0x400)</dt> </dl> | La estructura DATA STRUCT de OEM de PCI \_ BUS es \_ \_ \_ válida.<br/> |



 

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase MSMCAEvent \_ PCIBusError** se deriva de [**WMIEvent**](wmievent.md).

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

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

