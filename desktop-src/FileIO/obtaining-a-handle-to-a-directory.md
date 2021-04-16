---
description: Cada vez que un proceso crea o abre un objeto de directorio, recibe un identificador para el objeto.
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Identificadores de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669865"
---
# <a name="directory-handles"></a><span data-ttu-id="a679a-103">Identificadores de directorio</span><span class="sxs-lookup"><span data-stu-id="a679a-103">Directory Handles</span></span>

<span data-ttu-id="a679a-104">Cada vez que un proceso crea o abre un objeto de directorio, recibe un identificador para el objeto.</span><span class="sxs-lookup"><span data-stu-id="a679a-104">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span>

<span data-ttu-id="a679a-105">Para obtener un identificador de un directorio existente, llame a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con la marca de **semántica de copia de \_ \_ seguridad \_ del marcador de archivo** .</span><span class="sxs-lookup"><span data-stu-id="a679a-105">To obtain a handle to an existing directory, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_BACKUP\_SEMANTICS** flag.</span></span>

<span data-ttu-id="a679a-106">Puede pasar un identificador de directorio a las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="a679a-106">You can pass a directory handle to the following functions.</span></span>



| <span data-ttu-id="a679a-107">Función</span><span class="sxs-lookup"><span data-stu-id="a679a-107">Function</span></span>                                                         | <span data-ttu-id="a679a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a679a-108">Description</span></span>                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a679a-109">**BackupRead**</span><span class="sxs-lookup"><span data-stu-id="a679a-109">**BackupRead**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupread)                              | <span data-ttu-id="a679a-110">Realice una copia de seguridad de un archivo o directorio, incluida la información de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a679a-110">Back up a file or directory, including the security information.</span></span><br/>                                                                                      |
| [<span data-ttu-id="a679a-111">**BackupSeek**</span><span class="sxs-lookup"><span data-stu-id="a679a-111">**BackupSeek**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | <span data-ttu-id="a679a-112">Busca hacia delante en un flujo de datos al que se tiene acceso inicialmente mediante la función [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) o [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) .</span><span class="sxs-lookup"><span data-stu-id="a679a-112">Seeks forward in a data stream initially accessed by using the [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) or [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) function.</span></span><br/> |
| [<span data-ttu-id="a679a-113">**BackupWrite**</span><span class="sxs-lookup"><span data-stu-id="a679a-113">**BackupWrite**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | <span data-ttu-id="a679a-114">Restaure un archivo o directorio del que se realizó una copia de seguridad con [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).</span><span class="sxs-lookup"><span data-stu-id="a679a-114">Restore a file or directory that was backed up using [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).</span></span><br/>                                                             |
| [<span data-ttu-id="a679a-115">**GetFileInformationByHandle**</span><span class="sxs-lookup"><span data-stu-id="a679a-115">**GetFileInformationByHandle**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | <span data-ttu-id="a679a-116">Recupera información de archivo para el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a679a-116">Retrieves file information for the specified file.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="a679a-117">**GetFileSize**</span><span class="sxs-lookup"><span data-stu-id="a679a-117">**GetFileSize**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | <span data-ttu-id="a679a-118">Recupera el tamaño del archivo especificado, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a679a-118">Retrieves the size of the specified file, in bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="a679a-119">**GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="a679a-119">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="a679a-120">Recupera la fecha y la hora en que se creó un archivo o directorio, se obtuvo acceso por última vez y se modificó por última vez.</span><span class="sxs-lookup"><span data-stu-id="a679a-120">Retrieves the date and time that a file or directory was created, last accessed, and last modified.</span></span><br/>                                                   |
| [<span data-ttu-id="a679a-121">**GetFileType**</span><span class="sxs-lookup"><span data-stu-id="a679a-121">**GetFileType**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | <span data-ttu-id="a679a-122">Recupera el tipo de archivo del archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a679a-122">Retrieves the file type of the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="a679a-123">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="a679a-123">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | <span data-ttu-id="a679a-124">Recupera información que describe los cambios en el directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="a679a-124">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                      |
| [<span data-ttu-id="a679a-125">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="a679a-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="a679a-126">Establece la fecha y la hora en que se creó el archivo o directorio especificado, se obtuvo acceso por última vez o se modificó por última vez.</span><span class="sxs-lookup"><span data-stu-id="a679a-126">Sets the date and time that the specified file or directory was created, last accessed, or last modified.</span></span><br/>                                             |



 

 

