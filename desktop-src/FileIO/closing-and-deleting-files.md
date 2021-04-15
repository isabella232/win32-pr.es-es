---
description: Para utilizar los recursos del sistema operativo de forma eficaz, una aplicación debe cerrar los archivos cuando ya no se necesiten mediante la función CloseHandle. Si un archivo está abierto cuando una aplicación finaliza, el sistema lo cierra automáticamente.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Cerrar y eliminar archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3da31fe7ff38a1bbd1555e2685ceab9ae432574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669697"
---
# <a name="closing-and-deleting-files"></a><span data-ttu-id="52925-104">Cerrar y eliminar archivos</span><span class="sxs-lookup"><span data-stu-id="52925-104">Closing and Deleting Files</span></span>

<span data-ttu-id="52925-105">Para utilizar los recursos del sistema operativo de forma eficaz, una aplicación debe cerrar los archivos cuando ya no se necesiten mediante la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="52925-105">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="52925-106">Si un archivo está abierto cuando una aplicación finaliza, el sistema lo cierra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="52925-106">If a file is open when an application terminates, the system closes it automatically.</span></span>

<span data-ttu-id="52925-107">La función [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) se puede usar para eliminar un archivo al cerrar.</span><span class="sxs-lookup"><span data-stu-id="52925-107">The [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function can be used to delete a file on close.</span></span> <span data-ttu-id="52925-108">No se puede eliminar un archivo hasta que se cierren todos los identificadores.</span><span class="sxs-lookup"><span data-stu-id="52925-108">A file cannot be deleted until all handles to it are closed.</span></span> <span data-ttu-id="52925-109">Si no se puede eliminar un archivo, no se puede volver a usar su nombre.</span><span class="sxs-lookup"><span data-stu-id="52925-109">If a file cannot be deleted, its name cannot be reused.</span></span> <span data-ttu-id="52925-110">Para volver a usar un nombre de archivo inmediatamente, cambie el nombre del archivo existente.</span><span class="sxs-lookup"><span data-stu-id="52925-110">To reuse a file name immediately, rename the existing file.</span></span>

<span data-ttu-id="52925-111">Si elimina un archivo o un directorio abierto en un equipo remoto y ya se ha abierto en el equipo remoto sin el permiso leer recurso compartido establecido, no llame a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) o a [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) para abrir primero el archivo o el directorio para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="52925-111">If you are deleting an open file or directory on a remote machine and it has already been opened on the remote machine without the read share permission set, do not call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) to open the file or directory for deletion first.</span></span> <span data-ttu-id="52925-112">Si lo hace, se producirá una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="52925-112">Doing so will result in a sharing violation.</span></span>

 

 
