---
description: Windows almacena los datos en las operaciones de lectura y escritura de archivos en los búferes de datos mantenidos por el sistema para optimizar el rendimiento del disco.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Vaciar System-Buffered datos de e/s en el disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0639c5ea909d96a248bb563f1c6a08cd7a526d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546691"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a><span data-ttu-id="fc6f8-103">Vaciar System-Buffered datos de e/s en el disco</span><span class="sxs-lookup"><span data-stu-id="fc6f8-103">Flushing System-Buffered I/O Data to Disk</span></span>

<span data-ttu-id="fc6f8-104">Windows almacena los datos en las operaciones de lectura y escritura de archivos en los búferes de datos mantenidos por el sistema para optimizar el rendimiento del disco.</span><span class="sxs-lookup"><span data-stu-id="fc6f8-104">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span> <span data-ttu-id="fc6f8-105">Cuando una aplicación escribe en un archivo, el sistema normalmente almacena en búfer los datos y escribe los datos en el disco de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="fc6f8-105">When an application writes to a file, the system usually buffers the data and writes the data to the disk on a regular basis.</span></span> <span data-ttu-id="fc6f8-106">Una aplicación puede obligar al sistema operativo a escribir el contenido de estos búferes de datos en el disco mediante la función [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) .</span><span class="sxs-lookup"><span data-stu-id="fc6f8-106">An application can force the operating system to write the contents of these data buffers to the disk by using the [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) function.</span></span> <span data-ttu-id="fc6f8-107">Como alternativa, una aplicación puede especificar que las operaciones de escritura omitan el búfer de datos y escriban directamente en el disco estableciendo la marca de **archivo sin marca de \_ almacenamiento en \_ \_ búfer** cuando se crea o se abre el archivo con la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="fc6f8-107">Alternatively, an application can specify that write operations are to bypass the data buffer and write directly to the disk by setting the **FILE\_FLAG\_NO\_BUFFERING** flag when the file is created or opened using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

<span data-ttu-id="fc6f8-108">Si hay datos en el búfer interno cuando el archivo está cerrado, el sistema operativo no escribe automáticamente el contenido del búfer en el disco antes de cerrar el archivo.</span><span class="sxs-lookup"><span data-stu-id="fc6f8-108">If there is data in the internal buffer when the file is closed, the operating system does not automatically write the contents of the buffer to the disk before closing the file.</span></span> <span data-ttu-id="fc6f8-109">Si la aplicación no obliga al sistema operativo a escribir el búfer en el disco antes de cerrar el archivo, el algoritmo de almacenamiento en caché determina cuándo se escribe el búfer.</span><span class="sxs-lookup"><span data-stu-id="fc6f8-109">If the application does not force the operating system to write the buffer to disk before closing the file, the caching algorithm determines when the buffer is written.</span></span>

> [!Note]  
> <span data-ttu-id="fc6f8-110">El acceso a un búfer de datos mientras una operación de lectura o escritura lo está usando puede dañar el búfer.</span><span class="sxs-lookup"><span data-stu-id="fc6f8-110">Accessing a data buffer while a read or write operation is using it may corrupt the buffer.</span></span> <span data-ttu-id="fc6f8-111">Las aplicaciones no deben leer, escribir en, reasignar o liberar el búfer de datos que está usando una operación de lectura o escritura hasta que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="fc6f8-111">Applications must not read from, write to, reallocate, or free the data buffer that a read or write operation is using until the operation completes.</span></span>

 

 

 



