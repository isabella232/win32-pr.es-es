---
description: 'Hay dos tipos de sincronización de entrada/salida (e/s): e/s sincrónica y de e/s asincrónica. La e/s asincrónica también se conoce como e/s superpuesta.'
ms.assetid: ade51d98-cc9d-4b33-9c52-559a9cb14707
title: E/s sincrónica y asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 071dd2943537dcb6aff67a95cb5e2c3d514f4c1a
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105689904"
---
# <a name="synchronous-and-asynchronous-io"></a>E/s sincrónica y asincrónica

Vea también [aplicaciones de ejemplo relacionadas con e/s](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winbase/io).

Hay dos tipos de sincronización de entrada/salida (e/s): e/s sincrónica y de e/s asincrónica. La e/s asincrónica también se conoce como e/s superpuesta.

En la *e/s de archivos sincrónicos*, un subproceso inicia una operación de e/s y entra inmediatamente en un estado de espera hasta que se completa la solicitud de e/s. Un subproceso que realiza la *e/s de archivos asincrónica* envía una solicitud de e/s al kernel mediante una llamada a una función adecuada. Si el kernel acepta la solicitud, el subproceso que realiza la llamada continúa procesando otro trabajo hasta que el kernel señale al subproceso de que se ha completado la operación de e/s. Después, interrumpe su trabajo actual y procesa los datos de la operación de e/s según sea necesario.

Los dos tipos de sincronización se muestran en la ilustración siguiente.

![e/s sincrónica y asincrónica](images/fig2bedit.png)

En situaciones en las que se espera que una solicitud de e/s tome una gran cantidad de tiempo, como una actualización o una copia de seguridad de una base de datos de gran tamaño o un vínculo de comunicaciones lento, la e/s asincrónica suele ser una buena manera de optimizar la eficacia del procesamiento. Sin embargo, para operaciones de e/s relativamente rápidas, la sobrecarga que supone el procesamiento de las solicitudes de e/s de kernel y las señales de kernel puede hacer que la e/s asincrónica sea menos ventajosa, especialmente si es necesario realizar muchas operaciones de e/s rápidas. En este caso, la e/s sincrónica sería mejor. Los mecanismos y los detalles de implementación de cómo realizar estas tareas varían en función del tipo de identificador de dispositivo que se use y de las necesidades concretas de la aplicación. En otras palabras, normalmente hay varias formas de resolver el problema.

## <a name="synchronous-and-asynchronous-io-considerations"></a>Consideraciones de e/s sincrónicas y asincrónicas

Si se abre un archivo o un dispositivo para la e/s sincrónica (es decir, no se especifica la superposición de la **\_ marca \_ de archivo** ), las llamadas subsiguientes a funciones como [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) pueden bloquear la ejecución del subproceso de llamada hasta que se produzca uno de los siguientes eventos:

-   Se completa la operación de e/s (en este ejemplo, una escritura de datos).
-   Error de E/S. (Por ejemplo, la canalización se cierra desde el otro extremo).
-   Se ha producido un error en la propia llamada (por ejemplo, uno o más parámetros no son válidos).
-   Otro subproceso del proceso llama a la función [**CancelSynchronousIo**](cancelsynchronousio-func.md) con el identificador de subproceso del subproceso bloqueado, que finaliza la e/s para ese subproceso, con lo que se produce un error en la operación de e/s.
-   El sistema ha terminado el subproceso bloqueado; por ejemplo, el propio proceso finaliza, u otro subproceso llama a la función [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) mediante el identificador del subproceso bloqueado. (Esto suele considerarse un último recurso y no un buen diseño de la aplicación).

En algunos casos, este retraso puede ser inaceptable para el diseño y el propósito de la aplicación, por lo que los diseñadores de aplicaciones deben considerar el uso de la e/s asincrónica con objetos de sincronización de subprocesos adecuados, como los [puertos de finalización de e/s](i-o-completion-ports.md). Para obtener más información acerca de la sincronización de subprocesos, consulte [acerca de la sincronización](/windows/desktop/Sync/about-synchronization).

Un proceso abre un archivo para la e/s asincrónica en su llamada a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) especificando la marca de superposición de **\_ marca \_ de archivo** en el parámetro *dwFlagsAndAttributes* . Si no se especifica la **marca de archivo \_ \_ OVERLAPPED** , el archivo se abre para la e/s sincrónica. Cuando el archivo se ha abierto para la e/s asincrónica, se pasa un puntero a una estructura [**superpuesta**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) en la llamada a [**readfile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile). Al realizar operaciones de e/s sincrónicas, esta estructura no es necesaria en las llamadas a **readfile** y **WriteFile**.

> [!Note]  
> Si se abre un archivo o un dispositivo para la e/s asincrónica, las llamadas subsiguientes a funciones como [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) con ese identificador normalmente devuelven de inmediato pero también se comportan de forma sincrónica con respecto a la ejecución bloqueada. Para más información, consulte [https://support.microsoft.com/kb/156932](https://support.microsoft.com/kb/156932).

 

Aunque [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) es la función más común que se usa para abrir archivos, volúmenes de disco, canalizaciones anónimas y otros dispositivos similares, las operaciones de e/s también se pueden realizar mediante el uso de una *conversión* de identificador de otros objetos del sistema, como un socket creado por las funciones [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) o [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) .

Los identificadores de los objetos de directorio se obtienen mediante una llamada a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con el atributo de **semántica de copia de \_ \_ seguridad \_ del marcador de archivo** . Casi nunca se usan identificadores de directorio: las aplicaciones de copia de seguridad son una de las pocas aplicaciones que normalmente las usarán.

Después de abrir el objeto de archivo para la e/s asincrónica, una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) se debe crear, inicializar y pasar correctamente en cada llamada a funciones como [**readfile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile). Tenga en cuenta lo siguiente cuando use la estructura [**superpuesta**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) en operaciones asincrónicas de lectura y escritura:

-   No Desasigne ni modifique la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) o el búfer de datos hasta que se hayan completado todas las operaciones de e/s asincrónicas en el objeto de archivo.
-   Si declara el puntero a la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) como una variable local, no salga de la función local hasta que se hayan completado todas las operaciones de e/s asincrónicas en el objeto de archivo. Si la función local se sale prematuramente, la estructura **superpuesta** quedará fuera del ámbito y no será accesible para las funciones [**readfile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) que encuentre fuera de esa función.

También puede crear un evento y colocar el identificador en la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . a continuación, las [funciones de espera](/windows/desktop/Sync/wait-functions) se pueden usar para esperar a que se complete la operación de e/s esperando en el controlador de eventos.

Como se indicó anteriormente, al trabajar con un identificador asincrónico, las aplicaciones deben tener cuidado al realizar determinaciones sobre cuándo liberar recursos asociados a una operación de e/s especificada en ese controlador. Si se cancela la asignación del identificador prematuramente, [**readfile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) pueden informar incorrectamente de que se ha completado la operación de e/s. Además, la función **WriteFile** devolverá a veces **true** con un valor [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) de **error \_ Success**, aunque esté usando un identificador asincrónico (que también puede devolver **false** con el **error de \_ e/s \_ pendiente**). Los programadores acostumbrados al diseño de e/s sincrónica normalmente liberarán recursos de búfer de datos en este momento porque **true** y **error \_ Success** indican que la operación se ha completado. Sin embargo, si se usan [puertos de finalización de e/s](i-o-completion-ports.md) con este identificador asincrónico, también se enviará un paquete de finalización aunque la operación de e/s se complete inmediatamente. En otras palabras, si la aplicación libera recursos después de que **WriteFile** devuelva **true** con el **error \_ Success** , además de en la rutina del puerto de finalización de e/s, tendrá una condición de error de doble liberación. En este ejemplo, la recomendación sería permitir que la rutina del puerto de finalización sea la única responsable de todas las operaciones de liberación de estos recursos.

El sistema no mantiene el puntero de archivo en los identificadores asincrónicos de los archivos y dispositivos que admiten punteros de archivo (es decir, los dispositivos de búsqueda), por lo que la posición del archivo se debe pasar a las funciones de lectura y escritura en los miembros de datos de desplazamiento relacionados de la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . Para obtener más información, vea [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) y [**readfile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile).

El sistema mantiene la posición del puntero de archivo para un identificador sincrónico a medida que se leen o escriben datos y también se pueden actualizar mediante la función [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) o [**SetFilePointerEx**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointerex) .

Una aplicación también puede esperar en el identificador de archivo para sincronizar la finalización de una operación de e/s, pero esto requiere extrema precaución. Cada vez que se inicia una operación de e/s, el sistema operativo establece el identificador de archivo en el estado no señalado. Cada vez que se completa una operación de e/s, el sistema operativo establece el identificador de archivo en el estado señalado. Por lo tanto, si una aplicación inicia dos operaciones de e/s y espera en el identificador de archivo, no hay ninguna manera de determinar qué operación ha finalizado cuando el identificador se establece en el estado señalado. Si una aplicación debe realizar varias operaciones de e/s asincrónicas en un único archivo, debe esperar en el identificador de eventos de la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) específica para cada operación de e/s, en lugar de en el identificador de archivo común.

Para cancelar todas las operaciones de e/s asincrónicas pendientes, use:

-   [**CancelIo**](cancelio.md): esta función solo cancela las operaciones emitidas por el subproceso que realiza la llamada para el identificador de archivo especificado.
-   [**CancelIoEx**](cancelioex-func.md): esta función cancela todas las operaciones emitidas por los subprocesos para el identificador de archivo especificado.

Use [**CancelSynchronousIo**](cancelsynchronousio-func.md) para cancelar las operaciones de e/s sincrónicas pendientes.

Las funciones [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) permiten que una aplicación especifique una rutina que se va a ejecutar (consulte [**FileIOCompletionRoutine**](/windows/win32/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine)) cuando se completa la solicitud de e/s asincrónica.

 

 
