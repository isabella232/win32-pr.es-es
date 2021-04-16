---
description: Para obtener el tamaño comprimido de un archivo, use la función GetCompressedFileSize.
ms.assetid: c6bfd221-f125-48b4-b38b-822a23639c40
title: Obtención del tamaño de un archivo comprimido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4954a53184e55341838fef7cd70f01639f13bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542755"
---
# <a name="obtaining-the-size-of-a-compressed-file"></a><span data-ttu-id="abeb1-103">Obtención del tamaño de un archivo comprimido</span><span class="sxs-lookup"><span data-stu-id="abeb1-103">Obtaining the Size of a Compressed File</span></span>

<span data-ttu-id="abeb1-104">Utilice la función [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) para obtener el tamaño comprimido de un archivo.</span><span class="sxs-lookup"><span data-stu-id="abeb1-104">Use the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) function to obtain the compressed size of a file.</span></span> <span data-ttu-id="abeb1-105">Si el archivo está comprimido, su tamaño comprimido será menor que el tamaño sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="abeb1-105">If the file is compressed, its compressed size will be less than its uncompressed size.</span></span> <span data-ttu-id="abeb1-106">Utilice la función [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) para determinar el tamaño sin comprimir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="abeb1-106">Use the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function to determine the uncompressed size of a file.</span></span>

 

 



