---
description: La \_ estructura Job info \_ 1 especifica información del trabajo de impresión, como el valor del identificador de trabajo, el nombre de la impresora para la que se pone en cola el trabajo, el nombre del equipo que creó el trabajo de impresión, el nombre del usuario que posee el trabajo de impresión, etc.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: Estructura de JOB_INFO_1 (winspool. h)
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
ms.openlocfilehash: d56d4d6bce15a661ce141d8e22d27a15837a9f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361415"
---
# <a name="job_info_1-structure"></a>Estructura de información de trabajo \_ \_ 1

La estructura **Job \_ info \_ 1** especifica información del trabajo de impresión, como el valor del identificador de trabajo, el nombre de la impresora para la que se pone en cola el trabajo, el nombre del equipo que creó el trabajo de impresión, el nombre del usuario que posee el trabajo de impresión, etc.

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

Identificador del trabajo.

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

Puntero a una cadena terminada en null que especifica el nombre del usuario al que pertenece el trabajo de impresión.

</dd> <dt>

**pDocument**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el nombre del trabajo de impresión (por ejemplo, "MS-WORD: Review.doc").

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el tipo de datos utilizado para registrar el trabajo de impresión.

</dd> <dt>

**pStatus**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el estado del trabajo de impresión. Este miembro debe comprobarse antes del *Estado* y, si *pStatus* es **null**, el estado se define mediante el contenido del miembro status.

</dd> <dt>

**Estado**
</dt> <dd>

El estado del trabajo. El valor de este miembro puede ser cero o una combinación de uno o varios de los valores siguientes. Un valor de cero indica que la cola de impresión se pausó una vez finalizada la cola de impresión del documento.



| Value                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Estado del trabajo \_ \_ bloqueado \_ DEVQ      | El controlador no puede imprimir el trabajo.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Estado del trabajo \_ \_ completado           | **Windows XP y versiones posteriores:** El trabajo se envía a la impresora, pero es posible que el trabajo no se imprima todavía.<br/> Vea Comentarios para obtener más información.<br/>                                                                                                                                                                                                                                                                                                                           |
| Estado del trabajo \_ \_ eliminado            | El trabajo se ha eliminado.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_eliminación de estado de trabajo \_           | Se está eliminando el trabajo.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_error de estado de trabajo \_              | Se ha asociado un error al trabajo.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Estado del trabajo \_ \_ sin conexión            | La impresora está sin conexión.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Estado del trabajo \_ \_ PAPEROUT           | La impresora no tiene papel.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Estado del trabajo en \_ \_ pausa             | El trabajo está en pausa.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Estado del trabajo \_ \_ impreso            | El trabajo se ha impreso.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_impresión de estado del trabajo \_           | El trabajo está imprimiendo.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| reinicio del estado del trabajo \_ \_            | El trabajo se ha reiniciado.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Estado del trabajo \_ \_ retenido           | **Windows Vista y versiones posteriores:** El trabajo se ha conservado en la cola de impresión y no se puede eliminar. Esto puede deberse a lo siguiente:<br/> 1) el trabajo se reservó manualmente mediante una llamada a SetJob y el administrador de trabajos de impresión está esperando a que se libere el trabajo.<br/> 2) el trabajo no ha terminado la impresión y debe finalizar la impresión antes de que se pueda eliminar automáticamente.<br/> Vea [**SetJob**](setjob.md) para obtener más información acerca de los comandos de trabajos de impresión.<br/> |
| puesta en cola del \_ Estado del trabajo \_           | El trabajo está en cola.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Estado del trabajo de \_ \_ intervención del usuario \_ | La impresora tiene un error que requiere que el usuario haga algo.                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**Prioridad**
</dt> <dd>

La prioridad del trabajo. Este miembro puede ser uno de los valores siguientes o estar en el intervalo comprendido entre 1 y 99 ( \_ prioridad mínima a través de la \_ prioridad máxima).



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

**TotalPages**
</dt> <dd>

Número total de páginas que contiene el documento. Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de página.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Número de páginas que se han imprimido. Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de página.

</dd> <dt>

**Enviado**
</dt> <dd>

Estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica la hora A la que se puso en cola este documento.

Este valor de hora está en formato de horario universal coordinado (UTC). Debe convertirlo en un valor de hora local antes de mostrarlo. Puede usar la función [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) para realizar la conversión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los monitores de puerto que no son compatibles con TrueEndOfJob establecerán el trabajo como \_ estado \_ del trabajo impreso justo después de enviar el trabajo a la impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ Información del trabajo \_ \_ 1W** (Unicode) y la **\_ información del trabajo \_ \_ 1A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

