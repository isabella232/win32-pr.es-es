---
description: Las aplicaciones pueden recuperar y establecer la fecha y la hora en que se crea un archivo, se modifica por última vez o se obtiene acceso por última vez mediante las funciones GetFileTime y SetFileTime.
ms.assetid: f8930be6-7c2a-4e50-a7a1-d25f6e2a3951
title: Establecer y obtener la marca de tiempo de un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34735994dd3017662f517a8c0a57be1d5c0e3096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275574"
---
# <a name="setting-and-getting-the-timestamp-of-a-file"></a><span data-ttu-id="df158-103">Establecer y obtener la marca de tiempo de un archivo</span><span class="sxs-lookup"><span data-stu-id="df158-103">Setting and Getting the Timestamp of a File</span></span>

<span data-ttu-id="df158-104">Las aplicaciones pueden recuperar y establecer la fecha y la hora en que se crea un archivo, se modifica por última vez o se obtiene acceso por última vez mediante las funciones [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) y [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) .</span><span class="sxs-lookup"><span data-stu-id="df158-104">Applications can retrieve and set the date and time a file is created, last modified, or last accessed by using the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) and [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) functions.</span></span> <span data-ttu-id="df158-105">Para obtener más información, vea [tiempos de archivo](/windows/desktop/SysInfo/file-times).</span><span class="sxs-lookup"><span data-stu-id="df158-105">For more information, see [File Times](/windows/desktop/SysInfo/file-times).</span></span>

> [!Note]  
> <span data-ttu-id="df158-106">No todos los sistemas de archivos pueden registrar los tiempos de creación y último acceso, y no todos los sistemas de archivos los registran de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="df158-106">Not all file systems can record creation and last access times, and not all file systems record them in the same manner.</span></span> <span data-ttu-id="df158-107">Por ejemplo, en el sistema de archivos FAT, la hora de creación tiene una resolución de 10 milisegundos, el tiempo de escritura tiene una resolución de 2 segundos y el tiempo de acceso tiene una resolución de 1 día (realmente, la fecha de acceso).</span><span class="sxs-lookup"><span data-stu-id="df158-107">For example, on FAT file system, create time has a resolution of 10 milliseconds, write time has a resolution of 2 seconds, and access time has a resolution of 1 day (really, the access date).</span></span> <span data-ttu-id="df158-108">El sistema de archivos NTFS retrasa la actualización a la última hora de acceso de un archivo hasta una hora después del último acceso.</span><span class="sxs-lookup"><span data-stu-id="df158-108">The NTFS file system delays update to the last access time for a file by up to one hour after the last access.</span></span>

 

 

 
