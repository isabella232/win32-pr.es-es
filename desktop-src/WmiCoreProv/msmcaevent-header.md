---
description: Representa el encabezado común que usan todas las clases MSMCAEvent. Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: ff20522c-f805-47dc-bef2-4176211de698
title: MSMCAEvent_Header (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_Header
- MSMCAEvent_Header.AdditionalErrors
- MSMCAEvent_Header.Cpu
- MSMCAEvent_Header.ErrorSeverity
- MSMCAEvent_Header.RecordId
- MSMCAEvent_Header.Type
- MSMCAEvent_Header.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 426f943014f3b6cfbdba5a25d331c0ea621048cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697474"
---
# <a name="msmcaevent_header-class"></a>\_Clase de encabezado MSMCAEvent

La clase de **\_ encabezado MSMCAEvent** representa el encabezado común que usan todas [las clases MSMCA](msmca-classes.md) . Los archivos de encabezado se usan para que el código de C y C++ pueda tener una estructura de datos que describa el encabezado común para todos los eventos. Esta clase está reservada para uso interno. Esta clase solo está disponible en sistemas Windows de 64 bits.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAEvent_Header
{
  uint32 AdditionalErrors;
  uint32 Cpu;
  uint8  ErrorSeverity;
  uint64 RecordId;
  uint32 Type;
  uint32 LogToEventlog;
};
```

## <a name="members"></a>Miembros

La clase de **\_ encabezado MSMCAEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ encabezado MSMCAEvent** tiene estas propiedades.

<dl> <dt>

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

CPU que informa del error. Esta propiedad solo se aplica a un sistema de varios procesadores en el que el primer procesador tiene asignado el número 0, el segundo procesador tiene asignado el número 1 y así sucesivamente.

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

**LogToEventlog**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es 0 (cero), este evento no se registra en el registro de eventos del sistema.

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

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de mensaje de registro de eventos. Estos mensajes se corresponden con los códigos de mensaje de registro de eventos utilizados para insertar mensajes de registro de eventos del proveedor de consumidores del registro de eventos de Windows cuando recibe uno de los eventos.

</dd> </dl>

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

[Clases de C++ de WMI](/windows/desktop/WmiSdk/wmi-c-classes)
</dt> </dl>

 

