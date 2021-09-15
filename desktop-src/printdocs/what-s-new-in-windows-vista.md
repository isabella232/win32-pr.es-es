---
description: Enumera las interfaces de programación de aplicaciones (API) de impresión introducidas en Windows Vista.
ms.assetid: 7a4eb5d7-b37d-4090-aea4-7274daa1e15c
title: Novedades de la impresión en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8648d57f48623e6db0f6311bb07ae24ac15d96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570537"
---
# <a name="whats-new-for-printing-in-windows-vista"></a>Novedades de la impresión en Windows Vista

Enumera las interfaces de programación de aplicaciones (API) de impresión introducidas en Windows Vista.

Las siguientes funciones y enumeraciones se usan para administrar vales de impresión.



| Función                                                               | Descripción                                                                                                                                   | Encabezado    | Biblioteca     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-----------|-------------|
| [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) | Convierte un vale de impresión en una [**estructura DEVMODE.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)                                                                            | Prntvpt.h | Prntvpt.lib |
| [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) | Convierte un [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en un vale de impresión.                                                                                      | Prntvpt.h | Prntvpt.lib |
| [**PTReleaseMemory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)                             | Libera los búferes creados por ciertas funciones de administración de vales de impresión.                                                                        | Prntvpt.h | Prntvpt.lib |
| [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) | Valida y combina dos vales de impresión en un vale de impresión viable.                                                                            | Prntvpt.h | Prntvpt.lib |
| [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)               | Obtiene una cuenta de las funcionalidades de la impresora.                                                                                                | Prntvpt.h | Prntvpt.lib |
| [**PTOpenProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)                               | Abre un proveedor de vales de impresión.                                                                                                                | Prntvpt.h | Prntvpt.lib |
| [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)                           | Abre un proveedor de vales de impresión, incluso si no admite la versión preferida del [esquema de impresión](./print-schema.md). | Prntvpt.h | Prntvpt.lib |
| [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)                             | Cierra un proveedor de vales de impresión.                                                                                                               | Prntvpt.h | Prntvpt.lib |
| [**PTQuerySchemaVersionSupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)     | Obtiene la versión más reciente del [esquema de impresión](./print-schema.md) que admite una impresora especificada.                        | Prntvpt.h | Prntvpt.lib |



 



| Enumeración                                        | Descripción                                                                                                                                                                               | Encabezado    |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) | Permite a los llamadores especificar qué [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) se usa como origen de los valores predeterminados cuando un vale de impresión no especifica toda la configuración que podría estar en **un DEVMODE**. | Prntvpt.h |
| [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope)     | Especifica el ámbito de un vale de impresión.                                                                                                                                                    | Prntvpt.h |



 

Las siguientes funciones se usan para instalar controladores de impresora.



| Función                                                                   | Descripción                                                                                                                                                                 | Encabezado     | Biblioteca      |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**CorePrinterDriverInstalled**](coreprinterdriverinstalled.md)           | Indica si está instalado un controlador de impresora principal con un GUID, una fecha y una versión especificados.                                                                                | Winspool.h | Winspool.lib |
| [**DeletePrinterDriverPackage**](deleteprinterdriverpackage.md)           | Elimina un paquete de controladores de impresora del almacén de controladores.                                                                                                                     | Winspool.h | Winspool.lib |
| [**GetCorePrinterDrivers**](getcoreprinterdrivers.md)                     | Obtiene el GUID, la versión y la fecha de los controladores de impresora principales especificados y la ruta de acceso a sus paquetes.                                                                      | Winspool.h | Winspool.lib |
| [**GetPrinterDriverPackagePath**](getprinterdriverpackagepath.md)         | Obtiene la ruta de acceso al paquete de controladores de impresora especificado en un servidor de impresión.                                                                                                    | Winspool.h | Winspool.lib |
| [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) | Instala un controlador de impresora desde un paquete de controladores en el almacén de controladores del servidor de impresión.                                                                                         | Winspool.h | Winspool.lib |
| [**UploadPrinterDriverPackage**](uploadprinterdriverpackage.md)           | Carga un controlador de impresora en el almacén de controladores de un servidor de impresión para que se pueda instalar con [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md). | Winspool.h | Winspool.lib |



 

Las siguientes funciones, enumeraciones y estructuras se usan para imprimir y administrar impresoras y conexiones de impresoras.



| Función                                               | Descripción                                                                                                                                              | Encabezado     | Biblioteca      |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**AddPrinterConnection2**](addprinterconnection2.md) | Agrega una conexión a la impresora especificada para el usuario actual.                                                                                         | Winspool.h | Winspool.lib |
| [**OpenPrinter2**](openprinter2.md)                   | Recupera un identificador para la impresora o el servidor de impresión especificados u otros tipos de identificadores en el subsistema de impresión, al tiempo que establece algunas de las opciones de impresora. | Winspool.h | Winspool.lib |



 



| Enumeración                                            | Descripción                                                                                       | Encabezado     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------|------------|
| [**MARCAS DE \_ OPCIÓN \_ DE IMPRESORA**](printer-option-flags.md) | Especifica el almacenamiento en caché de un identificador para una impresora abierta con [**OpenPrinter2.**](openprinter2.md) | Winspool.h |



 



| Estructura                                                         | Descripción                                                                            | Encabezado     |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------|
| [**CONTROLADOR DE \_ IMPRESORA \_ PRINCIPAL**](core-printer-driver.md)              | Representa un controlador de impresora del que dependen otros controladores de impresora.              | Winspool.h |
| [**INFORMACIÓN \_ DEL CONTROLADOR \_ 8**](driver-info-8.md)                          | Representa un controlador de impresora.                                                           | Winspool.h |
| [**FORM \_ INFO \_ 2**](form-info-2.md)                              | Representa información sobre un formulario de impresión localizable.                                 | Winspool.h |
| [**INFORMACIÓN \_ DEL \_ TRABAJO 4**](job-info-4.md)                                | Representa un conjunto completo de valores asociados a un trabajo y admite archivos de cola de 64 bits. | Winspool.h |
| [**INFORMACIÓN DE \_ CONEXIÓN \_ DE IMPRESORA \_ 1**](printer-connection-info-1.md) | Representa información sobre una conexión a una impresora.                                | Winspool.h |
| [**OPCIONES DE \_ IMPRESORA**](printer-options.md)                       | Representa las opciones de impresora.                                                            | Winspool.h |
| [**PRINTPROCESSOR \_ CAPS \_ 2**](printprocessor-caps-2.md)          | Representa la información de funcionalidad de la impresora.                                             | Winspool.h |



 

Las siguientes funciones, enumeraciones e interfaces se usan para implementar un nuevo sistema de notificación de impresión asincrónica.



| Función                                                                             | Descripción                                                                                                                                                                                       | Encabezado     | Biblioteca      |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)               | Crea un canal de comunicación entre el componente de impresión hospedado en cola, como un controlador de impresión o un monitor de puerto, y una aplicación que necesita recibir notificaciones del componente. | Prnasnot.h | Winspool.lib |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)     | Registra una aplicación para recibir notificaciones de componentes hospedados en cola, como controladores de impresora, procesadores de impresión y monitores de puerto.                                                    | Prnasnot.h | Winspool.lib |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications) | Permite que una aplicación que se ha registrado reciba notificaciones de componentes de impresión hospedados en cola para finalizar su suscripción a las notificaciones.                                         | Prnasnot.h | Winspool.lib |



 



| Enumeración                                                                    | Descripción                                                                                                                                                                                                          | Encabezado     |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| [**PrintAsyncNotifyConversationStyle**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle) | Especifica si la comunicación entre las aplicaciones y los componentes hospedados en print Spooler, como los controladores de impresora, los procesadores de impresión y los monitores de puerto, es bidireccional o unidireccional.                          | Prnasnot.h |
| [**PrintAsyncNotifyError**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)                         | Especifica un error en una transacción de notificación asincrónica.                                                                                                                                                      | Prnasnot.h |
| [**PrintAsyncNotifyUserFilter**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)               | Especifica si las notificaciones solo irán a las aplicaciones de escucha asociadas al mismo usuario que el remitente hospedado en Print Spooler o si irán a un conjunto más amplio de aplicaciones de escucha. | Prnasnot.h |



 



| Interfaz y método                                                                                                      | Descripción                                                                                                                                                   | Encabezado     | Biblioteca      |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**IPrintAsyncNotifyCallback::ChannelClosed**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-channelclosed)    | Lo usa un miembro de un canal de comunicación para informar al otro miembro de que el canal se está cierrando.                                                    | Prnasnot.h | Winspool.lib |
| [**IPrintAsyncNotifyCallback::OnEventNotify**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-oneventnotify)    | Llamado por el colador de impresión para alertar a un agente de escucha de que hay una notificación disponible en un canal especificado.                                                      | Prnasnot.h | Winspool.lib |
| [**IPrintAsyncNotifyChannel::CloseChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-closechannel)         | Cierra un canal de comunicación.                                                                                                                               | Prnasnot.h | Winspool.lib |
| [**IPrintAsyncNotifyChannel::SendNotification**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-sendnotification) | Envía una notificación desde un componente hospedado en Print Spooler a una o varias aplicaciones de escucha o envía una respuesta de una aplicación a un componente. | Prnasnot.h | Winspool.lib |
| [**IPrintAsyncNotifyDataObject::AcquireData**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-acquiredata)  | Señala las aplicaciones de escucha a los datos de notificación, así como el tamaño y el tipo de los datos.                                                                   | Prnasnot.h | Winspool.lib |
| [**IPrintAsyncNotifyDataObject::ReleaseData**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-releasedata)  | Libera la memoria utilizada por los datos encapsulados en [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject).                                  | Prnasnot.h | Winspool.lib |



 

La enumeración y las estructuras siguientes se usan para invocar el Convertidor de documentos xps de Microsoft (MXDC), que escribe documentos XML Paper Specification (XPS) en un dispositivo o archivo.



| Enumeración                                | Descripción                                                            | Encabezado |
|--------------------------------------------|------------------------------------------------------------------------|--------|
| [**MxdcS0PageEnums**](mxdcs0pageenums.md) | Especifica tipos de recursos, como fuentes o imágenes, en una página XPS. | Mxdc.h |



 



| Estructura                                                          | Descripción                                                                                                                                    | Encabezado |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| [**MxdcEscapeHeader**](mxdcescapeheader.md)                       | Representa una instrucción para el MXDC.                                                                                                         | Mxdc.h |
| [**MxdcGetFileNameData**](mxdcgetfilenamedata.md)                 | Representa la ruta de acceso completa y el nombre de un archivo de salida MXDC.                                                                                     | Mxdc.h |
| [**MxdcPrintTicketEscape**](mxdcprintticketescape.md)             | Representa una combinación de [**MxdcEscapeHeader**](mxdcescapeheader.md) y [**MxdcPrintTicketPassthrough.**](mxdcprintticketpassthrough.md) | Mxdc.h |
| [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md)   | Representa un vale de impresión que se asociará a un documento XPS.                                                                        | Mxdc.h |
| [**MxdcS0PageData**](mxdcs0pagedata.md)                           | Representa una página con formato XPS que se pasará al archivo de salida MXDC sin ningún procesamiento.                                                  | Mxdc.h |
| [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) | Representa una combinación de [**MxdcEscapeHeader**](mxdcescapeheader.md) y [**MxdcS0PageData.**](mxdcs0pagedata.md)                         | Mxdc.h |
| [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md)       | Representa una combinación de [**MxdcEscapeHeader**](mxdcescapeheader.md) y [**MxdcS0PageResource.**](mxdcs0pageresourceescape.md)           | Mxdc.h |
| [**MxdcS0PageResource**](mxdcs0pageresourceescape.md)             | Representa un recurso, como una fuente o una imagen, que el MXDC incluye en una página XPS.                                                   | Mxdc.h |



 

 

 
