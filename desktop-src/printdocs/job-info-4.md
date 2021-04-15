---
description: Describe un conjunto completo de valores asociados a un trabajo y admite archivos de cola de impresión grandes con tamaños expresados con 64 bits.
ms.assetid: 90932ae2-ea9e-43bc-9a1d-c68223f6d0ee
title: Estructura de JOB_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_4
- _JOB_INFO_4A
- _JOB_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5a6ccd7bf589ed341c9aceab86205cd9852c0896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649253"
---
# <a name="job_info_4-structure"></a>Estructura de información de trabajo \_ \_ 4

Describe un conjunto completo de valores asociados a un trabajo y admite archivos de cola de impresión grandes con tamaños expresados con 64 bits.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _JOB_INFO_4 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
  LONG                 SizeHigh;
} JOB_INFO_4, *PJOB_INFO_4;
```



## <a name="members"></a>Miembros

<dl> <dt>

**JobId**
</dt> <dd>

Un valor de identificador de trabajo.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre de la impresora para la que se pone en cola el trabajo.

</dd> <dt>

**pMachineName**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del equipo que creó el trabajo de impresión.

</dd> <dt>

**pUserName**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el nombre del usuario que posee el trabajo de impresión.

</dd> <dt>

**pDocument**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el nombre del trabajo de impresión (por ejemplo, "MS-WORD: Review.doc").

</dd> <dt>

**pNotifyName**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del usuario al que se debe notificar cuando se ha impreso el trabajo o cuando se produce un error durante la impresión del trabajo.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el tipo de datos utilizado para registrar el trabajo de impresión.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del procesador de impresión que se debe usar para imprimir el trabajo.

</dd> <dt>

**pParameters**
</dt> <dd>

Puntero a una cadena terminada en null que especifica los parámetros del procesador de impresión.

</dd> <dt>

**pDriverName**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del controlador de impresora que se debe usar para procesar el trabajo de impresión.

</dd> <dt>

**pDevMode**
</dt> <dd>

Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contiene los datos de entorno y de inicialización del dispositivo para el controlador de impresora.

</dd> <dt>

**pStatus**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el estado del trabajo de impresión. Este miembro debe comprobarse antes del **Estado** y, si **pStatus** es **null**, el estado se define mediante el contenido del miembro status.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

El valor de este miembro es **null**. En esta versión no se admite la recuperación y configuración de descriptores de seguridad de documentos.

</dd> <dt>

**Estado**
</dt> <dd>

El estado del trabajo. Este miembro puede ser uno o varios de los siguientes valores:

| Value                           | Significado                                                      |
|---------------------------------|--------------------------------------------------------------|
| Estado del trabajo \_ \_ bloqueado \_ DEVQ      | El controlador no puede imprimir el trabajo.                             |
| Estado del trabajo \_ \_ eliminado            | El trabajo se ha eliminado.                                        |
| \_eliminación de estado de trabajo \_           | Se está eliminando el trabajo.                                        |
| \_error de estado de trabajo \_              | Se ha asociado un error al trabajo.                         |
| Estado del trabajo \_ \_ sin conexión            | La impresora está sin conexión.                                          |
| Estado del trabajo \_ \_ PAPEROUT           | La impresora no tiene papel.                                     |
| Estado del trabajo en \_ \_ pausa             | El trabajo está en pausa.                                               |
| Estado del trabajo \_ \_ impreso            | El trabajo se ha impreso.                                             |
| \_impresión de estado del trabajo \_           | El trabajo está imprimiendo.                                             |
| reinicio del estado del trabajo \_ \_            | El trabajo se ha reiniciado.                                      |
| puesta en cola del \_ Estado del trabajo \_           | El trabajo está en cola.                                             |
| Estado del trabajo de \_ \_ intervención del usuario \_ | La impresora tiene un error que requiere que el usuario haga algo. |



 

En Windows XP y versiones posteriores de Windows, también se pueden usar los valores siguientes:

| Value                 | Significado                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| Estado del trabajo \_ \_ completado | El trabajo se envía a la impresora, pero es posible que no se imprima todavía. Vea Comentarios para obtener más información. |
| Estado del trabajo \_ \_ retenido | El trabajo se ha conservado en la cola de impresión después de la impresión.                              |



 

</dd> <dt>

**Prioridad**
</dt> <dd>

La prioridad del trabajo. Este miembro puede ser uno de los valores siguientes o en el intervalo comprendido entre 1 y 99 ( \_ prioridad mínima a través de la \_ prioridad máxima).



| Value         | Significado           |
|---------------|-------------------|
| \_prioridad mínima | Prioridad mínima. |
| \_prioridad máxima | Prioridad máxima. |
| prioridad de DEF \_ | Prioridad predeterminada. |



 

</dd> <dt>

**Position**
</dt> <dd>

Posición del trabajo en la cola de impresión.

</dd> <dt>

**StartTime**
</dt> <dd>

La primera vez que se puede imprimir el trabajo.

</dd> <dt>

**UntilTime**
</dt> <dd>

La última vez que se puede imprimir el trabajo.

</dd> <dt>

**TotalPages**
</dt> <dd>

Número de páginas necesarias para el trabajo. Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de página.

</dd> <dt>

**Tamaño**
</dt> <dd>

Los cuatro bytes inferiores del tamaño, en bytes, del trabajo. Vea también el miembro **SizeHigh** a continuación.

</dd> <dt>

**Enviado**
</dt> <dd>

Estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica la hora A la que se envió el trabajo.

Este valor de hora está en formato de horario universal coordinado (UTC). Debe convertirlo en un valor de hora local antes de mostrarlo. Puede usar la función [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) para realizar la conversión.

</dd> <dt>

**Time**
</dt> <dd>

El tiempo total, en milisegundos, que ha transcurrido desde que comenzó la impresión del trabajo.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Número de páginas que se han imprimido. Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de página.

</dd> <dt>

**SizeHigh**
</dt> <dd>

Los cuatro bytes superiores del tamaño, en bytes, del trabajo. Vea también el miembro de **tamaño** anterior.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los monitores de puerto que no admiten TrueEndOfJob establecerán el trabajo como estado del trabajo \_ \_ impreso inmediatamente después de enviar el trabajo a la impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Winspool. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ Información del trabajo \_ \_ 4W** (Unicode) y la **\_ información del trabajo \_ \_ 4A** (ANSI)<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

