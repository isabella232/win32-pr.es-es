---
description: La estructura de datos de notificación de la impresora \_ \_ \_ identifica un campo de información de la impresora o del trabajo y proporciona los datos actuales para ese campo.
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: Estructura de PRINTER_NOTIFY_INFO_DATA (winspool. h)
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
ms.openlocfilehash: 4c76ffe70a8388e920b5f8576830e31ed23edc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277250"
---
# <a name="printer_notify_info_data-structure"></a>\_Estructura de \_ \_ datos de notificación de impresora

La estructura de **\_ \_ \_ datos de notificación** de la impresora identifica un campo de información de la impresora o del trabajo y proporciona los datos actuales para ese campo.

La función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) devuelve una estructura de [**\_ \_ información de notificación de impresora**](printer-notify-info.md) , que contiene una matriz de estructuras de **\_ \_ \_ datos de información de notificación de impresora** .

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

Indica el tipo de información proporcionado. Este miembro puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                      | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**Trabajo \_ de NOTIFICAr \_ tipo**</dt> <dt>0x01</dt> </dl>             | Indica que el miembro de **campo** especifica una \_ constante de campo de notificación de trabajo \_ \_ \* .<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**Impresora \_ de NOTIFICAr el \_ tipo**</dt> <dt>0x00</dt> </dl> | Indica que el miembro de **campo** especifica una \_ constante de campo de notificación de impresora \_ \_ \* .<br/> |



 

</dd> <dt>

**Campo**
</dt> <dd>

Indica el campo que ha cambiado. Para obtener una lista de los valores posibles, vea la sección Comentarios.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**Id**
</dt> <dd>

Indica el identificador de trabajo si el miembro de **tipo** especifica el tipo de notificación de trabajo \_ \_ . Si el miembro de **tipo** especifica \_ el \_ tipo de notificación de la impresora, este miembro es indefinido.

</dd> <dt>

**NotifyData**
</dt> <dd>

Unión de información de datos basada en los miembros de **campo** y **tipo** . Para obtener una descripción del tipo de datos asociado a cada campo, vea la sección Comentarios.

<dl> <dt>

**adwData \[ 2\]**
</dt> <dd>

Matriz de dos valores **DWORD** . En el caso de los campos de información que usan un solo **DWORD**, los datos están en **adwData** \[ 0 \] .

</dd> <dt>

**Data**
</dt> <dd> <dl> <dt>

**cbBuf**
</dt> <dd>

Indica el tamaño, en bytes, del búfer al que apunta **pBuf**.

</dd> <dt>

**pBuf**
</dt> <dd>

Puntero a un búfer que contiene los datos actuales del campo.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Si el miembro de **tipo** especifica el \_ tipo de notificación de impresora \_ , el miembro de **campo** puede tener uno de los valores siguientes.



<table>
<thead>
<tr class="header">
<th>Campo</th>
<th>Tipo de datos</th>
<th>Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SERVER_NAME</td>
<td>No se admite.</td>
<td>0x00</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINTER_NAME</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en null que contiene el nombre de la impresora.</td>
<td>0x01</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SHARE_NAME</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en null que identifica el punto de recurso compartido para la impresora.</td>
<td>0x02</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PORT_NAME</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en null que contiene el nombre del puerto en el que se imprimirán los trabajos de impresión. Si &quot; &quot; se selecciona agrupación de impresoras, se trata de una lista separada por comas de puertos.</td>
<td>0x03</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_DRIVER_NAME</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en null que contiene el nombre del controlador de la impresora.</td>
<td>0x04</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_COMMENT</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en null que contiene la nueva cadena de comentario, que suele ser una breve descripción de la impresora.</td>
<td>0x05</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_LOCATION</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en null que contiene la nueva ubicación física de la impresora (por ejemplo, &quot; Bldg. 38, habitación 1164 &quot; ).</td>
<td>0x06</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEVMODE</td>
<td><strong>pBuf</strong> es un puntero a una estructura <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> que define los datos de impresora predeterminados, como la orientación del papel y la resolución.</td>
<td>0x07</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SEPFILE</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en null que especifica el nombre del archivo usado para crear la página separadora. Esta página se utiliza para separar los trabajos de impresión que se envían a la impresora.</td>
<td>0x08</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en null que especifica el nombre del procesador de impresión utilizado por la impresora.</td>
<td>0x09</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PARAMETERS</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en null que especifica los parámetros predeterminados del procesador de impresión.</td>
<td>0x0A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DATATYPE</td>
<td><strong>pBuf</strong> es un puntero a una cadena terminada en null que especifica el tipo de datos utilizado para registrar el trabajo de impresión.</td>
<td>0x0B</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</td>
<td><strong>pBuf</strong> es un puntero a una estructura de <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> para la impresora. El puntero puede ser <strong>null</strong> si no hay ningún descriptor de seguridad.</td>
<td>0x0C</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_ATTRIBUTES</td>
<td><strong>adwData</strong> [0] especifica los atributos de la impresora, que pueden ser uno de los siguientes valores:<dl> PRINTER_ATTRIBUTE_QUEUED<br />
PRINTER_ATTRIBUTE_DIRECT<br />
PRINTER_ATTRIBUTE_DEFAULT<br />
PRINTER_ATTRIBUTE_SHARED<br />
</dl></td>
<td>0x0D</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PRIORITY</td>
<td><strong>adwData</strong> [0] especifica un valor de prioridad que el administrador de trabajos de impresión utiliza para enrutar los trabajos de impresión.</td>
<td>0x0E</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</td>
<td><strong>adwData</strong> [0] especifica el valor de prioridad predeterminado asignado a cada trabajo de impresión.</td>
<td>0x0F</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_START_TIME</td>
<td><strong>adwData</strong> [0] especifica la primera hora en la que la impresora imprimirá un trabajo. (Este valor se especifica en minutos transcurridos desde las 12:00 A.M.)</td>
<td>0x10</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_UNTIL_TIME</td>
<td><strong>adwData</strong> [0] especifica la hora más reciente en la que la impresora imprimirá un trabajo. (Este valor se especifica en minutos transcurridos desde las 12:00 A.M.)</td>
<td>0x11</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_STATUS</td>
<td><strong>adwData</strong> [0] especifica el estado de la impresora. Para obtener una lista de los valores posibles, vea la estructura <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> .</td>
<td>0X12</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_STATUS_STRING</td>
<td>No se admite.</td>
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
<td>No se admite.</td>
<td>0x16</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PAGES_PRINTED</td>
<td>No se admite.</td>
<td>0 x 17</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_TOTAL_BYTES</td>
<td>No se admite.</td>
<td>0x18</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_BYTES_PRINTED</td>
<td>No se admite.</td>
<td>0x19</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_OBJECT_GUID</td>
<td>Se establece si el GUID del objeto cambia.</td>
<td>0x1A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</td>
<td>Se establece si se cambia el nombre de la conexión de impresora.</td>
<td>0x1B</td>
</tr>
</tbody>
</table>



 

Si el miembro de **tipo** especifica el \_ tipo de notificación de trabajo \_ , el miembro de **campo** puede ser uno de los valores siguientes.



| Campo                                    | Tipo de datos                                                                                                                                                                                                                                            | Value |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| \_nombre de \_ impresora del campo de notificación de trabajo \_ \_        | **pBuf** es un puntero a una cadena terminada en null que contiene el nombre de la impresora para la que se pone en cola el trabajo.                                                                                                                                      | 0x00  |
| \_nombre de \_ equipo de campo de notificación de trabajo \_ \_        | **pBuf** es un puntero a una cadena terminada en null que especifica el nombre del equipo que creó el trabajo de impresión.                                                                                                                                    | 0x01  |
| \_nombre de \_ Puerto de campo de notificación de trabajo \_ \_           | **pBuf** es un puntero a una cadena terminada en null que identifica los puertos que se usan para transmitir datos a la impresora. Si una impresora está conectada a más de un puerto, los nombres de los puertos se separan por comas (por ejemplo, "LPT1:, LPT2:, LPT3:"). | 0x02  |
| \_nombre de \_ usuario del campo de notificación de trabajo \_ \_           | **pBuf** es un puntero a una cadena terminada en null que especifica el nombre del usuario que envió el trabajo de impresión.                                                                                                                                           | 0x03  |
| \_nombre de \_ notificación de campo de notificación de trabajo \_ \_         | **pBuf** es un puntero a una cadena terminada en null que especifica el nombre del usuario al que se debe notificar cuando se ha impreso el trabajo o cuando se produce un error durante la impresión del trabajo.                                                              | 0x04  |
| \_tipo de \_ campo de notificación de trabajo \_             | **pBuf** es un puntero a una cadena terminada en null que especifica el tipo de datos que se usa para registrar el trabajo de impresión.                                                                                                                                         | 0x05  |
| \_procesador de \_ impresión de campo de notificación de trabajo \_ \_     | **pBuf** es un puntero a una cadena terminada en null que especifica el nombre del procesador de impresión que se va a usar para imprimir el trabajo.                                                                                                                           | 0x06  |
| \_parámetros de \_ campo de notificación de trabajo \_           | **pBuf** es un puntero a una cadena terminada en null que especifica los parámetros del procesador de impresión.                                                                                                                                                            | 0x07  |
| \_nombre del \_ controlador de campo de notificación de trabajo \_ \_         | **pBuf** es un puntero a una cadena terminada en null que especifica el nombre del controlador de impresora que se debe usar para procesar el trabajo de impresión.                                                                                                           | 0x08  |
| campo de notificación de trabajo \_ \_ \_ DEVMODE              | **pBuf** es un puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contiene datos de entorno y de inicialización del dispositivo para el controlador de impresora.                                                                                                        | 0x09  |
| \_Estado de \_ campo de notificación de trabajo \_               | **adwData** \[ 0 \] especifica el estado del trabajo. Para obtener una lista de los valores posibles, consulte la estructura [**Job \_ info \_ 2**](job-info-2.md) .                                                                                                                        | 0x0A  |
| \_cadena de \_ Estado de campo de notificación de trabajo \_ \_       | **pBuf** es un puntero a una cadena terminada en null que especifica el estado del trabajo de impresión.                                                                                                                                                           | 0x0B  |
| \_descriptor de seguridad de campo de notificación de trabajo \_ \_ \_ | No se admite.                                                                                                                                                                                                                                          | 0x0C  |
| \_documento de \_ campo de notificación de trabajo \_             | **pBuf** es un puntero a una cadena terminada en null que especifica el nombre del trabajo de impresión (por ejemplo, "MS-WORD: Review.doc").                                                                                                                        | 0x0D  |
| \_prioridad de \_ campo de notificación de trabajo \_             | **adwData** \[ 0 \] especifica la prioridad del trabajo.                                                                                                                                                                                                           | 0x0E  |
| \_posición del \_ campo de notificación del trabajo \_             | **adwData** \[ 0 \] especifica la posición del trabajo en la cola de impresión.                                                                                                                                                                                      | 0x0F  |
| campo de notificación de trabajo \_ \_ \_ enviado            | **pBuf** es un puntero a una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica la hora a la que se envió el trabajo.                                                                                                                          | 0x10  |
| \_hora de \_ Inicio del campo de notificación de trabajo \_ \_          | **adwData** \[ 0 \] especifica la hora más temprana en que se puede imprimir el trabajo. (Este valor se especifica en minutos transcurridos desde las 12:00 A.M.)                                                                                                                | 0x11  |
| campo de notificación de trabajo \_ \_ hasta la \_ \_ hora          | **adwData** \[ 0 \] especifica la última hora a la que se puede imprimir el trabajo. (Este valor se especifica en minutos transcurridos desde las 12:00 A.M.)                                                                                                                  | 0X12  |
| \_tiempo de \_ campo de notificación de trabajo \_                 | **adwData** \[ 0 \] especifica el tiempo total, en segundos, que ha transcurrido desde que comenzó la impresión del trabajo.                                                                                                                                                  | 0x13  |
| \_ \_ páginas totales de campo de notificación de \_ trabajo \_         | **adwData** \[ 0 \] especifica el tamaño, en páginas, del trabajo.                                                                                                                                                                                             | 0x14  |
| páginas de campo de notificación de trabajo \_ \_ \_ \_ impresas       | **adwData** \[ 0 \] especifica el número de páginas que se han impreso.                                                                                                                                                                                      | 0x15  |
| \_ \_ bytes totales de campo de notificación \_ de trabajo \_         | **adwData** \[ 0 \] especifica el tamaño, en bytes, del trabajo.                                                                                                                                                                                             | 0x16  |
| \_bytes de campo de notificación de trabajo \_ \_ \_ impresos       | **adwData** \[ 0 \] especifica el número de bytes que se han impreso en este trabajo. En este campo, el objeto de notificación de cambios se señaliza cuando se envían bytes a la impresora.                                                                      | 0 x 17  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**Información de trabajo \_ \_ 2**](job-info-2.md)
</dt> <dt>

[**Información de la impresora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_información de notificación de impresora \_**](printer-notify-info.md)
</dt> <dt>

[**descriptor de seguridad \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

