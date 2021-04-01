---
description: Obtiene el tamaño asignado o el tamaño total de un archivo mediante la función GetCompressedFileSize o GetFileSize.
ms.assetid: 1894ea01-49ff-41e3-9912-1cd75966bd3f
title: Obtención del tamaño de un archivo disperso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93a1c6a33f0d6913e0e6848e4593ea0e0bf0259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908193"
---
# <a name="obtaining-the-size-of-a-sparse-file"></a><span data-ttu-id="d48a8-103">Obtención del tamaño de un archivo disperso</span><span class="sxs-lookup"><span data-stu-id="d48a8-103">Obtaining the Size of a Sparse File</span></span>

<span data-ttu-id="d48a8-104">Utilice la función [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) para obtener el tamaño real asignado en el disco para un archivo disperso.</span><span class="sxs-lookup"><span data-stu-id="d48a8-104">Use the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) function to obtain the actual size allocated on disk for a sparse file.</span></span> <span data-ttu-id="d48a8-105">Este total no incluye el tamaño de las regiones que se han desasignado porque se han rellenado con ceros.</span><span class="sxs-lookup"><span data-stu-id="d48a8-105">This total does not include the size of the regions which were deallocated because they were filled with zeros.</span></span> <span data-ttu-id="d48a8-106">Use la función [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) para determinar el tamaño total de un archivo, incluido el tamaño de las regiones dispersas que se han desasignado.</span><span class="sxs-lookup"><span data-stu-id="d48a8-106">Use the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function to determine the total size of a file, including the size of the sparse regions that were deallocated.</span></span>

 

 



