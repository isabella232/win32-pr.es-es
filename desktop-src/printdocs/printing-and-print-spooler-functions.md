---
description: Print Spooler API contiene las funciones y estructuras de datos que las aplicaciones usan para administrar el colador de impresión de Windows y las impresoras y los trabajos de impresión que controla.
ms.assetid: d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39
title: Funciones de la API del administrador de trabajos de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cab0a23afcfa95c4acb427437c72758356ee9771182301111f9660455d2081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824895"
---
# <a name="print-spooler-api-functions"></a>Funciones de la API del administrador de trabajos de impresión

Print Spooler API contiene las funciones y estructuras de datos que las aplicaciones usan para administrar el colador de impresión de Windows y las impresoras y los trabajos de impresión que controla.

Las funciones de Print Spooler API se dividen en los siguientes grupos:

-   [Funciones de trabajo de impresión](#print-job-functions)
-   [Funciones de Interfaz de usuario impresora](#printer-user-interface-functions)
-   [Funciones de impresora](#printer-functions)
-   [Funciones de notificación de cambio de impresora](#printer-change-notification-functions)
-   [Funciones de formulario de impresora](#printer-form-functions)
-   [Funciones de cola de impresión](#print-spooler-api-functions)

## <a name="print-job-functions"></a>Funciones de trabajo de impresión

Estas funciones envían trabajos de impresión a una impresora y realiza un seguimiento y controlan los trabajos de impresión en el colador de impresión.



| Función                                                                      | Descripción                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddJob**](addjob.md)<br/>                                           | La [**función AddJob**](/windows/desktop/printdocs/addjob) agrega un trabajo de impresión a la lista de trabajos de impresión que el colador de impresión puede programar. La función recupera el nombre del archivo que puede usar para almacenar el trabajo. <br/>                                      |
| [**ClosePrinter**](closeprinter.md)<br/>                               | La [**función ClosePrinter**](/windows/desktop/printdocs/closeprinter) cierra el objeto de impresora especificado. <br/>                                                                                                                                                      |
| [**DocumentEvent**](documentevent.md)<br/>                             | La [**función DocumentEvent**](/windows/desktop/printdocs/documentevent) es un controlador de eventos para los eventos asociados a la impresión de un documento. <br/>                                                                                                                     |
| [**Documentproperties**](documentproperties.md)<br/>                   | La [**función DocumentProperties**](/windows/desktop/printdocs/documentproperties) recupera o modifica la información de inicialización de la impresora o muestra una hoja de propiedades de configuración de impresora para la impresora especificada. <br/>                                        |
| [**EndDocPrinter**](enddocprinter.md)<br/>                             | La [**función EndDocPrinter**](/windows/desktop/printdocs/enddocprinter) finaliza un trabajo de impresión para la impresora especificada. <br/>                                                                                                                                             |
| [**EndPagePrinter**](endpageprinter.md)<br/>                           | La [**función EndPagePrinter**](/windows/desktop/printdocs/endpageprinter) notifica al administrador de trabajos de impresión que la aplicación está al final de una página de un trabajo de impresión. <br/>                                                                                               |
| [**EnumJobs**](enumjobs.md)<br/>                                       | La [**función EnumJobs**](/windows/desktop/printdocs/enumjobs) recupera información sobre un conjunto especificado de trabajos de impresión para una impresora especificada. <br/>                                                                                                                |
| [**GetJob**](getjob.md)<br/>                                           | La [**función GetJob**](/windows/desktop/printdocs/getjob) recupera información sobre un trabajo de impresión especificado. <br/>                                                                                                                                                    |
| [**OpenPrinter**](openprinter.md)<br/>                                 | La [**función OpenPrinter**](/windows/desktop/printdocs/openprinter) recupera un identificador para la impresora o el servidor de impresión especificados u otros tipos de identificadores del subsistema de impresión. <br/>                                                                               |
| [**OpenPrinter2**](openprinter2.md)<br/>                               | Recupera un identificador para la impresora, el servidor de impresión u otros tipos de identificadores especificados en el subsistema de impresión, al tiempo que establece algunas de las opciones de impresora.<br/>                                                                                      |
| [**ReportJobProcessingProgress**](reportjobprocessingprogress.md)<br/> | Informa al servicio Print Spooler de si un trabajo de impresión XPS está en la fase de representación o en la cola y qué parte del procesamiento está en curso actualmente.<br/>                                                                               |
| [**ScheduleJob**](schedulejob.md)<br/>                                 | La [**función ScheduleJob**](/windows/desktop/printdocs/schedulejob) solicita que el colador de impresión programe un trabajo de impresión especificado para la impresión. <br/>                                                                                                                |
| [**SetJob**](setjob.md)<br/>                                           | La [**función SetJob**](/windows/desktop/printdocs/setjob) pausa, reanuda, cancela o reinicia un trabajo de impresión en una impresora especificada. También puede usar la función **SetJob** para establecer parámetros de trabajo de impresión, como la prioridad del trabajo de impresión y el nombre del documento. <br/> |
| [**StartDocPrinter**](startdocprinter.md)<br/>                         | La [**función StartDocPrinter**](/windows/desktop/printdocs/startdocprinter) notifica al administrador de trabajos de impresión que un documento se va a colar para imprimirlo. <br/>                                                                                                           |
| [**StartPagePrinter**](startpageprinter.md)<br/>                       | La [**función StartPagePrinter**](/windows/desktop/printdocs/startpageprinter) notifica al administrador de trabajos de cola que una página está a punto de imprimirse en la impresora especificada. <br/>                                                                                                 |



 

## <a name="printer-user-interface-functions"></a>Funciones de Interfaz de usuario impresora

Estas funciones muestran una interfaz de usuario que permite al usuario seleccionar o configurar una impresora.



| Función                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedDocumentProperties**](advanceddocumentproperties.md)<br/> | La [**función AdvancedDocumentProperties**](/windows/desktop/printdocs/advanceddocumentproperties) muestra un cuadro de diálogo de configuración de impresora para la impresora especificada, lo que permite al usuario configurar esa impresora. <br/>                                                                                                                                                      |
| [**ConfigurePort**](configureport.md)<br/>                           | La [**función ConfigurePort**](/windows/desktop/printdocs/configureport) muestra el cuadro de diálogo port-configuration de un puerto en el servidor especificado. <br/>                                                                                                                                                                                                                     |
| [**ConnectToPrinterDlg**](connecttoprinterdlg.md)<br/>               | La [**función ConnectToPrinterDlg**](/windows/desktop/printdocs/connecttoprinterdlg) muestra un cuadro de diálogo que permite a los usuarios examinar impresoras de una red y conectarse a estas. Si el usuario selecciona una impresora, la función intenta crear una conexión a ella. Si no hay un controlador adecuado instalado en el servidor, el usuario tiene la opción de crear una impresora localmente. <br/> |
| [**PrinterProperties**](printerproperties.md)<br/>                   | La [**función PrinterProperties**](/windows/desktop/printdocs/printerproperties) muestra una hoja de propiedades de propiedades de impresora para la impresora especificada. <br/>                                                                                                                                                                                                                    |



 

## <a name="printer-functions"></a>Funciones de impresora

Estas funciones agregan y configuran las impresoras que usa el colador de impresión.



| Función                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPrinter**](abortprinter.md)<br/>                       | La [**función AbortPrinter**](/windows/desktop/printdocs/abortprinter) elimina el archivo de cola de una impresora si la impresora está configurada para la cola. <br/>                                                                                                                                                                                                                                                                  |
| [**Addprinter**](addprinter.md)<br/>                           | La [**función AddPrinter**](/windows/desktop/printdocs/addprinter) agrega una impresora a la lista de impresoras admitidas para un servidor especificado. <br/>                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection**](addprinterconnection.md)<br/>       | La **función AddPrinterConnection** agrega una conexión a la impresora especificada para el usuario actual. <br/>                                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection2**](addprinterconnection2.md)<br/>     | Agrega una conexión a la impresora especificada para el usuario actual y especifica los detalles de conexión.<br/>                                                                                                                                                                                                                                                                                             |
| [**DeletePrinter**](deleteprinter.md)<br/>                     | La [**función DeletePrinter**](/windows/desktop/printdocs/deleteprinter) elimina el objeto de impresora especificado. <br/>                                                                                                                                                                                                                                                                                                    |
| [**DeletePrinterConnection**](deleteprinterconnection.md)<br/> | La [**función DeletePrinterConnection**](/windows/desktop/printdocs/deleteprinterconnection) elimina una conexión a una impresora establecida por una llamada a [**AddPrinterConnection**](addprinterconnection.md) o [**ConnectToPrinterDlg.**](connecttoprinterdlg.md) <br/>                                                                                                                                      |
| [**DeletePrinterData**](deleteprinterdata.md)<br/>             | La [**función DeletePrinterData**](/windows/desktop/printdocs/deleteprinterdata) elimina los datos de configuración especificados para una impresora. Los datos de configuración de una impresora constan de un conjunto de valores con nombre y con tipo. La **función DeletePrinterData** elimina uno de estos valores, especificados por su nombre de valor. <br/>                                                                                                     |
| [**DeletePrinterDataEx**](deleteprinterdataex.md)<br/>         | La [**función DeletePrinterDataEx**](/windows/desktop/printdocs/deleteprinterdataex) elimina un valor especificado de los datos de configuración de una impresora. Los datos de configuración de una impresora constan de un conjunto de valores con nombre y con tipo almacenados en una jerarquía de claves del Registro. La función elimina un valor especificado bajo una clave especificada. <br/>                                                                        |
| [**DeletePrinterKey**](deleteprinterkey.md)<br/>               | La [**función DeletePrinterKey**](/windows/desktop/printdocs/deleteprinterkey) elimina una clave especificada y todas sus subclaves para una impresora especificada. <br/>                                                                                                                                                                                                                                                               |
| [**EnumPrinterData**](enumprinterdata.md)<br/>                 | La [**función EnumPrinterData**](/windows/desktop/printdocs/enumprinterdata) enumera los datos de configuración de una impresora especificada. <br/>                                                                                                                                                                                                                                                                               |
| [**EnumPrinterDataEx**](enumprinterdataex.md)<br/>             | La [**función EnumPrinterDataEx**](/windows/desktop/printdocs/enumprinterdataex) enumera todos los nombres de valor y los datos de una impresora y clave especificadas. <br/>                                                                                                                                                                                                                                                             |
| [**EnumPrinterKey**](enumprinterkey.md)<br/>                   | La [**función EnumPrinterKey**](/windows/desktop/printdocs/enumprinterkey) enumera las subclaves de una clave especificada para una impresora especificada. <br/>                                                                                                                                                                                                                                                                     |
| [**EnumPrinters**](enumprinters.md)<br/>                       | La [**función EnumPrinters**](/windows/desktop/printdocs/enumprinters) enumera las impresoras, servidores de impresión, dominios o proveedores de impresión disponibles. <br/>                                                                                                                                                                                                                                                                 |
| [**FlushPrinter**](flushprinter.md)<br/>                       | La [**función FlushPrinter**](/windows/desktop/printdocs/flushprinter) envía un búfer a la impresora para borrarlo de un estado transitorio. <br/>                                                                                                                                                                                                                                                                 |
| [**GetDefaultPrinter**](getdefaultprinter.md)<br/>             | La [**función GetDefaultPrinter**](/windows/desktop/printdocs/getdefaultprinter) recupera el nombre de la impresora predeterminada para el usuario actual en el equipo local. <br/>                                                                                                                                                                                                                                    |
| [**GetPrinter**](getprinter.md)<br/>                           | La [**función GetPrinter**](/windows/desktop/printdocs/getprinter) recupera información sobre una impresora especificada. <br/>                                                                                                                                                                                                                                                                                               |
| [**GetPrinterData**](getprinterdata.md)<br/>                   | La [**función GetPrinterData**](/windows/desktop/printdocs/getprinterdata) recupera los datos de configuración de la impresora o el servidor de impresión especificados. <br/>                                                                                                                                                                                                                                                                |
| [**GetPrinterDataEx**](getprinterdataex.md)<br/>               | La [**función GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) recupera los datos de configuración de la impresora o el servidor de impresión especificados. **GetPrinterDataEx puede** recuperar los valores almacenados por la [**función SetPrinterData.**](setprinterdata.md) Además, **GetPrinterDataEx puede** recuperar valores almacenados bajo una clave especificada por la [**función SetPrinterDataEx.**](setprinterdataex.md) <br/> |
| [**IsValidDevmode**](isvaliddevmode.md)<br/>                   | La [**función IsValidDevmode**](isvaliddevmode.md) comprueba que el contenido de una estructura DEVMODE es válido. <br/>                                                                                                                                                                                                                                                                           |
| [**ReadPrinter**](readprinter.md)<br/>                         | La [**función ReadPrinter**](/windows/desktop/printdocs/readprinter) recupera datos de la impresora especificada. <br/>                                                                                                                                                                                                                                                                                                   |
| [**ResetPrinter**](resetprinter.md)<br/>                       | La [**función ResetPrinter**](/windows/desktop/printdocs/resetprinter) especifica el tipo de datos y los valores de modo de dispositivo que se usarán para imprimir documentos enviados por la [**función StartDocPrinter.**](startdocprinter.md) Estos valores se pueden invalidar mediante la función [**SetJob**](setjob.md) después de que se haya iniciado la impresión de documentos. <br/>                                                                  |
| [**SetDefaultPrinter**](setdefaultprinter.md)<br/>             | La [**función SetDefaultPrinter**](/windows/desktop/printdocs/setdefaultprinter) establece el nombre de impresora de la impresora predeterminada para el usuario actual en el equipo local. <br/>                                                                                                                                                                                                                                         |
| [**SetPort**](setport.md)<br/>                                 | La [**función SetPort**](/windows/desktop/printdocs/setport) establece el estado asociado a un puerto de impresora. <br/>                                                                                                                                                                                                                                                                                                      |
| [**SetPrinter**](setprinter.md)<br/>                           | La [**función SetPrinter**](/windows/desktop/printdocs/setprinter) establece los datos de una impresora especificada o establece el estado de la impresora especificada al pausar la impresión, reanudar la impresión o borrar todos los trabajos de impresión. <br/>                                                                                                                                                                                           |
| [**SetPrinterData**](setprinterdata.md)<br/>                   | La [**función SetPrinterData**](/windows/desktop/printdocs/setprinterdata) establece los datos de configuración de una impresora o un servidor de impresión. <br/>                                                                                                                                                                                                                                                                             |
| [**SetPrinterDataEx**](setprinterdataex.md)<br/>               | La [**función SetPrinterDataEx**](/windows/desktop/printdocs/setprinterdataex) establece los datos de configuración de una impresora o un servidor de impresión. La función almacena los datos de configuración en la clave del Registro de la impresora. <br/>                                                                                                                                                                                            |
| [**WritePrinter**](writeprinter.md)<br/>                       | La [**función WritePrinter**](writeprinter.md) notifica al administrador de trabajos de impresión que los datos se deben escribir en la impresora especificada. <br/>                                                                                                                                                                                                                                                           |



 

## <a name="printer-change-notification-functions"></a>Funciones de notificación de cambios de impresora

Estas funciones permiten notificar a una aplicación los cambios en el estado de una impresora.



| Función                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)<br/> | La [**función FindClosePrinterChangeNotification**](/windows/desktop/printdocs/findcloseprinterchangenotification) cierra un objeto de notificación de cambios creado mediante una llamada a la [**función FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md) Ese objeto ya no supervisará la impresora o el servidor de impresión asociados al objeto de notificación de cambios. <br/> |
| [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)<br/> | La [**función FindFirstPrinterChangeNotification**](/windows/desktop/printdocs/findfirstprinterchangenotification) crea un objeto de notificación de cambios y devuelve un identificador al objeto . A continuación, puede usar este identificador en una llamada a una de las funciones de espera para supervisar los cambios en la impresora o el servidor de impresión. <br/>                                                                              |
| [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)<br/>   | La [**función FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) recupera información sobre la notificación de cambios más reciente para un objeto de notificación de cambios asociado a una impresora o servidor de impresión. Llame a esta función cuando se cumple una operación de espera en el objeto de notificación de cambios. <br/>                                           |
| [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md)<br/>                           | La [**función FreePrinterNotifyInfo**](/windows/desktop/printdocs/freeprinternotifyinfo) libera un búfer asignado por el sistema creado por la función [**FindNextPrinterChangeNotification.**](findnextprinterchangenotification.md) <br/>                                                                                                                                                                |



 

## <a name="printer-form-functions"></a>Funciones de formulario de impresora

Estas funciones administran los formularios utilizados por una impresora.



| Función                                    | Descripción                                                                                                                                    |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddForm**](addform.md)<br/>       | La [**función AddForm**](/windows/desktop/printdocs/addform) agrega un formulario a la lista de formularios disponibles que se pueden seleccionar para la impresora especificada. <br/> |
| [**DeleteForm**](deleteform.md)<br/> | La [**función DeleteForm**](/windows/desktop/printdocs/deleteform) quita un nombre de formulario de la lista de formularios admitidos. <br/>                                |
| [**EnumForms**](enumforms.md)<br/>   | La [**función EnumForms**](/windows/desktop/printdocs/enumforms) enumera los formularios admitidos por la impresora especificada. <br/>                               |
| [**GetForm**](getform.md)<br/>       | La [**función GetForm**](/windows/desktop/printdocs/getform) recupera información sobre un formulario especificado. <br/>                                              |
| [**SetForm**](setform.md)<br/>       | La [**función SetForm**](/windows/desktop/printdocs/setform) establece la información del formulario para la impresora especificada. <br/>                                       |



 

## <a name="print-spooler-functions"></a>Funciones del colador de impresión

Estas funciones interactúan con el colador de impresión en un nivel bajo.



| Función                                                          | Descripción                                                                                                                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseSpoolFileHandle**](closespoolfilehandle.md)<br/>   | La [**función CloseSpoolFileHandle**](/windows/desktop/printdocs/closespoolfilehandle) cierra un identificador a un archivo de cola asociado al trabajo de impresión enviado actualmente por la aplicación. <br/>                    |
| [**CommitSpoolData**](commitspooldata.md)<br/>             | La [**función CommitSpoolData**](/windows/desktop/printdocs/commitspooldata) notifica al administrador de trabajos de impresión que una cantidad especificada de datos se ha escrito en un archivo de cola especificado y está lista para representarse. <br/> |
| [**GetPrintExecutionData**](getprintexecutiondata.md)<br/> | [**GetPrintExecutionData recupera**](getprintexecutiondata.md) el contexto de impresión actual.<br/>                                                                                             |
| [**GetSpoolFileHandle**](getspoolfilehandle.md)<br/>       | La [**función GetSpoolFileHandle**](/windows/desktop/printdocs/getspoolfilehandle) recupera un identificador para el archivo spool asociado al trabajo enviado actualmente por la aplicación. <br/>                        |



 

 

