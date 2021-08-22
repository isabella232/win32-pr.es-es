---
description: La estructura PRINTER NOTIFY INFO DATA identifica un campo de información de trabajo o impresora y proporciona \_ \_ los datos \_ actuales para ese campo.
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: PRINTER_NOTIFY_INFO_DATA estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO_DATA,
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e26f7ed7f002801d3bbdf60708d83234231fe3333675a1c211488431868a4236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731199"
---
# <a name="printer_notify_info_data-structure"></a>ESTRUCTURA DE \_ DATOS DE INFORMACIÓN DE NOTIFICACIÓN DE \_ \_ IMPRESORA

La **estructura PRINTER NOTIFY INFO \_ \_ \_ DATA** identifica un campo de información de trabajo o impresora y proporciona los datos actuales para ese campo.

La [**función FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) devuelve una estructura [**PRINTER NOTIFY \_ \_ INFO,**](printer-notify-info.md) que contiene una matriz de **estructuras PRINTER NOTIFY INFO \_ \_ \_ DATA.**

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_NOTIFY_INFO_DATA {
  WORD  Type;
  WORD  Field;
  DWORD Reserved;
  DWORD Id;
  union {
    DWORD  adwData[2];
    struct {
      DWORD  cbBuf;
      LPVOID pBuf;
    } Data;
  } NotifyData;
} PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tipo**
</dt> <dd>

Indica el tipo de información proporcionada. Este miembro puede ser uno de los siguientes valores.



| Valor                                                                                                                                                                                                                                      | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**JOB \_ NOTIFICACIÓN \_ DE TIPO**</dt> <dt>0x01</dt> </dl>             | Indica que el miembro **Field** especifica una constante JOB \_ NOTIFY \_ \_ \* FIELD.<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**IMPRESORA \_ NOTIFICACIÓN \_ DE TIPO**</dt> <dt>0x00</dt> </dl> | Indica que el miembro **Field** especifica una constante PRINTER \_ NOTIFY \_ \_ \* FIELD.<br/> |



 

</dd> <dt>

**Campo**
</dt> <dd>

Indica el campo que ha cambiado. Para obtener una lista de los valores posibles, consulte la sección Comentarios.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**Id**
</dt> <dd>

Indica el identificador de trabajo si el **miembro Type** especifica JOB \_ NOTIFY \_ TYPE. Si el **miembro Type** especifica PRINTER \_ NOTIFY \_ TYPE, este miembro no está definido.

</dd> <dt>

**NotifyData**
</dt> <dd>

Unión de información de datos basada en los **miembros Type** **y Field.** Para obtener una descripción del tipo de datos asociado a cada campo, vea la sección Comentarios.

<dl> <dt>

**adwData \[ 2\]**
</dt> <dd>

Matriz de dos **valores DWORD.** Para los campos de información que usan solo un **DWORD** único, los datos están **en adwData** \[ \] 0.

</dd> <dt>

**Datos**
</dt> <dd> <dl> <dt>

**cbBuf**
</dt> <dd>

Indica el tamaño, en bytes, del búfer al que apunta **pBuf**.

</dd> <dt>

**pBuf**
</dt> <dd>

Puntero a un búfer que contiene los datos actuales del campo.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Si el **miembro Type** especifica PRINTER \_ NOTIFY \_ TYPE, el miembro **Field** puede ser uno de los siguientes valores.



<table>
<thead>
<tr class="header">
<th>Campo</th>
<th>Tipo de datos</th>
<th>Valor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SERVER_NAME</td>
<td>No compatible.</td>
<td>0x00</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINTER_NAME</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en NULL que contiene el nombre de la impresora.</td>
<td>0x01</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SHARE_NAME</td>
<td><strong>pBuf es</strong> un puntero a una cadena terminada en NULL que identifica el punto de recurso compartido de la impresora.</td>
<td>0x02</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PORT_NAME</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en NULL que contiene el nombre del puerto en el que se imprimirán los trabajos de impresión. Si &quot; la agrupación de &quot; impresoras está seleccionada, se trata de una lista separada por comas de puertos.</td>
<td>0x03</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_DRIVER_NAME</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en NULL que contiene el nombre del controlador de la impresora.</td>
<td>0x04</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_COMMENT</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en NULL que contiene la nueva cadena de comentario, que suele ser una breve descripción de la impresora.</td>
<td>0x05</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_LOCATION</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en NULL que contiene la nueva ubicación física de la impresora (por ejemplo, &quot; Bldg. 38, Sala 1164 &quot; ).</td>
<td>0x06</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEVMODE</td>
<td><strong>pBuf es</strong> un puntero a una estructura <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> que define los datos de impresora predeterminados, como la orientación del papel y la resolución.</td>
<td>0x07</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SEPFILE</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en NULL que especifica el nombre del archivo utilizado para crear la página separadora. Esta página se usa para separar los trabajos de impresión enviados a la impresora.</td>
<td>0x08</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en NULL que especifica el nombre del procesador de impresión utilizado por la impresora.</td>
<td>0x09</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PARAMETERS</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en NULL que especifica los parámetros predeterminados del procesador de impresión.</td>
<td>0x0A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DATATYPE</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en NULL que especifica el tipo de datos utilizado para registrar el trabajo de impresión.</td>
<td>0x0B</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</td>
<td><strong>pBuf</strong> es un puntero a una <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> estructura de la impresora. El puntero puede ser <strong>NULL</strong> si no hay ningún descriptor de seguridad.</td>
<td>0x0C</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_ATTRIBUTES</td>
<td><strong>adwData</strong> [0] especifica los atributos de impresora, que pueden ser uno de los siguientes valores:<dl> PRINTER_ATTRIBUTE_QUEUED<br />
PRINTER_ATTRIBUTE_DIRECT<br />
PRINTER_ATTRIBUTE_DEFAULT<br />
PRINTER_ATTRIBUTE_SHARED<br />
</dl></td>
<td>0x0D</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PRIORITY</td>
<td><strong>adwData</strong> [0] especifica un valor de prioridad que el colador usa para enrutar los trabajos de impresión.</td>
<td>0x0E</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</td>
<td><strong>adwData</strong> [0] especifica el valor de prioridad predeterminado asignado a cada trabajo de impresión.</td>
<td>0x0F</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_START_TIME</td>
<td><strong>adwData</strong> [0] especifica la hora más temprana en la que la impresora imprimirá un trabajo. (Este valor se especifica en minutos transcurridos desde las 12:00 a.m.)</td>
<td>0x10</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_UNTIL_TIME</td>
<td><strong>adwData</strong> [0] especifica la hora más reciente a la que la impresora imprimirá un trabajo. (Este valor se especifica en minutos transcurridos desde las 12:00 a.m.).</td>
<td>0x11</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_STATUS</td>
<td><strong>adwData</strong> [0] especifica el estado de la impresora. Para obtener una lista de los valores posibles, vea <a href="printer-info-2.md"><strong>la PRINTER_INFO_2</strong></a> estructura.</td>
<td>0x12</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_STATUS_STRING</td>
<td>No compatible.</td>
<td>0x13</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_CJOBS</td>
<td><strong>adwData</strong> [0] especifica el número de trabajos de impresión que se han puesto en cola para la impresora.</td>
<td>0x14</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_AVERAGE_PPM</td>
<td><strong>adwData</strong> [0] especifica el número medio de páginas por minuto que se han impreso en la impresora.</td>
<td>0x15</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_TOTAL_PAGES</td>
<td>No compatible.</td>
<td>0x16</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PAGES_PRINTED</td>
<td>No compatible.</td>
<td>0 x 17</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_TOTAL_BYTES</td>
<td>No compatible.</td>
<td>0x18</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_BYTES_PRINTED</td>
<td>No compatible.</td>
<td>0x19</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_OBJECT_GUID</td>
<td>Se establece si cambia el GUID del objeto.</td>
<td>0x1A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</td>
<td>Se establece si se cambia el nombre de la conexión de impresora.</td>
<td>0x1B</td>
</tr>
</tbody>
</table>



 

Si el **miembro Type** especifica JOB \_ NOTIFY \_ TYPE, el miembro **Field** puede ser uno de los valores siguientes.



| Campo                                    | Tipo de datos                                                                                                                                                                                                                                            | Valor |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| NOMBRE DE \_ LA IMPRESORA DEL CAMPO DE NOTIFICACIÓN DE \_ \_ \_ TRABAJO        | **pBuf** es un puntero a una cadena terminada en NULL que contiene el nombre de la impresora para la que se encuentra en cola el trabajo.                                                                                                                                      | 0x00  |
| NOMBRE DE \_ LA MÁQUINA DEL CAMPO DE NOTIFICACIÓN DE \_ \_ \_ TRABAJO        | **pBuf** es un puntero a una cadena terminada en NULL que especifica el nombre de la máquina que creó el trabajo de impresión.                                                                                                                                    | 0x01  |
| NOMBRE DE \_ PUERTO DE CAMPO DE NOTIFICACIÓN DE \_ \_ \_ TRABAJO           | **pBuf** es un puntero a una cadena terminada en NULL que identifica los puertos utilizados para transmitir datos a la impresora. Si una impresora está conectada a más de un puerto, los nombres de los puertos se separan por comas (por ejemplo, "LPT1:,LPT2:,LPT3:"). | 0x02  |
| NOMBRE DE \_ USUARIO DEL CAMPO DE NOTIFICACIÓN DE \_ \_ \_ TRABAJO           | **pBuf** es un puntero a una cadena terminada en NULL que especifica el nombre del usuario que envió el trabajo de impresión.                                                                                                                                           | 0x03  |
| NOMBRE DE \_ NOTIFICACIÓN DE CAMPO DE NOTIFICACIÓN DE \_ \_ \_ TRABAJO         | **pBuf** es un puntero a una cadena terminada en NULL que especifica el nombre del usuario al que se debe notificar cuando se ha impreso el trabajo o cuando se produce un error al imprimir el trabajo.                                                              | 0x04  |
| JOB \_ NOTIFY \_ FIELD \_ DATATYPE             | **pBuf** es un puntero a una cadena terminada en NULL que especifica el tipo de datos usados para registrar el trabajo de impresión.                                                                                                                                         | 0x05  |
| PROCESADOR DE \_ IMPRESIÓN DE CAMPO DE NOTIFICACIÓN DE \_ \_ \_ TRABAJO     | **pBuf** es un puntero a una cadena terminada en NULL que especifica el nombre del procesador de impresión que se va a usar para imprimir el trabajo.                                                                                                                           | 0x06  |
| PARÁMETROS DE \_ CAMPO DE NOTIFICACIÓN DE \_ \_ TRABAJO           | **pBuf** es un puntero a una cadena terminada en NULL que especifica los parámetros del procesador de impresión.                                                                                                                                                            | 0x07  |
| NOMBRE DEL \_ CONTROLADOR DEL CAMPO DE NOTIFICACIÓN DE \_ \_ \_ TRABAJO         | **pBuf** es un puntero a una cadena terminada en NULL que especifica el nombre del controlador de impresora que se debe usar para procesar el trabajo de impresión.                                                                                                           | 0x08  |
| JOB \_ NOTIFY \_ FIELD \_ DEVMODE              | **pBuf es** un puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contiene datos de entorno y inicialización de dispositivos para el controlador de impresora.                                                                                                        | 0x09  |
| ESTADO DE \_ CAMPO DE NOTIFICACIÓN DE \_ \_ TRABAJO               | **adwData** \[ 0 \] especifica el estado del trabajo. Para obtener una lista de valores posibles, vea la [**estructura \_ JOB INFO \_ 2.**](job-info-2.md)                                                                                                                        | 0x0A  |
| CADENA DE \_ ESTADO DE CAMPO DE NOTIFICACIÓN DE \_ \_ \_ TRABAJO       | **pBuf** es un puntero a una cadena terminada en NULL que especifica el estado del trabajo de impresión.                                                                                                                                                           | 0x0B  |
| DESCRIPTOR DE \_ SEGURIDAD DE CAMPO DE NOTIFICACIÓN DE \_ \_ \_ TRABAJO | No compatible.                                                                                                                                                                                                                                          | 0x0C  |
| DOCUMENTO DE \_ CAMPO DE NOTIFICACIÓN DE \_ \_ TRABAJO             | **pBuf** es un puntero a una cadena terminada en NULL que especifica el nombre del trabajo de impresión (por ejemplo, "MS-WORD: Review.doc").                                                                                                                        | 0x0D  |
| PRIORIDAD \_ DE CAMPO DE NOTIFICACIÓN DE \_ \_ TRABAJO             | **adwData** \[ 0 \] especifica la prioridad del trabajo.                                                                                                                                                                                                           | 0x0E  |
| POSICIÓN DE \_ CAMPO DE NOTIFICACIÓN DE \_ \_ TRABAJO             | **adwData** \[ 0 \] especifica la posición del trabajo en la cola de impresión.                                                                                                                                                                                      | 0x0F  |
| CAMPO \_ DE NOTIFICACIÓN DE TRABAJO \_ \_ ENVIADO            | **pBuf** es un puntero a una [**estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica la hora a la que se envió el trabajo.                                                                                                                          | 0x10  |
| HORA DE \_ INICIO DEL CAMPO DE NOTIFICACIÓN DE \_ \_ \_ TRABAJO          | **adwData** \[ 0 \] especifica la primera vez que se puede imprimir el trabajo. (Este valor se especifica en minutos transcurridos desde las 12:00 a.m.).                                                                                                                | 0x11  |
| CAMPO NOTIFICACIÓN \_ DE TRABAJO HASTA LA \_ \_ \_ HORA          | **adwData** \[ 0 \] especifica la hora más reciente en la que se puede imprimir el trabajo. (Este valor se especifica en minutos transcurridos desde las 12:00 a.m.).                                                                                                                  | 0x12  |
| TIEMPO DE \_ CAMPO DE NOTIFICACIÓN DEL \_ \_ TRABAJO                 | **adwData** \[ 0 especifica el tiempo total, en segundos, que ha transcurrido desde que \] el trabajo empezó a imprimirse.                                                                                                                                                  | 0x13  |
| PÁGINAS TOTALES \_ DE CAMPOS DE NOTIFICACIÓN DE \_ \_ \_ TRABAJO         | **adwData** \[ 0 \] especifica el tamaño, en páginas, del trabajo.                                                                                                                                                                                             | 0x14  |
| PÁGINAS \_ DE CAMPOS DE NOTIFICACIÓN DE TRABAJO \_ \_ \_ IMPRESAS       | **adwData** \[ 0 \] especifica el número de páginas que se han impreso.                                                                                                                                                                                      | 0x15  |
| BYTES TOTALES \_ DE CAMPO DE NOTIFICACIÓN DE \_ \_ \_ TRABAJO         | **adwData** \[ 0 \] especifica el tamaño, en bytes, del trabajo.                                                                                                                                                                                             | 0x16  |
| BYTES DE \_ CAMPO DE NOTIFICACIÓN DE TRABAJO \_ \_ \_ IMPRESOS       | **adwData** \[ 0 \] especifica el número de bytes que se han impreso en este trabajo. Para este campo, el objeto de notificación de cambios se señala cuando se envían bytes a la impresora.                                                                      | 0 x 17  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ TRABAJO 2**](job-info-2.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 2**](printer-info-2.md)
</dt> <dt>

[**INFORMACIÓN DE \_ NOTIFICACIÓN DE \_ IMPRESORA**](printer-notify-info.md)
</dt> <dt>

[**DESCRIPTOR \_ DE SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

