---
description: Cuando un proceso abre un archivo mediante la función CreateFile, se asocia un identificador de archivo hasta que el proceso finaliza o el identificador se cierra con la función CloseHandle.
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: Identificadores de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a54db1935108ab18666fb460a071d77c50f793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912862"
---
# <a name="file-handles"></a><span data-ttu-id="94a58-103">Identificadores de archivo</span><span class="sxs-lookup"><span data-stu-id="94a58-103">File Handles</span></span>

<span data-ttu-id="94a58-104">Cuando un proceso abre un archivo mediante la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , se asocia un *identificador de archivo* hasta que el proceso finaliza o el identificador se cierra con la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="94a58-104">When a file is opened by a process using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, a *file handle* is associated with it until either the process terminates or the handle is closed using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="94a58-105">El identificador de archivo se utiliza para identificar el archivo en muchas llamadas a funciones.</span><span class="sxs-lookup"><span data-stu-id="94a58-105">The file handle is used to identify the file in many function calls.</span></span>

<span data-ttu-id="94a58-106">Cada objeto de archivo y identificador de archivo es generalmente único para cada proceso que abre un archivo, lo único que se produce cuando se duplica un identificador de archivo mantenido por un proceso, o cuando un proceso secundario hereda los identificadores de archivo del proceso primario.</span><span class="sxs-lookup"><span data-stu-id="94a58-106">Each file handle and file object is generally unique to each process that opens a file—the only exceptions to this are when a file handle held by a process is duplicated, or when a child process inherits the file handles of the parent process.</span></span> <span data-ttu-id="94a58-107">En estas situaciones, estos identificadores de archivo son únicos, pero se ve un solo objeto de archivo compartido.</span><span class="sxs-lookup"><span data-stu-id="94a58-107">In these situations, these file handles are unique, but see a single, shared file object.</span></span> <span data-ttu-id="94a58-108">Consulte [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) para obtener más información sobre la duplicación de identificadores de archivos que se mantienen en los procesos.</span><span class="sxs-lookup"><span data-stu-id="94a58-108">See [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) for more information on duplicating file handles held by processes.</span></span>

<span data-ttu-id="94a58-109">Tenga en cuenta que, mientras que los identificadores de archivo suelen ser privados para un proceso, los datos de archivo a los que apunta el punto de control no son.</span><span class="sxs-lookup"><span data-stu-id="94a58-109">Note that while the file handles are typically private to a process, the file data that the file handles point to is not.</span></span> <span data-ttu-id="94a58-110">Por lo tanto, los procesos y subprocesos que comparten el mismo archivo deben sincronizar su acceso.</span><span class="sxs-lookup"><span data-stu-id="94a58-110">Therefore, processes and threads that share the same file must synchronize their access.</span></span> <span data-ttu-id="94a58-111">Para la mayoría de las operaciones en un archivo, un proceso identifica el archivo a través de su grupo privado de identificadores.</span><span class="sxs-lookup"><span data-stu-id="94a58-111">For most operations on a file, a process identifies the file through its private pool of handles.</span></span>

 

 
