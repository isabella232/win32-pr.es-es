---
description: La función SetJob pausa, reanuda, cancela o reinicia un trabajo de impresión en una impresora especificada. También puede usar la función SetJob para establecer parámetros de trabajo de impresión, como la prioridad del trabajo de impresión y el nombre del documento.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: Función SetJob (WinSpool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetJob
- SetJobA
- SetJobW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9259429a7696e832bbbe6d0dd4bbb6fb46e7bce2bf7157122c10ca47656af346
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060025"
---
# <a name="setjob-function"></a>Función SetJob

La **función SetJob** pausa, reanuda, cancela o reinicia un trabajo de impresión en una impresora especificada. También puede usar la función **SetJob** para establecer parámetros de trabajo de impresión, como la prioridad del trabajo de impresión y el nombre del documento.

Puede usar la **función SetJob** para proporcionar un comando a un trabajo de impresión, para establecer parámetros de trabajo de impresión o para realizar ambos en la misma llamada. El valor del parámetro *Command* no afecta al modo en que la función usa los *parámetros Level* y *pJob.* Además, puede usar **SetJob** con [**JOB INFO \_ \_ 3**](job-info-3.md) para vincular un conjunto de trabajos de impresión. Vea Comentarios para obtener más información.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SetJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  JobId,
  _In_ DWORD  Level,
  _In_ LPBYTE pJob,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador del objeto de impresora de interés. Use la [**función OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*JobId* \[ En\]
</dt> <dd>

Identificador que especifica el trabajo de impresión. Para obtener un identificador de trabajo de impresión, llame a [**la función AddJob**](addjob.md) o [**a la función StartDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)

Si el *parámetro Level* se establece en 3, el parámetro *JobId* debe coincidir con el miembro **JobId** de la estructura [**JOB INFO \_ \_ 3**](job-info-3.md) a la que apunta *pJob.*

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Tipo de estructura de información de trabajo a la que apunta el *parámetro pJob.*

**Todas las versiones Windows**: puede establecer el *parámetro Level* en 0, 1 o 2. Cuando se establece *Level en* 0, *pJob* debe ser **NULL.** Use estos valores cuando no esté estableciendo ningún parámetro de trabajo de impresión.

También puede establecer el *parámetro Level* en 3.

A partir **Windows Vista**: también puede establecer el *parámetro Level* en 4.

</dd> <dt>

*pJob* \[ En\]
</dt> <dd>

Puntero a una estructura que establece los parámetros del trabajo de impresión.

**Todas las versiones Windows**: *pJob* puede apuntar a una [**estructura JOB INFO \_ \_ 1**](job-info-1.md) o [**JOB INFO \_ \_ 2.**](job-info-2.md)

*pJob* también puede apuntar a una [**estructura JOB INFO \_ \_ 3.**](job-info-3.md) Debe tener el **permiso de acceso JOB ACCESS \_ \_ ADMINISTER** para los trabajos especificados por los miembros **JobId** y **NextJobId** de la **estructura JOB INFO \_ \_ 3.**

A partir **Windows Vista:** *pJob* también puede apuntar a una [**estructura JOB INFO \_ \_ 4.**](job-info-4.md)

Si el *parámetro Level* es 0, *pJob* debe ser **NULL.**

</dd> <dt>

*Comando* \[ En\]
</dt> <dd>

Operación de trabajo de impresión que se realizará. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                            | Significado                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <dt>**JOB \_ CONTROL \_ CANCEL**</dt> </dl>                                    | No debe usarse. Para eliminar un trabajo de impresión, use **JOB \_ CONTROL \_ DELETE**.<br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <dt>**PAUSA \_ DEL CONTROL DE \_ TRABAJO**</dt> </dl>                                       | Pausar el trabajo de impresión.<br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <dt>**REINICIO \_ DEL CONTROL DE \_ TRABAJO**</dt> </dl>                                 | Reinicie el trabajo de impresión. Un trabajo solo se puede reiniciar si se estaba imprimendo.<br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <dt>**REANUDACIÓN \_ DEL CONTROL \_ DE TRABAJO**</dt> </dl>                                    | Reanudar un trabajo de impresión en pausa.<br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <dt>**ELIMINACIÓN \_ DEL CONTROL \_ DE TRABAJO**</dt> </dl>                                    | Elimine el trabajo de impresión.<br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <dt>**CONTROL DE \_ TRABAJO ENVIADO A LA \_ \_ \_ IMPRESORA**</dt> </dl>       | Lo usan los monitores de puerto para finalizar el trabajo de impresión.<br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <dt>**ÚLTIMA \_ PÁGINA \_ EXPULSADA DEL CONTROL \_ DE \_ TRABAJO**</dt> </dl> | Lo usan los monitores de idioma para finalizar el trabajo de impresión.<br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <dt>**JOB \_ CONTROL \_ RETAIN**</dt> </dl>                                    | **Windows Vista y versiones posteriores:** mantenga el trabajo en la cola después de imprimirlo.<br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <dt>**VERSIÓN DEL \_ CONTROL \_ DE TRABAJO**</dt> </dl>                                 | **Windows Vista y versiones posteriores:** libere el trabajo de impresión.<br/>                     |



 

Puede usar la misma llamada a la función **SetJob** para establecer parámetros de trabajo de impresión y para proporcionar un comando a un trabajo de impresión. Por lo *tanto,* El comando no necesita ser 0 si está estableciendo parámetros de trabajo de impresión, aunque puede serlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Puede usar la función **SetJob** para establecer varios parámetros de trabajo de impresión si proporciona un puntero a una estructura [**JOB INFO \_ \_ 1**](job-info-1.md), [**JOB INFO \_ \_ 2,**](job-info-2.md) [**JOB INFO \_ \_ 3**](job-info-3.md)o [**JOB INFO \_ \_ 4**](job-info-4.md) que contiene los datos necesarios.

Para quitar o eliminar todos los trabajos de impresión de una impresora determinada, llame a la función [**SetPrinter**](setprinter.md) con su parámetro *Command* establecido en **PRINTER CONTROL \_ \_ PURGE**.

Los siguientes miembros de una estructura [**\_ JOB INFO \_ 1,**](job-info-1.md) [**JOB INFO \_ \_ 2**](job-info-2.md)o [**JOB INFO \_ \_ 4**](job-info-4.md) se omiten en una llamada a **SetJob:** **JobId**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **Size**, **Submitted**, **Time** y **TotalPages.**

Debe tener el **permiso de acceso PRINTER ACCESS \_ \_ ADMINISTER** para una impresora con el fin de cambiar la posición de un trabajo de impresión en la cola de impresión.

Si no desea establecer la posición de un trabajo de impresión en la cola de impresión, debe establecer el miembro **Position** de la estructura [**JOB INFO \_ \_ 1**](job-info-1.md), [**JOB INFO \_ \_ 2**](job-info-2.md)o [**JOB INFO \_ \_ 4**](job-info-4.md) en **JOB POSITION \_ \_ UNSPECIFIED**.

Use la **función SetJob** con la estructura [**JOB INFO \_ \_ 3**](job-info-3.md) para vincular un conjunto de trabajos de impresión (también conocido como cadena). Esto resulta útil en situaciones en las que un único documento consta de varias partes que desea representar por separado. Para imprimir los trabajos A, B, C y D en orden, llame a **SetJob** con [**JOB INFO \_ \_ 4**](job-info-4.md) para vincular A a B, B a C y C a D.

Si vincula trabajos de impresión, tenga en cuenta lo siguiente:

-   Los trabajos se pueden agregar al principio o al final de una cadena.
-   Todos los trabajos de la cadena deben tener el mismo tipo de datos.
-   La cadena debe estar completamente vinculada antes de comenzar la cola; de lo contrario, el colador puede imprimir y eliminar trabajos en cola antes de vincularlos todos. Hay dos maneras de evitar que la cadena se imprima prematuramente:

    -   Pause el primer trabajo de la cadena hasta que la cadena esté completamente vinculada. El estado en pausa del primer trabajo rige el estado de todos los trabajos de la cadena.
    -   Mantenga incompleto el primer trabajo, es decir, no llame a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) o [**ScheduleJob**](schedulejob.md) para el primer trabajo. Sin embargo, si "print while spooling" está habilitado (valor predeterminado), este método bloquea el puerto mientras se genera la cadena, lo que también impide la impresión de trabajos no relacionados.

-   La aplicación debe controlar el caso en el que el usuario elimina un trabajo de la cadena antes de que la cadena termine de imprimirse. [**GetLastError devuelve**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) **INVALID \_ PARAMETER** cuando jobID no existe.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>WinSpool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WinSpool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **SetJobW** (Unicode) y **SetJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ TRABAJO 1**](job-info-1.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ TRABAJO 2**](job-info-2.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ TRABAJO 3**](job-info-3.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ TRABAJO 4**](job-info-4.md)
</dt> </dl>

 

