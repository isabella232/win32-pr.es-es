---
description: La API del administrador de trabajos de impresión contiene las funciones y estructuras de datos que usan las aplicaciones para administrar el administrador de trabajos de impresión de Windows y las impresoras y los trabajos de impresión que controla.
ms.assetid: d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39
title: Funciones de la API del administrador de trabajos de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df751b11206ebf26d2d0e8fd88f61ede8447dad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278911"
---
# <a name="print-spooler-api-functions"></a>Funciones de la API del administrador de trabajos de impresión

La API del administrador de trabajos de impresión contiene las funciones y estructuras de datos que usan las aplicaciones para administrar el administrador de trabajos de impresión de Windows y las impresoras y los trabajos de impresión que controla.

Las funciones de la API del administrador de trabajos de impresión se dividen en los siguientes grupos:

-   [Funciones de trabajo de impresión](#print-job-functions)
-   [Funciones de la interfaz de usuario de impresora](#printer-user-interface-functions)
-   [Funciones de impresora](#printer-functions)
-   [Funciones de notificación de cambio de impresora](#printer-change-notification-functions)
-   [Funciones de formulario de impresora](#printer-form-functions)
-   [Funciones del administrador de trabajos de impresión](#print-spooler-api-functions)

## <a name="print-job-functions"></a>Funciones de trabajo de impresión

Estas funciones envían trabajos de impresión a una impresora y realizan un seguimiento de los trabajos de impresión y los controlan en el administrador de trabajos de impresión.



| Función                                                                      | Descripción                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddJob**](addjob.md)<br/>                                           | La función [**AddJob**](/windows/desktop/printdocs/addjob) agrega un trabajo de impresión a la lista de trabajos de impresión que puede programar el administrador de trabajos de impresión. La función recupera el nombre del archivo que puede usar para almacenar el trabajo. <br/>                                      |
| [**ClosePrinter**](closeprinter.md)<br/>                               | La función [**ClosePrinter**](/windows/desktop/printdocs/closeprinter) cierra el objeto de impresora especificado. <br/>                                                                                                                                                      |
| [**DocumentEvent**](documentevent.md)<br/>                             | La función [**DocumentEvent**](/windows/desktop/printdocs/documentevent) es un controlador de eventos para los eventos asociados a la impresión de un documento. <br/>                                                                                                                     |
| [**DocumentProperties**](documentproperties.md)<br/>                   | La función [**DocumentProperties**](/windows/desktop/printdocs/documentproperties) recupera o modifica la información de inicialización de la impresora o muestra una hoja de propiedades de configuración de impresora para la impresora especificada. <br/>                                        |
| [**EndDocPrinter**](enddocprinter.md)<br/>                             | La función [**EndDocPrinter**](/windows/desktop/printdocs/enddocprinter) finaliza un trabajo de impresión para la impresora especificada. <br/>                                                                                                                                             |
| [**EndPagePrinter**](endpageprinter.md)<br/>                           | La función [**EndPagePrinter**](/windows/desktop/printdocs/endpageprinter) notifica al administrador de trabajos de impresión que la aplicación está al final de una página en un trabajo de impresión. <br/>                                                                                               |
| [**EnumJobs**](enumjobs.md)<br/>                                       | La función [**EnumJobs**](/windows/desktop/printdocs/enumjobs) recupera información acerca de un conjunto especificado de trabajos de impresión para una impresora especificada. <br/>                                                                                                                |
| [**GetJob**](getjob.md)<br/>                                           | La función [**GetJob**](/windows/desktop/printdocs/getjob) recupera información acerca de un trabajo de impresión especificado. <br/>                                                                                                                                                    |
| [**OpenPrinter**](openprinter.md)<br/>                                 | La función [**OpenPrinter**](/windows/desktop/printdocs/openprinter) recupera un identificador de la impresora o del servidor de impresión especificado u otros tipos de controladores en el subsistema de impresión. <br/>                                                                               |
| [**OpenPrinter2**](openprinter2.md)<br/>                               | Recupera un identificador de la impresora, el servidor de impresión u otros tipos de controladores del subsistema de impresión especificados, mientras se establecen algunas de las opciones de la impresora.<br/>                                                                                      |
| [**ReportJobProcessingProgress**](reportjobprocessingprogress.md)<br/> | Notifica al servicio Administrador de trabajos de impresión si un trabajo de impresión XPS está en cola o en la fase de representación y qué parte del procesamiento está en curso actualmente.<br/>                                                                               |
| [**ScheduleJob**](schedulejob.md)<br/>                                 | La función [**ScheduleJob**](/windows/desktop/printdocs/schedulejob) solicita que el administrador de trabajos de impresión programe un trabajo de impresión especificado para imprimirlo. <br/>                                                                                                                |
| [**SetJob**](setjob.md)<br/>                                           | La función [**SetJob**](/windows/desktop/printdocs/setjob) pausa, reanuda, cancela o reinicia un trabajo de impresión en una impresora especificada. También puede usar la función **SetJob** para establecer los parámetros del trabajo de impresión, como la prioridad del trabajo de impresión y el nombre del documento. <br/> |
| [**StartDocPrinter**](startdocprinter.md)<br/>                         | La función [**StartDocPrinter**](/windows/desktop/printdocs/startdocprinter) notifica al administrador de trabajos de impresión que se va a poner en cola un documento para su impresión. <br/>                                                                                                           |
| [**StartPagePrinter**](startpageprinter.md)<br/>                       | La función [**StartPagePrinter**](/windows/desktop/printdocs/startpageprinter) notifica al administrador de trabajos de impresión que se va a imprimir una página en la impresora especificada. <br/>                                                                                                 |



 

## <a name="printer-user-interface-functions"></a>Funciones de la interfaz de usuario de impresora

Estas funciones muestran una interfaz de usuario que permite al usuario seleccionar o configurar una impresora.



| Función                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedDocumentProperties**](advanceddocumentproperties.md)<br/> | La función [**AdvancedDocumentProperties**](/windows/desktop/printdocs/advanceddocumentproperties) muestra un cuadro de diálogo de configuración de impresora para la impresora especificada, lo que permite al usuario configurar esa impresora. <br/>                                                                                                                                                      |
| [**ConfigurePort**](configureport.md)<br/>                           | La función [**ConfigurePort**](/windows/desktop/printdocs/configureport) muestra el cuadro de diálogo de configuración de puerto para un puerto en el servidor especificado. <br/>                                                                                                                                                                                                                     |
| [**ConnectToPrinterDlg**](connecttoprinterdlg.md)<br/>               | La función [**ConnectToPrinterDlg**](/windows/desktop/printdocs/connecttoprinterdlg) muestra un cuadro de diálogo que permite a los usuarios examinar y conectarse a las impresoras de una red. Si el usuario selecciona una impresora, la función intenta crear una conexión con ella. Si no hay un controlador adecuado instalado en el servidor, el usuario tiene la opción de crear una impresora localmente. <br/> |
| [**PrinterProperties**](printerproperties.md)<br/>                   | La función [**PrinterProperties**](/windows/desktop/printdocs/printerproperties) muestra una hoja de propiedades de las propiedades de la impresora especificada. <br/>                                                                                                                                                                                                                    |



 

## <a name="printer-functions"></a>Funciones de impresora

Estas funciones agregan y configuran las impresoras que utiliza el administrador de trabajos de impresión.



| Función                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPrinter**](abortprinter.md)<br/>                       | La función [**AbortPrinter**](/windows/desktop/printdocs/abortprinter) elimina el archivo de cola de impresión de una impresora si la impresora está configurada para la puesta en cola. <br/>                                                                                                                                                                                                                                                                  |
| [**AddPrinter (**](addprinter.md)<br/>                           | La función [**AddPrinter (**](/windows/desktop/printdocs/addprinter) agrega una impresora a la lista de impresoras admitidas para un servidor especificado. <br/>                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection**](addprinterconnection.md)<br/>       | La función **AddPrinterConnection** agrega una conexión a la impresora especificada para el usuario actual. <br/>                                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection2**](addprinterconnection2.md)<br/>     | Agrega una conexión a la impresora especificada para el usuario actual y especifica los detalles de conexión.<br/>                                                                                                                                                                                                                                                                                             |
| [**DeletePrinter**](deleteprinter.md)<br/>                     | La función [**DeletePrinter**](/windows/desktop/printdocs/deleteprinter) elimina el objeto de impresora especificado. <br/>                                                                                                                                                                                                                                                                                                    |
| [**DeletePrinterConnection**](deleteprinterconnection.md)<br/> | La función [**DeletePrinterConnection**](/windows/desktop/printdocs/deleteprinterconnection) elimina una conexión a una impresora establecida por una llamada a [**AddPrinterConnection**](addprinterconnection.md) o [**ConnectToPrinterDlg**](connecttoprinterdlg.md). <br/>                                                                                                                                      |
| [**DeletePrinterData**](deleteprinterdata.md)<br/>             | La función [**DeletePrinterData**](/windows/desktop/printdocs/deleteprinterdata) elimina los datos de configuración especificados para una impresora. Los datos de configuración de una impresora se componen de un conjunto de valores con nombre y con tipo. La función **DeletePrinterData** elimina uno de estos valores, especificado por su nombre de valor. <br/>                                                                                                     |
| [**DeletePrinterDataEx**](deleteprinterdataex.md)<br/>         | La función [**DeletePrinterDataEx**](/windows/desktop/printdocs/deleteprinterdataex) elimina un valor especificado de los datos de configuración de una impresora. Los datos de configuración de una impresora se componen de un conjunto de valores con nombre y con tipo que se almacenan en una jerarquía de claves del registro. La función elimina un valor especificado en una clave especificada. <br/>                                                                        |
| [**DeletePrinterKey**](deleteprinterkey.md)<br/>               | La función [**DeletePrinterKey**](/windows/desktop/printdocs/deleteprinterkey) elimina una clave especificada y todas sus subclaves para una impresora especificada. <br/>                                                                                                                                                                                                                                                               |
| [**EnumPrinterData**](enumprinterdata.md)<br/>                 | La función [**EnumPrinterData**](/windows/desktop/printdocs/enumprinterdata) enumera los datos de configuración de una impresora especificada. <br/>                                                                                                                                                                                                                                                                               |
| [**EnumPrinterDataEx**](enumprinterdataex.md)<br/>             | La función [**EnumPrinterDataEx**](/windows/desktop/printdocs/enumprinterdataex) enumera todos los nombres de valor y los datos de una impresora y una clave especificadas. <br/>                                                                                                                                                                                                                                                             |
| [**EnumPrinterKey**](enumprinterkey.md)<br/>                   | La función [**EnumPrinterKey**](/windows/desktop/printdocs/enumprinterkey) enumera las subclaves de una clave especificada para una impresora especificada. <br/>                                                                                                                                                                                                                                                                     |
| [**EnumPrinters**](enumprinters.md)<br/>                       | La función [**EnumPrinters**](/windows/desktop/printdocs/enumprinters) enumera las impresoras, los servidores de impresión, los dominios o los proveedores de impresión disponibles. <br/>                                                                                                                                                                                                                                                                 |
| [**FlushPrinter**](flushprinter.md)<br/>                       | La función [**FlushPrinter**](/windows/desktop/printdocs/flushprinter) envía un búfer a la impresora para borrarlo de un estado transitorio. <br/>                                                                                                                                                                                                                                                                 |
| [**GetDefaultPrinter**](getdefaultprinter.md)<br/>             | La función [**GetDefaultPrinter**](/windows/desktop/printdocs/getdefaultprinter) recupera el nombre de la impresora predeterminada del usuario actual en el equipo local. <br/>                                                                                                                                                                                                                                    |
| [**GetPrinter**](getprinter.md)<br/>                           | La función [**GetPrinter**](/windows/desktop/printdocs/getprinter) recupera información sobre una impresora especificada. <br/>                                                                                                                                                                                                                                                                                               |
| [**GetPrinterData**](getprinterdata.md)<br/>                   | La función [**GetPrinterData**](/windows/desktop/printdocs/getprinterdata) recupera los datos de configuración para la impresora o el servidor de impresión especificado. <br/>                                                                                                                                                                                                                                                                |
| [**GetPrinterDataEx**](getprinterdataex.md)<br/>               | La función [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) recupera los datos de configuración para la impresora o el servidor de impresión especificado. **GetPrinterDataEx** puede recuperar los valores almacenados por la función [**SetPrinterData**](setprinterdata.md) . Además, **GetPrinterDataEx** puede recuperar valores almacenados en una clave especificada mediante la función [**SetPrinterDataEx**](setprinterdataex.md) . <br/> |
| [**IsValidDevmode**](isvaliddevmode.md)<br/>                   | La función [**IsValidDevmode**](isvaliddevmode.md) comprueba que el contenido de una estructura DEVMODE es válido. <br/>                                                                                                                                                                                                                                                                           |
| [**ReadPrinter**](readprinter.md)<br/>                         | La función [**ReadPrinter**](/windows/desktop/printdocs/readprinter) recupera datos de la impresora especificada. <br/>                                                                                                                                                                                                                                                                                                   |
| [**ResetPrinter**](resetprinter.md)<br/>                       | La función [**ResetPrinter**](/windows/desktop/printdocs/resetprinter) especifica el tipo de datos y los valores de modo de dispositivo que se van a usar para imprimir documentos enviados por la función [**StartDocPrinter**](startdocprinter.md) . Estos valores se pueden invalidar mediante la función [**SetJob**](setjob.md) una vez iniciada la impresión del documento. <br/>                                                                  |
| [**SetDefaultPrinter**](setdefaultprinter.md)<br/>             | La función [**SetDefaultPrinter**](/windows/desktop/printdocs/setdefaultprinter) establece el nombre de la impresora predeterminada para el usuario actual en el equipo local. <br/>                                                                                                                                                                                                                                         |
| [**SetPort**](setport.md)<br/>                                 | La función [**SetPort**](/windows/desktop/printdocs/setport) establece el estado asociado a un puerto de impresora. <br/>                                                                                                                                                                                                                                                                                                      |
| [**SetPrinter**](setprinter.md)<br/>                           | La función [**SetPrinter**](/windows/desktop/printdocs/setprinter) establece los datos de una impresora especificada o establece el estado de la impresora especificada mediante la pausa de la impresión, la reanudación de la impresión o la eliminación de todos los trabajos de impresión. <br/>                                                                                                                                                                                           |
| [**SetPrinterData**](setprinterdata.md)<br/>                   | La función [**SetPrinterData**](/windows/desktop/printdocs/setprinterdata) establece los datos de configuración de una impresora o un servidor de impresión. <br/>                                                                                                                                                                                                                                                                             |
| [**SetPrinterDataEx**](setprinterdataex.md)<br/>               | La función [**SetPrinterDataEx**](/windows/desktop/printdocs/setprinterdataex) establece los datos de configuración de una impresora o un servidor de impresión. La función almacena los datos de configuración en la clave del registro de la impresora. <br/>                                                                                                                                                                                            |
| [**WritePrinter**](writeprinter.md)<br/>                       | La función [**WritePrinter**](writeprinter.md) notifica al administrador de trabajos de impresión que los datos se deben escribir en la impresora especificada. <br/>                                                                                                                                                                                                                                                           |



 

## <a name="printer-change-notification-functions"></a>Funciones de notificación de cambio de impresora

Estas funciones permiten a una aplicación recibir notificaciones de los cambios en el estado de una impresora.



| Función                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)<br/> | La función [**FindClosePrinterChangeNotification**](/windows/desktop/printdocs/findcloseprinterchangenotification) cierra un objeto de notificación de cambios creado llamando a la función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . Dicho objeto ya no supervisará la impresora o el servidor de impresión asociado al objeto de notificación de cambios. <br/> |
| [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)<br/> | La función [**FindFirstPrinterChangeNotification**](/windows/desktop/printdocs/findfirstprinterchangenotification) crea un objeto de notificación de cambio y devuelve un identificador al objeto. Después, puede usar este identificador en una llamada a una de las funciones de espera para supervisar los cambios en la impresora o el servidor de impresión. <br/>                                                                              |
| [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)<br/>   | La función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) recupera información sobre la notificación de cambios más reciente para un objeto de notificación de cambios asociado a una impresora o un servidor de impresión. Llame a esta función cuando se satisfaga una operación de espera en el objeto de notificación de cambios. <br/>                                           |
| [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md)<br/>                           | La función [**FreePrinterNotifyInfo**](/windows/desktop/printdocs/freeprinternotifyinfo) libera un búfer asignado por el sistema creado por la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) . <br/>                                                                                                                                                                |



 

## <a name="printer-form-functions"></a>Funciones de formulario de impresora

Estas funciones administran los formularios utilizados por una impresora.



| Función                                    | Descripción                                                                                                                                    |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddForm**](addform.md)<br/>       | La función [**AddForm**](/windows/desktop/printdocs/addform) agrega un formulario a la lista de formularios disponibles que se pueden seleccionar para la impresora especificada. <br/> |
| [**DeleteForm**](deleteform.md)<br/> | La función [**DeleteForm**](/windows/desktop/printdocs/deleteform) quita un nombre de formulario de la lista de formularios admitidos. <br/>                                |
| [**EnumForms**](enumforms.md)<br/>   | La función [**EnumForms**](/windows/desktop/printdocs/enumforms) enumera los formatos admitidos por la impresora especificada. <br/>                               |
| [**GetForm**](getform.md)<br/>       | La función [**GetForm**](/windows/desktop/printdocs/getform) recupera información sobre un formulario especificado. <br/>                                              |
| [**SetForm**](setform.md)<br/>       | La función [**SetForm**](/windows/desktop/printdocs/setform) establece la información del formulario para la impresora especificada. <br/>                                       |



 

## <a name="print-spooler-functions"></a>Funciones del administrador de trabajos de impresión

Estas funciones interactúan con el administrador de trabajos de impresión en un nivel bajo.



| Función                                                          | Descripción                                                                                                                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseSpoolFileHandle**](closespoolfilehandle.md)<br/>   | La función [**CloseSpoolFileHandle**](/windows/desktop/printdocs/closespoolfilehandle) cierra un identificador a un archivo de cola de impresión asociado al trabajo de impresión actualmente enviado por la aplicación. <br/>                    |
| [**CommitSpoolData**](commitspooldata.md)<br/>             | La función [**CommitSpoolData**](/windows/desktop/printdocs/commitspooldata) notifica al administrador de trabajos de impresión que se ha escrito una cantidad de datos especificada en un archivo de cola especificado y está listo para ser representada. <br/> |
| [**GetPrintExecutionData**](getprintexecutiondata.md)<br/> | [**GetPrintExecutionData**](getprintexecutiondata.md) recupera el contexto de impresión actual.<br/>                                                                                             |
| [**GetSpoolFileHandle**](getspoolfilehandle.md)<br/>       | La función [**GetSpoolFileHandle**](/windows/desktop/printdocs/getspoolfilehandle) recupera un identificador para el archivo de cola asociado al trabajo enviado actualmente por la aplicación. <br/>                        |



 

 

