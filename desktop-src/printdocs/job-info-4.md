---
description: Describe un conjunto completo de valores asociados a un trabajo y admite archivos de cola grandes con tamaños expresados con 64 bits.
ms.assetid: 90932ae2-ea9e-43bc-9a1d-c68223f6d0ee
title: JOB_INFO_4 estructura (Winspool.h)
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
ms.openlocfilehash: dd338b4e6e486c59bfdac705b68c72c56eafb96c9f4e1899e9b4cb3b294791de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091925"
---
# <a name="job_info_4-structure"></a>Estructura JOB \_ INFO \_ 4

Describe un conjunto completo de valores asociados a un trabajo y admite archivos de cola grandes con tamaños expresados con 64 bits.

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

Valor de identificador de trabajo.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre de la impresora para la que se encuentra en cola el trabajo.

</dd> <dt>

**pMachineName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre de la máquina que creó el trabajo de impresión.

</dd> <dt>

**pUserName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del usuario propietario del trabajo de impresión.

</dd> <dt>

**pDocument**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del trabajo de impresión (por ejemplo, "MS-WORD: Review.doc").

</dd> <dt>

**pNotifyName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del usuario al que se debe notificar cuando se ha impreso el trabajo o cuando se produce un error al imprimir el trabajo.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el tipo de datos usados para registrar el trabajo de impresión.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del procesador de impresión que se debe usar para imprimir el trabajo.

</dd> <dt>

**pParameters**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica los parámetros del procesador de impresión.

</dd> <dt>

**pDriverName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del controlador de impresora que se debe usar para procesar el trabajo de impresión.

</dd> <dt>

**pDevMode**
</dt> <dd>

Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contiene datos de inicialización de dispositivos y de entorno para el controlador de impresora.

</dd> <dt>

**pStatus**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el estado del trabajo de impresión. Este miembro debe comprobarse antes de **Status** y, si **pStatus** es **NULL,** el estado se define mediante el contenido del miembro Status.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

El valor de este miembro es **NULL.** La recuperación y configuración de descriptores de seguridad de documentos no se admiten en esta versión.

</dd> <dt>

**Estado**
</dt> <dd>

Estado del trabajo. Este miembro puede ser uno o varios de los siguientes valores:

| Valor                           | Significado                                                      |
|---------------------------------|--------------------------------------------------------------|
| ESTADO \_ DEL TRABAJO BLOQUEADO \_ \_ DEVQ      | El controlador no puede imprimir el trabajo.                             |
| ESTADO \_ DEL \_ TRABAJO ELIMINADO            | Se ha eliminado el trabajo.                                        |
| ELIMINACIÓN \_ DEL \_ ESTADO DEL TRABAJO           | Se está eliminando el trabajo.                                        |
| ERROR DE \_ ESTADO \_ DEL TRABAJO              | Se asocia un error al trabajo.                         |
| ESTADO DEL \_ TRABAJO \_ SIN CONEXIÓN            | La impresora está sin conexión.                                          |
| DOCUMENTO DE \_ ESTADO \_ DEL TRABAJO           | La impresora está sin papel.                                     |
| ESTADO \_ DEL TRABAJO EN \_ PAUSA             | El trabajo está en pausa.                                               |
| ESTADO \_ DEL \_ TRABAJO IMPRESO            | Se ha impreso el trabajo.                                             |
| IMPRESIÓN DEL \_ ESTADO DEL \_ TRABAJO           | El trabajo está imprimiendo.                                             |
| REINICIO DEL \_ ESTADO DEL \_ TRABAJO            | Se ha reiniciado el trabajo.                                      |
| JOB \_ STATUS \_ SPOOLING           | El trabajo está en cola.                                             |
| INTERVENCIÓN \_ DEL USUARIO EN EL ESTADO DEL \_ \_ TRABAJO | La impresora tiene un error que requiere que el usuario haga algo. |



 

En Windows XP y versiones posteriores de Windows, también se pueden usar los siguientes valores:

| Valor                 | Significado                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| ESTADO \_ DEL TRABAJO \_ COMPLETADO | El trabajo se envía a la impresora, pero es posible que aún no se imprima. Vea Comentarios para obtener más información. |
| ESTADO \_ DEL \_ TRABAJO RETENIDO | El trabajo se ha conservado en la cola de impresión después de la impresión.                              |



 

</dd> <dt>

**Prioridad**
</dt> <dd>

Prioridad del trabajo. Este miembro puede ser uno de los siguientes valores, o en el intervalo entre 1 y 99 (PRIORIDAD MÍNIMA \_ a PRIORIDAD \_ MÁXIMA).



| Valor         | Significado           |
|---------------|-------------------|
| PRIORIDAD \_ MÍNIMA | Prioridad mínima. |
| PRIORIDAD \_ MÁXIMA | Prioridad máxima. |
| PRIORIDAD \_ DEF | Prioridad predeterminada. |



 

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

La hora más reciente en la que se puede imprimir el trabajo.

</dd> <dt>

**TotalPages**
</dt> <dd>

Número de páginas necesarias para el trabajo. Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de páginas.

</dd> <dt>

**Tamaño**
</dt> <dd>

Los cuatro bytes inferiores del tamaño, en bytes, del trabajo. Consulte también el **miembro SizeHigh a** continuación.

</dd> <dt>

**Enviado**
</dt> <dd>

Estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica la hora a la que se envió el trabajo.

Este valor de hora está en formato de coordenada de hora universal (UTC). Debe convertirlo a un valor de hora local antes de mostrarlo. Puede usar la [**función FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) para realizar la conversión.

</dd> <dt>

**Time**
</dt> <dd>

Tiempo total, en milisegundos, que ha transcurrido desde que el trabajo empezó a imprimirse.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Número de páginas que se han impreso. Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de páginas.

</dd> <dt>

**SizeHigh**
</dt> <dd>

Los cuatro bytes más altos del tamaño, en bytes, del trabajo. Consulte también el **miembro Size** anterior.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los monitores de puerto que no admiten TrueEndOfJob establecerán el trabajo como ESTADO DEL TRABAJO IMPRESO inmediatamente después de enviar el trabajo \_ \_ a la impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Winspool.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ JOB \_ INFO \_ 4W** (Unicode) e **\_ JOB INFO \_ \_ 4A** (ANSI)<br/>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

