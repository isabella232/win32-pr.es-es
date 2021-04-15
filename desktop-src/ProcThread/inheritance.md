---
description: Un proceso secundario puede heredar varias propiedades y recursos de su proceso primario.
ms.assetid: c530e723-2d40-4022-a259-dfc650604e44
title: Herencia (procesos y subprocesos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713fe398360b510fab3c66f5cf74dc07b642dac
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "105676521"
---
# <a name="inheritance"></a>Herencia

Un proceso secundario puede heredar varias propiedades y recursos de su proceso primario. También puede impedir que un proceso secundario herede propiedades de su proceso primario. Se puede heredar lo siguiente:

-   Abrir los identificadores devueltos por la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . Esto incluye los identificadores de los archivos, los búferes de entrada de la consola, los búferes de pantalla, las canalizaciones con nombre, los dispositivos de comunicación en serie y los buzones.
-   Abrir los identificadores de proceso, subproceso, exclusión mutua, evento, semáforo, canalización con nombre, canalización anónima y objetos de asignación de archivos. Los devuelven las funciones [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa), [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**createsemaphore (**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), [**CreateNamedPipe**](/windows/desktop/api/winbase/nf-winbase-createnamedpipea), [**CreatePipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe)y [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) , respectivamente.
-   Variables de entorno.
-   El directorio actual.
-   La consola, a menos que se desasocie el proceso o se cree una nueva consola. Un proceso de consola secundaria también puede heredar los identificadores estándar del elemento primario, así como el acceso al búfer de entrada y al búfer de pantalla activo.
-   El modo de error, según lo establecido por la función [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) .
-   Máscara de afinidad del procesador.
-   Asociación con un trabajo.

El proceso secundario no hereda lo siguiente:

-   Clase de prioridad.
-   Identificadores devueltos por [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**HeapCreate**](/windows/desktop/api/heapapi/nf-heapapi-heapcreate)y [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc).
-   Pseudo manipuladores, como en los identificadores devueltos por la función [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) o [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) . Estos identificadores solo son válidos para el proceso de llamada.
-   Identificadores de módulo DLL devueltos por la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) .
-   GDI o identificadores de usuario, como **hBitmap** o **HMENU**.

## <a name="inheriting-handles"></a>Herencia de identificadores

Un proceso secundario puede heredar algunos de sus identificadores principales, pero no heredar otros. Para hacer que un identificador se herede, debe hacer dos cosas:

-   Especifique que el identificador se va a heredar al crear, abrir o duplicar el identificador. Las funciones de creación suelen usar el miembro **bInheritHandle** de una estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) para este propósito. [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) usa el parámetro *bInheritHandles* .
-   Especifique que se hereden los identificadores heredables estableciendo el parámetro *bInheritHandles* en true al llamar a la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Además, para heredar los identificadores de entrada estándar, salida estándar y error estándar, el miembro **dwFlags** de la estructura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) debe incluir STARTF \_ USESTDHANDLES.

Para especificar una lista de los identificadores que debe heredar un proceso secundario concreto, llame a la función [**UpdateProcThreadAttribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) con la marca *PROC_THREAD_ATTRIBUTE_HANDLE_LIST* .

Un identificador heredado hace referencia al mismo objeto en el proceso secundario que en el proceso primario. También tiene el mismo valor y privilegios de acceso. Por lo tanto, cuando un proceso cambia el estado del objeto, el cambio afecta a ambos procesos. Para usar un identificador, el proceso secundario debe recuperar el valor del identificador y "conocer" el objeto al que hace referencia. Normalmente, el proceso primario comunica esta información al proceso secundario a través de la línea de comandos, el bloque de entorno o algún tipo de [comunicación entre procesos](/windows/desktop/ipc/interprocess-communications).

Utilice la función [**SetHandleInformation**](/windows/win32/api/handleapi/nf-handleapi-sethandleinformation) para controlar si un identificador existente es heredable o no.

## <a name="inheriting-environment-variables"></a>Heredar variables de entorno

De forma predeterminada, un proceso secundario hereda las variables de entorno del proceso primario. Sin embargo, [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) permite al proceso primario especificar un bloque diferente de variables de entorno. Para obtener más información, consulte [variables de entorno](environment-variables.md).

## <a name="inheriting-the-current-directory"></a>Heredar el directorio actual

La función [**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) recupera el directorio actual del proceso que realiza la llamada. De forma predeterminada, un proceso secundario hereda el directorio actual de su proceso primario. Sin embargo, [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) permite al proceso primario especificar un directorio actual diferente para el proceso secundario. Para cambiar el directorio actual del proceso de llamada, use la función [**SetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) .
