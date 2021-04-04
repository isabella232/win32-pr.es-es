---
description: La estructura NMEVENTDATA contiene información sobre una condición de evento que se pasa a Monitor de red para insertar una línea en el visor de expertos.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: Estructura NMEVENTDATA (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMEVENTDATA
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6258b1b1bfde5b159165de2efb9a010053c0421a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908181"
---
# <a name="nmeventdata-structure"></a>Estructura NMEVENTDATA

La estructura **NMEVENTDATA** contiene información sobre una condición de evento que se pasa a monitor de red para insertar una línea en el visor de expertos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  BYTE         Version;
  DWORD        EventIdent;
  DWORD        Flags;
  DWORD        Severity;
  BYTE         NumColumns;
  LPSTR        szSourceName;
  LPSTR        szEventName;
  LPSTR        szDescription;
  LPSTR        szMachine;
  JTYPE        Justification;
  LPSTR        szUrl;
  SYSTEMTIME   SysTime;
  NMCOLUMNINFO Column[];
} NMEVENTDATA, *PNMEVENTDATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Versión**
</dt> <dd>

Número de versión de la estructura **NMEVENTDATA** . El número de versión debe ser cero. Las versiones futuras de Monitor de red pueden admitir un número de versión superior.

</dd> <dt>

**EventIdent**
</dt> <dd>

Identificador del evento. **EventIdent** es único para cada experto y hace referencia a una [Página de referencia de evento](event-reference-page.md).

</dd> <dt>

**Marcas**
</dt> <dd>

Un conjunto de marcas que describe quién envía los datos de evento y cómo se muestra el evento.



| Value                                                                                                                                                                                                                                              | Significado                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <dt>**\_experto en marcas de evento \_**</dt> </dl>                                                                         | El evento procede de un experto. <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <dt>**NMEVENTFLAG \_ \_ no \_ Mostrar \_ gravedad**</dt> </dl>                 | No mostrar el nivel de gravedad para el evento. <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <dt>**NMEVENTFLAG \_ \_ no \_ Mostrar el \_ origen**</dt> </dl>                       | No se muestra el nombre del origen del evento. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <dt>**NMEVENTFLAG \_ \_ no \_ Mostrar \_ nombre de evento \_**</dt> </dl>          | No muestre el nombre del evento. <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <dt>**NMEVENTFLAG \_ \_ no \_ Mostrar \_ Descripción**</dt> </dl>        | No se muestra la descripción del evento. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <dt>**NMEVENTFLAG \_ \_ no \_ Mostrar \_ equipo**</dt> </dl>                    | No muestre el nombre del equipo para el evento. <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <dt>**NMEVENTFLAG \_ \_ no \_ Mostrar \_ hora**</dt> </dl>                             | No mostrar la hora del evento <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <dt>**NMEVENTFLAG \_ \_ no \_ Mostrar \_ columnas fijas \_**</dt> </dl> | No muestre la gravedad, el origen, el nombre del evento, la descripción, la máquina o las columnas de tiempo. No se trata de una marca única, pero es una Unión de las seis marcas anteriores. <br/> |



 

</dd> <dt>

**Gravedad**
</dt> <dd>

Nivel de gravedad del evento. El nivel de gravedad puede tener uno de los siguientes valores:

NMEVENT \_ gravedad \_ informativa NMEVENT \_ gravedad \_ ADVERTENCIA NMEVENT gravedad \_ \_ severa \_ ADVERTENCIA NMEVENT \_ gravedad NMEVENT gravedad grave error \_ \_ \_ \_ NMEVENT \_ gravedad \_ crítico \_ error

</dd> <dt>

**NumColumns**
</dt> <dd>

Número de columnas designadas en la estructura actual.

</dd> <dt>

**szSourceName**
</dt> <dd>

Nombre del experto que se muestra.

</dd> <dt>

**szEventName**
</dt> <dd>

Nombre del evento que se muestra.

</dd> <dt>

**szDescription**
</dt> <dd>

Descripción del evento que se muestra.

</dd> <dt>

**szMachine**
</dt> <dd>

Obsoleto, debe ser **null**.

</dd> <dt>

**Justificación**
</dt> <dd>

Información que se muestra en la segunda ventana del Visor de eventos. El miembro de **justificación** puede ser **null**. Si es **null**, la segunda ventana no es visible.

</dd> <dt>

**szUrl**
</dt> <dd>

Sector Este miembro debe ser **null**.

</dd> <dt>

**SysTime**
</dt> <dd>

Hora a la que se produce la condición de evento. La hora se mide en relación con el principio de la captura.

</dd> <dt>

**Columna**
</dt> <dd>

Tabla de estructuras de columna que aparece en el panel superior del Visor de eventos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




