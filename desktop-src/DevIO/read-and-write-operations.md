---
description: Windows admite operaciones de e/s de archivos sincrónicas y asincrónicas (superpuestas) en recursos de comunicaciones serie.
ms.assetid: cee44596-ad73-4afb-b86a-744b0b46d9d5
title: Operaciones de lectura y escritura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26cc53dbe8c52286fe53c81202ab3828808b1aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153041"
---
# <a name="read-and-write-operations"></a>Operaciones de lectura y escritura

Windows admite operaciones de e/s de archivos sincrónicas y asincrónicas (superpuestas) en recursos de comunicaciones serie. Las operaciones superpuestas permiten que el subproceso que realiza la llamada realice otras tareas mientras la operación se ejecuta en segundo plano. Un subproceso utiliza la función [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) para leer desde un recurso de comunicaciones y la función [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) o [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) para escribir en un recurso de comunicaciones. **Readfile** y **WriteFile** se pueden realizar de forma sincrónica o asincrónica. **ReadFileEx** y **WriteFileEx** solo se pueden realizar de forma asincrónica.

El comportamiento de estas funciones de lectura y escritura se ve afectado por si la función se ejecuta como una operación superpuesta, si los parámetros de tiempo de espera están asociados al identificador y si los parámetros de control de flujo están asociados al identificador.

Un subproceso también puede escribir en un recurso de comunicaciones mediante la función [**TransmitCommChar**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar) , que transmite un carácter especificado por encima de los datos pendientes en el búfer de salida. Esta función es útil para transmitir un carácter de señal de prioridad alta al sistema receptor. La transmisión del carácter de prioridad alta todavía está sujeta a los tiempos de espera de control de flujo y de escritura, y la operación se realiza sincrónicamente.

Un subproceso puede usar la función [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) para descartar todos los caracteres del búfer de entrada o salida de un dispositivo. **PurgeComm** también puede finalizar las operaciones de lectura o escritura pendientes, incluso si las operaciones no se han completado. Si un subproceso usa **PurgeComm** para vaciar un búfer de salida, los caracteres eliminados no se transmiten. Para vaciar el búfer de salida y asegurarse de que se transmite el contenido, un subproceso puede llamar a la función [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) (una operación sincrónica). Sin embargo, tenga en cuenta que **FlushFileBuffers** está sujeto al control de flujo pero no a los tiempos de espera de escritura, y no se devolverá hasta que se hayan transmitido todas las operaciones de escritura pendientes.

 

 
