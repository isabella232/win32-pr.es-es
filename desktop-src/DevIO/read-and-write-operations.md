---
description: Windows admite operaciones de E/S de archivos sincrónicas y asincrónicas (superpuestas) en recursos de comunicaciones serie.
ms.assetid: cee44596-ad73-4afb-b86a-744b0b46d9d5
title: Operaciones de lectura y escritura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26cc53dbe8c52286fe53c81202ab3828808b1aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164302"
---
# <a name="read-and-write-operations"></a>Operaciones de lectura y escritura

Windows admite operaciones de E/S de archivos sincrónicas y asincrónicas (superpuestas) en recursos de comunicaciones serie. Las operaciones superpuestas permiten al subproceso que realiza la llamada realizar otras tareas mientras la operación se ejecuta en segundo plano. Un subproceso usa las funciones [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) para leer desde un recurso de comunicaciones, y la función [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) o [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) para escribir en un recurso de comunicaciones. **ReadFile** y **WriteFile** se pueden realizar de forma sincrónica o asincrónica. **ReadFileEx** y **WriteFileEx** solo se pueden realizar de forma asincrónica.

El comportamiento de estas funciones de lectura y escritura se ve afectado por si la función se ejecuta como una operación superpuesta, si los parámetros de tiempo de espera están asociados al identificador y si los parámetros de control de flujo están asociados al identificador.

Un subproceso también puede escribir en un recurso de comunicaciones mediante la función [**TransmitCommChar,**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar) que transmite un carácter especificado delante de los datos pendientes en el búfer de salida. Esta función es útil para transmitir un carácter de señal de alta prioridad al sistema receptor. La transmisión del carácter de prioridad alta sigue sujeta a tiempos de espera de escritura y control de flujo, y la operación se realiza de forma sincrónica.

Un subproceso puede usar la [**función PurgeComm para**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) descartar todos los caracteres del búfer de entrada o salida de un dispositivo. **PurgeComm también** puede finalizar las operaciones de lectura o escritura pendientes, incluso si las operaciones no se han completado. Si un subproceso usa **PurgeComm para** vaciar un búfer de salida, no se transmiten los caracteres eliminados. Para vaciar el búfer de salida mientras se garantiza que se transmite el contenido, un subproceso puede llamar a la función [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) (una operación sincrónica). Sin embargo, tenga en cuenta que **FlushFileBuffers** está sujeto al control de flujo, pero no a los tiempos de espera de escritura, y no volverá hasta que se hayan transmitido todas las operaciones de escritura pendientes.

 

 
