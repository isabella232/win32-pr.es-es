---
description: La estructura NMEVENTDATA contiene información sobre una condición de evento que se pasa a Monitor de red para insertar una línea en el visor experto.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: Estructura NMEVENTDATA (Netmon.h)
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
ms.openlocfilehash: af2a4775be7d9e123974fbab865a8171d9bc9dec7dacae7692054bc6db0d3085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037045"
---
# <a name="nmeventdata-structure"></a>NMEVENTDATA (estructura)

La **estructura NMEVENTDATA** contiene información sobre una condición de evento que se pasa a Monitor de red para insertar una línea en el visor experto.

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

Número de versión de la **estructura NMEVENTDATA.** El número de versión debe ser cero. Las versiones futuras Monitor de red pueden admitir un número de versión mayor.

</dd> <dt>

**EventIdent**
</dt> <dd>

Identificador del evento. **EventIdent** es único para cada experto y hace referencia a una página [de referencia de eventos](event-reference-page.md).

</dd> <dt>

**Marcas**
</dt> <dd>

Conjunto de marcas que describe quién envía los datos del evento y cómo se muestra el evento.



| Value                                                                                                                                                                                                                                              | Significado                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <dt>**EXPERTO \_ EN MARCAS DE \_ EVENTOS**</dt> </dl>                                                                         | El evento provenía de un experto. <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <dt>**NMEVENTFLAG \_ NO \_ MUESTRA \_ \_ GRAVEDAD**</dt> </dl>                 | No muestre el nivel de gravedad del evento. <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <dt>**NMEVENTFLAG \_ NO MUESTRA EL \_ \_ \_ ORIGEN**</dt> </dl>                       | No muestre el nombre de origen del evento. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <dt>**NMEVENTFLAG \_ NO MUESTRA EL NOMBRE DEL \_ \_ \_ \_ EVENTO**</dt> </dl>          | No muestre el nombre del evento. <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <dt>**NMEVENTFLAG \_ NO MUESTRA LA \_ \_ \_ DESCRIPCIÓN**</dt> </dl>        | No muestre la descripción del evento. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <dt>**NMEVENTFLAG \_ NO MUESTRA LA \_ \_ \_ MÁQUINA**</dt> </dl>                    | No muestre el nombre de la máquina para el evento. <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <dt>**NMEVENTFLAG \_ NO MUESTRA LA \_ \_ \_ HORA**</dt> </dl>                             | No mostrar la hora del evento <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <dt>**NMEVENTFLAG \_ NO MUESTRA COLUMNAS \_ \_ \_ \_ FIJAS**</dt> </dl> | No muestre las columnas Gravedad, Origen, Nombre del evento, Descripción, Máquina o Hora. No se trata de una sola marca, pero es una unión de las seis marcas anteriores. <br/> |



 

</dd> <dt>

**Gravedad**
</dt> <dd>

Nivel de gravedad del evento. El nivel de gravedad puede tener uno de los siguientes valores:

INFORMACIÓN DE GRAVEDAD DE NMEVENT ADVERTENCIA DE GRAVEDAD NMEVENT ADVERTENCIA DE GRAVEDAD NMEVENT ADVERTENCIA FUERTE ADVERTENCIA NMEVENT ERROR DE GRAVEDAD \_ \_ \_ \_ \_ \_ \_ NMEVENT \_ GRAVEDAD \_ NMEVENT ERROR GRAVE ERROR \_ \_ \_ CRÍTICO \_ \_ \_ DE GRAVEDAD NMEVENT

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

Obsoleto, debe ser **NULL.**

</dd> <dt>

**Justificación**
</dt> <dd>

Información que se muestra en la segunda ventana de la Visor de eventos. El **miembro Justification** puede ser **NULL.** Si es **NULL,** la segunda ventana no estará visible.

</dd> <dt>

**szUrl**
</dt> <dd>

Reservado; este miembro debe ser **NULL.**

</dd> <dt>

**SysTime**
</dt> <dd>

Hora a la que se produce la condición de evento. El tiempo se mide con respecto al principio de la captura.

</dd> <dt>

**Columna**
</dt> <dd>

Tabla de estructuras de columna que aparece en el panel superior de la Visor de eventos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




