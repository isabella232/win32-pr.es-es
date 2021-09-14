---
description: 'Hay dos tipos de sincronización de entrada/salida (E/S): E/S sincrónica y E/S asincrónica. La E/S asincrónica también se conoce como E/S superpuesta.'
ms.assetid: ade51d98-cc9d-4b33-9c52-559a9cb14707
title: E/S sincrónica y asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 071dd2943537dcb6aff67a95cb5e2c3d514f4c1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069830"
---
# <a name="synchronous-and-asynchronous-io"></a>E/S sincrónica y asincrónica

Consulte también [Aplicaciones de ejemplo relacionadas con E/S.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winbase/io)

Hay dos tipos de sincronización de entrada/salida (E/S): E/S sincrónica y E/S asincrónica. La E/S asincrónica también se conoce como E/S superpuesta.

En *la E/S de* archivo sincrónica, un subproceso inicia una operación de E/S y entra inmediatamente en un estado de espera hasta que se completa la solicitud de E/S. Un subproceso que *realiza E/S de archivo asincrónica* envía una solicitud de E/S al kernel mediante una llamada a una función adecuada. Si el kernel acepta la solicitud, el subproceso que realiza la llamada continúa procesando otro trabajo hasta que el kernel indica al subproceso que la operación de E/S se ha completado. A continuación, interrumpe su trabajo actual y procesa los datos de la operación de E/S según sea necesario.

Los dos tipos de sincronización se muestran en la ilustración siguiente.

![E/S sincrónica y asincrónica](images/fig2bedit.png)

En situaciones en las que se espera que una solicitud de E/S lleve una gran cantidad de tiempo, como una actualización o una copia de seguridad de una base de datos grande o un vínculo de comunicaciones lentas, la E/S asincrónica suele ser una buena manera de optimizar la eficacia del procesamiento. Sin embargo, para las operaciones de E/S relativamente rápidas, la sobrecarga de procesamiento de solicitudes de E/S de kernel y señales de kernel puede hacer que la E/S asincrónica sea menos beneficiosa, especialmente si es necesario realizar muchas operaciones de E/S rápidas. En este caso, la E/S sincrónica sería mejor. Los mecanismos y los detalles de implementación de cómo realizar estas tareas varían según el tipo de identificador de dispositivo que se usa y las necesidades concretas de la aplicación. En otras palabras, normalmente hay varias maneras de resolver el problema.

## <a name="synchronous-and-asynchronous-io-considerations"></a>Consideraciones de E/S sincrónicas y asincrónicas

Si se abre un archivo o dispositivo para E/S sincrónica (es decir, no se especifica **FILE \_ FLAG \_ OVERLAPPED),** las llamadas posteriores a funciones como [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) pueden bloquear la ejecución del subproceso de llamada hasta que se produzca uno de los siguientes eventos:

-   La operación de E/S se completa (en este ejemplo, una escritura de datos).
-   Error de E/S. (Por ejemplo, la canalización se cierra desde el otro extremo).
-   Se ha producido un error en la propia llamada (por ejemplo, uno o varios parámetros no son válidos).
-   Otro subproceso del proceso llama a la función [**CancelSynchronousIo**](cancelsynchronousio-func.md) mediante el identificador de subproceso del subproceso bloqueado, que finaliza la E/S de ese subproceso, lo que da error a la operación de E/S.
-   El sistema finaliza el subproceso bloqueado; Por ejemplo, el proceso en sí finaliza o otro subproceso llama a la [**función TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) mediante el identificador del subproceso bloqueado. (Por lo general, esto se considera un último recurso y no es un buen diseño de aplicaciones).

En algunos casos, este retraso puede ser inaceptable para el diseño y el propósito de la aplicación, por lo que los diseñadores de aplicaciones deben considerar el uso de E/S asincrónica con los objetos de sincronización de subprocesos adecuados, como los puertos de finalización [de E/S.](i-o-completion-ports.md) Para obtener más información sobre la sincronización de subprocesos, vea [Acerca de la sincronización.](/windows/desktop/Sync/about-synchronization)

Un proceso abre un archivo para E/S asincrónica en su llamada a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) especificando la marca **FILE FLAG \_ \_ OVERLAPPED** en el *parámetro dwFlagsAndAttributes.* Si **no se especifica FILE FLAG \_ \_ OVERLAPPED,** el archivo se abre para la E/S sincrónica. Cuando se ha abierto el archivo para E/S asincrónica, se pasa un puntero a una estructura [**OVERLAPPED**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) a la llamada a [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile). Al realizar E/S sincrónica, esta estructura no es necesaria en las llamadas a **ReadFile** y **WriteFile.**

> [!Note]  
> Si se abre un archivo o dispositivo para E/S asincrónica, las llamadas posteriores a funciones como [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) que usan ese identificador generalmente se devuelven inmediatamente, pero también pueden comportarse sincrónicamente con respecto a la ejecución bloqueada. Para más información, consulte [https://support.microsoft.com/kb/156932](https://support.microsoft.com/kb/156932).

 

Aunque [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) es la función más común que se usa para abrir archivos, volúmenes de disco,  canalizaciones anónimas y otros dispositivos similares, las operaciones de E/S también se pueden realizar mediante una transmisión de tipos de identificador desde otros objetos del sistema, como un socket creado por el [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) o funciones de [**aceptación.**](/windows/desktop/api/winsock2/nf-winsock2-accept)

Los identificadores de los objetos de directorio se obtienen llamando a la [**función CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con el **atributo FILE FLAG BACKUP \_ \_ \_ SEMANTICS.** Los identificadores de directorio casi nunca se usan: las aplicaciones de copia de seguridad son una de las pocas aplicaciones que normalmente los usarán.

Después de abrir el objeto de archivo para E/S asincrónica, se debe crear, inicializar y pasar correctamente una estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) a cada llamada a funciones como [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) y [**WriteFile.**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) Tenga en cuenta lo siguiente al usar la [**estructura OVERLAPPED**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) en operaciones asincrónicas de lectura y escritura:

-   No desasigne ni modifique la estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) ni el búfer de datos hasta que se hayan completado todas las operaciones de E/S asincrónicas en el objeto de archivo.
-   Si declara el puntero a la estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) como una variable local, no salga de la función local hasta que se hayan completado todas las operaciones de E/S asincrónicas en el objeto de archivo. Si la función local se cierra prematuramente, la estructura **OVERLAPPED** sale del ámbito y no será accesible para las funciones [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) que encuentre fuera de esa función.

También puede crear un evento y colocar el identificador en la [**estructura OVERLAPPED;**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Las [funciones de](/windows/desktop/Sync/wait-functions) espera se pueden usar para esperar a que se complete la operación de E/S esperando al identificador de evento.

Como se indicó anteriormente, al trabajar con un identificador asincrónico, las aplicaciones deben tener cuidado al tomar determinaciones sobre cuándo liberar recursos asociados a una operación de E/S especificada en ese identificador. Si el identificador se desasigna prematuramente, [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) pueden informar incorrectamente de que la operación de E/S se ha completado. Además, la **función WriteFile** devolverá a veces **TRUE** con un valor [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) de **ERROR \_ SUCCESS,** aunque use un identificador asincrónico (que también puede devolver **FALSE** con ERROR **IO \_ \_ PENDING**). Los programadores acostumbrados al diseño sincrónico de E/S normalmente liberarán recursos de búfer de datos en este momento porque **TRUE** y **ERROR \_ SUCCESS** significan que la operación se ha completado. Sin embargo, si se usan puertos de finalización de [E/S](i-o-completion-ports.md) con este identificador asincrónico, también se enviará un paquete de finalización aunque la operación de E/S se complete inmediatamente. En otras palabras, si la aplicación libera recursos después de que **WriteFile** devuelva **TRUE** con **ERROR \_ SUCCESS,** además de en la rutina de puerto de finalización de E/S, tendrá una condición de error sin doble uso. En este ejemplo, la recomendación sería permitir que la rutina de puerto de finalización sea la única responsable de todas las operaciones de liberar dichos recursos.

El sistema no mantiene el puntero de archivo en identificadores asincrónicos a archivos y dispositivos que admiten punteros de archivo (es decir, buscar dispositivos), por lo que la posición del archivo debe pasarse a las funciones de lectura y escritura en los miembros de datos de desplazamiento relacionados de la [**estructura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Para obtener más información, [**vea WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) y [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile).

El sistema mantiene la posición del puntero de archivo para un identificador sincrónico a medida que se leen o escriben datos y también se pueden actualizar mediante la función [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) o [**SetFilePointerEx.**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointerex)

Una aplicación también puede esperar en el identificador de archivo para sincronizar la finalización de una operación de E/S, pero hacerlo requiere una precaución extrema. Cada vez que se inicia una operación de E/S, el sistema operativo establece el identificador de archivo en el estado no firmado. Cada vez que se completa una operación de E/S, el sistema operativo establece el identificador de archivo en el estado señalado. Por lo tanto, si una aplicación inicia dos operaciones de E/S y espera en el identificador de archivo, no hay ninguna manera de determinar qué operación finaliza cuando el identificador está establecido en el estado señalado. Si una aplicación debe realizar varias operaciones asincrónicas de E/S en un solo archivo, debe esperar en el identificador de evento en la estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) específica para cada operación de E/S, en lugar de en el identificador de archivo común.

Para cancelar todas las operaciones de E/S asincrónicas pendientes, use:

-   [**CancelIo**](cancelio.md): esta función solo cancela las operaciones emitidas por el subproceso de llamada para el identificador de archivo especificado.
-   [**CancelIoEx:**](cancelioex-func.md)esta función cancela todas las operaciones emitidas por los subprocesos para el identificador de archivo especificado.

Use [**CancelSynchronousIo para cancelar**](cancelsynchronousio-func.md) las operaciones de E/S sincrónicas pendientes.

Las [**funciones ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) permiten a una aplicación especificar una rutina para ejecutar (vea [**FileIOCompletionRoutine)**](/windows/win32/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine)cuando se completa la solicitud de E/S asincrónica.

 

 
