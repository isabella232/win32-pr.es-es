---
description: La función SetJob pausa, reanuda, cancela o reinicia un trabajo de impresión en una impresora especificada. También puede usar la función SetJob para establecer los parámetros del trabajo de impresión, como la prioridad del trabajo de impresión y el nombre del documento.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: Función SetJob (WinSpool. h)
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
ms.openlocfilehash: 34dfc8c0239a10d7e7f036beed457d57329f4c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687966"
---
# <a name="setjob-function"></a>SetJob función)

La función **SetJob** pausa, reanuda, cancela o reinicia un trabajo de impresión en una impresora especificada. También puede usar la función **SetJob** para establecer los parámetros del trabajo de impresión, como la prioridad del trabajo de impresión y el nombre del documento.

Puede usar la función **SetJob** para proporcionar un comando a un trabajo de impresión o para establecer los parámetros de un trabajo de impresión, o para realizar ambas acciones en la misma llamada. El valor del parámetro *Command* no afecta al modo en que la función utiliza los parámetros *LEVEL* y *pJob* . Además, puede usar **SetJob** con la [**información de trabajo \_ \_ 3**](job-info-3.md) para vincular un conjunto de trabajos de impresión. Vea Comentarios para obtener más información.

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

*hPrinter* \[ de\]
</dt> <dd>

Identificador del objeto de impresora de interés. Use la función [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*JobID* \[ de\]
</dt> <dd>

Identificador que especifica el trabajo de impresión. Para obtener un identificador de trabajo de impresión, llame a la función [**AddJob**](addjob.md) o a la función [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .

Si el parámetro *LEVEL* está establecido en 3, el parámetro *JobID* debe coincidir con el miembro **JobID** de la estructura [**Job \_ info \_ 3**](job-info-3.md) indicada por *pJob*

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

El tipo de estructura de información de trabajo al que apunta el parámetro *pJob* .

**Todas las versiones de Windows**: puede establecer el parámetro *LEVEL* en 0, 1 o 2. Al establecer *LEVEL* en 0, *PJob* debe ser **null**. Utilice estos valores cuando no esté configurando ningún parámetro de trabajo de impresión.

También puede establecer el parámetro *LEVEL* en 3.

A partir de **Windows Vista**: también puede establecer el parámetro *LEVEL* en 4.

</dd> <dt>

*pJob* \[ de\]
</dt> <dd>

Puntero a una estructura que establece los parámetros del trabajo de impresión.

**Todas las versiones de Windows**: *pJob* pueden apuntar a una estructura Job [**\_ info \_ 1**](job-info-1.md) o [**Job \_ info \_ 2**](job-info-2.md) .

*pJob* también puede apuntar a una estructura [**Job \_ info \_ 3**](job-info-3.md) . Debe tener **acceso de \_ trabajo \_ administrar** el permiso de acceso para los trabajos especificados por los miembros **JobID** y **NextJobId** de la estructura **Job \_ info \_ 3** .

A partir de **Windows Vista**: *pJob* también puede apuntar a una estructura [**Job \_ info \_ 4**](job-info-4.md) .

Si el parámetro *LEVEL* es 0, *PJob* debe ser **null**.

</dd> <dt>

*Comando* \[ de\]
</dt> <dd>

Operación de trabajo de impresión que se va a realizar. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                            | Significado                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <dt>**\_cancelación de control de trabajo \_**</dt> </dl>                                    | No debe usarse. Para eliminar un trabajo de impresión, use el **control de trabajo \_ \_ eliminar**.<br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <dt>**pausar control de trabajo \_ \_**</dt> </dl>                                       | Pausar el trabajo de impresión.<br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <dt>**reinicio del control de trabajo \_ \_**</dt> </dl>                                 | Reinicie el trabajo de impresión. Un trabajo solo se puede reiniciar si se imprimió.<br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <dt>**\_reanudación de control de trabajo \_**</dt> </dl>                                    | Reanudar un trabajo de impresión en pausa.<br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <dt>**\_eliminación de control de trabajo \_**</dt> </dl>                                    | Elimine el trabajo de impresión.<br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <dt>**\_control \_ de trabajo enviado a la \_ \_ impresora**</dt> </dl>       | Lo usan los monitores de puerto para finalizar el trabajo de impresión.<br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <dt>**\_última página de control de trabajo \_ \_ \_ expulsada**</dt> </dl> | Lo usan los monitores de idioma para finalizar el trabajo de impresión.<br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <dt>**\_conservar control de trabajo \_**</dt> </dl>                                    | **Windows Vista y versiones posteriores**: Mantenga el trabajo en la cola después de imprimirlo.<br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <dt>**\_versión de control de trabajo \_**</dt> </dl>                                 | **Windows Vista y versiones posteriores**: libere el trabajo de impresión.<br/>                     |



 

Puede usar la misma llamada a la función **SetJob** para establecer los parámetros del trabajo de impresión y proporcionar un comando a un trabajo de impresión. Por lo tanto, el *comando* no tiene que ser 0 si está estableciendo parámetros de trabajo de impresión, aunque puede ser.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Puede usar la función **SetJob** para establecer varios parámetros de trabajo de impresión proporcionando un puntero a una estructura de información de trabajo [**\_ \_ 1**](job-info-1.md), [**información de trabajo \_ \_ 2**](job-info-2.md), [**información de trabajo \_ \_ 3**](job-info-3.md)o [**información de trabajo \_ \_ 4**](job-info-4.md) que contenga los datos necesarios.

Para quitar o eliminar todos los trabajos de impresión de una impresora determinada, llame a la función [**SetPrinter**](setprinter.md) con su parámetro de *comando* establecido en **purga de \_ control \_ de impresora**.

Los siguientes miembros de una estructura Job info [**\_ \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)o [**Job \_ info \_ 4**](job-info-4.md) se omiten en una llamada a **SetJob**: **JobID**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **size**, **almeterd**, **Time** y **TotalPages**.

Para cambiar la posición de un trabajo de impresión en la cola de impresión, debe disponer del permiso de acceso de **\_ \_ Administración** de acceso de impresora para una impresora.

Si no desea establecer la posición de un trabajo de impresión en la cola de impresión, debe establecer el miembro **Position** de la estructura Job info [**\_ \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)o [**Job \_ info \_ 4**](job-info-4.md) en la posición del **trabajo \_ \_ sin especificar**.

Use la función **SetJob** con la estructura [**Job \_ info \_ 3**](job-info-3.md) para vincular un conjunto de trabajos de impresión (también conocido como cadena). Esto resulta útil en situaciones en las que un único documento consta de varias partes que se desean representar por separado. Para imprimir los trabajos a, B, C y D en orden, llame a **SetJob** con la [**información de trabajo \_ \_ 4**](job-info-4.md) para vincular a b, b a c y c a D.

Si vincula los trabajos de impresión, tenga en cuenta lo siguiente:

-   Los trabajos se pueden agregar al principio o al final de una cadena.
-   Todos los trabajos de la cadena deben tener el mismo tipo de datos.
-   La cadena debe estar completamente vinculada antes de que comience la cola de impresión; de lo contrario, el administrador de trabajos de impresión puede imprimir y eliminar los trabajos en cola antes de vincularlos todos. Hay dos maneras de evitar que la cadena se imprima prematuramente:

    -   PAUSE el primer trabajo de la cadena hasta que la cadena esté completamente vinculada. El estado en pausa del primer trabajo rige el estado de todos los trabajos de la cadena.
    -   Mantener el primer trabajo incompleto, es decir, no llamar a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) o [**ScheduleJob**](schedulejob.md) para el primer trabajo. Sin embargo, si está habilitada la opción ' imprimir mientras se pone en cola ' (valor predeterminado), este método bloquea el puerto mientras se compila la cadena, lo que también impide la impresión de trabajos no relacionados.

-   La aplicación debe controlar el caso en el que el usuario elimina un trabajo en la cadena antes de que la cadena finalice la impresión. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **un \_ parámetro no válido** cuando no existe un JobID.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>WinSpool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WinSpool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |
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

[**Información de trabajo \_ \_ 1**](job-info-1.md)
</dt> <dt>

[**Información de trabajo \_ \_ 2**](job-info-2.md)
</dt> <dt>

[**Información de trabajo \_ \_ 3**](job-info-3.md)
</dt> <dt>

[**Información del trabajo \_ \_ 4**](job-info-4.md)
</dt> </dl>

 

