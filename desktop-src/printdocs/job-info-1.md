---
description: La estructura JOB INFO 1 especifica información del trabajo de impresión, como el valor del identificador de trabajo, el nombre de la impresora para la que se encuentra en cola el trabajo, el nombre de la máquina que creó el trabajo de impresión, el nombre del usuario que posee el trabajo de impresión, y así \_ \_ sucesivamente.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: JOB_INFO_1 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_1
- _JOB_INFO_1A
- _JOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c6e8d5900a0f2d0a2dce5c12d2629abfc80776cdc0ada1354070005e28fbcd37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971334"
---
# <a name="job_info_1-structure"></a>Estructura \_ JOB INFO \_ 1

La estructura **\_ JOB INFO \_ 1** especifica información del trabajo de impresión, como el valor del identificador de trabajo, el nombre de la impresora para la que se encuentra en cola el trabajo, el nombre de la máquina que creó el trabajo de impresión, el nombre del usuario que posee el trabajo de impresión, y así sucesivamente.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _JOB_INFO_1 {
  DWORD      JobId;
  LPTSTR     pPrinterName;
  LPTSTR     pMachineName;
  LPTSTR     pUserName;
  LPTSTR     pDocument;
  LPTSTR     pDatatype;
  LPTSTR     pStatus;
  DWORD      Status;
  DWORD      Priority;
  DWORD      Position;
  DWORD      TotalPages;
  DWORD      PagesPrinted;
  SYSTEMTIME Submitted;
} JOB_INFO_1, *PJOB_INFO_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**JobId**
</dt> <dd>

Identificador de trabajo.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre de la impresora para la que se ha puesto en cola el trabajo.

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

**pDatatype**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el tipo de datos usados para registrar el trabajo de impresión.

</dd> <dt>

**pStatus**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el estado del trabajo de impresión. Este miembro debe comprobarse antes de *Status* y, si *pStatus* es **NULL,** el estado se define mediante el contenido del miembro Status.

</dd> <dt>

**Estado**
</dt> <dd>

Estado del trabajo. El valor de este miembro puede ser cero o una combinación de uno o varios de los valores siguientes. Un valor de cero indica que la cola de impresión se ha pausado después de que el documento terminara de poner en cola.



| Value                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ESTADO \_ DEL TRABAJO BLOQUEADO \_ \_ DEVQ      | El controlador no puede imprimir el trabajo.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ESTADO \_ DEL \_ TRABAJO COMPLETADO           | **Windows XP y versiones posteriores:** El trabajo se envía a la impresora, pero es posible que el trabajo no se haya impreso todavía.<br/> Vea Comentarios para obtener más información.<br/>                                                                                                                                                                                                                                                                                                                           |
| ESTADO \_ DEL \_ TRABAJO ELIMINADO            | Se ha eliminado el trabajo.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ELIMINACIÓN \_ \_ DEL ESTADO DEL TRABAJO           | Se está eliminando el trabajo.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ERROR DE \_ ESTADO DEL \_ TRABAJO              | Se asocia un error al trabajo.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ESTADO DEL \_ TRABAJO \_ SIN CONEXIÓN            | La impresora está sin conexión.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| DOCUMENTO DE \_ ESTADO \_ DEL TRABAJO           | La impresora está sin papel.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ESTADO \_ DEL TRABAJO EN \_ PAUSA             | El trabajo está en pausa.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ESTADO \_ DEL \_ TRABAJO IMPRESO            | El trabajo se ha impreso.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| IMPRESIÓN DEL \_ ESTADO DEL \_ TRABAJO           | El trabajo está imprimendo.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| REINICIO DEL \_ ESTADO DEL \_ TRABAJO            | Se ha reiniciado el trabajo.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ESTADO \_ DEL \_ TRABAJO RETENIDO           | **Windows Vista y versiones posteriores:** El trabajo se ha conservado en la cola de impresión y no se puede eliminar. Esto puede deberse a lo siguiente:<br/> 1) El trabajo se retuvo manualmente mediante una llamada a SetJob y el colador está esperando a que se liberara el trabajo.<br/> 2) El trabajo no ha terminado de imprimirse y debe finalizar la impresión antes de que se pueda eliminar automáticamente.<br/> Consulte [**SetJob para**](setjob.md) obtener más información sobre los comandos de trabajo de impresión.<br/> |
| JOB \_ STATUS \_ SPOOLING           | El trabajo está en cola.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| INTERVENCIÓN \_ DEL USUARIO DEL ESTADO DEL \_ \_ TRABAJO | La impresora tiene un error que requiere que el usuario haga algo.                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**Prioridad**
</dt> <dd>

Prioridad del trabajo. Este miembro puede ser uno de los siguientes valores o en el intervalo entre 1 y 99 (PRIORIDAD MÍNIMA \_ a PRIORIDAD \_ MÁXIMA).



| Value         | Significado           |
|---------------|-------------------|
| PRIORIDAD \_ MÍNIMA | Prioridad mínima. |
| PRIORIDAD \_ MÁXIMA | Prioridad máxima. |
| PRIORIDAD \_ DEF | Prioridad predeterminada. |



 

</dd> <dt>

**Position**
</dt> <dd>

Posición del trabajo en la cola de impresión.

</dd> <dt>

**TotalPages**
</dt> <dd>

Número total de páginas que contiene el documento. Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de páginas.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Número de páginas que se han impreso. Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de páginas.

</dd> <dt>

**Enviado**
</dt> <dd>

Estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica la hora a la que se ha colado este documento.

Este valor de hora está en formato de coordenadas de hora universal (UTC). Debe convertirlo en un valor de hora local antes de mostrarlo. Puede usar la [**función FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) para realizar la conversión.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los monitores de puerto que no admiten TrueEndOfJob establecerán el trabajo como ESTADO DEL TRABAJO IMPRESO justo después de enviar el trabajo \_ \_ a la impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ JOB \_ INFO \_ 1W** (Unicode) e **\_ JOB INFO \_ \_ 1A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

