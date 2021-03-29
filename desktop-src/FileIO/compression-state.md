---
description: Cada archivo y directorio de un volumen que admite la compresión de archivos y directorios individuales tiene un estado de compresión.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: Estado de compresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e182921a6c5e1b79c08fbafb6a8104c4bd8ca1cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277057"
---
# <a name="compression-state"></a><span data-ttu-id="6896a-103">Estado de compresión</span><span class="sxs-lookup"><span data-stu-id="6896a-103">Compression State</span></span>

<span data-ttu-id="6896a-104">Cada archivo y directorio de un volumen que admite la compresión de archivos y directorios individuales tiene un *Estado de compresión*.</span><span class="sxs-lookup"><span data-stu-id="6896a-104">Each file and directory on a volume that supports compression for individual files and directories has a *compression state*.</span></span>

<span data-ttu-id="6896a-105">Mientras que el atributo de compresión de un archivo o directorio indica simplemente si el archivo o el directorio está comprimido o no comprimido, el estado de compresión también especifica el formato de los datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="6896a-105">Whereas the compression attribute of a file or directory indicates simply whether the file or directory is compressed or not compressed, the compression state also specifies the format of any compressed data.</span></span>

<span data-ttu-id="6896a-106">Use el código de control de [**\_ \_ compresión de FSCTL obtener**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) para determinar el estado de compresión de un archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="6896a-106">Use the [**FSCTL\_GET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) control code to determine the compression state of a file or directory.</span></span>

<span data-ttu-id="6896a-107">El estado de compresión se codifica como un valor de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6896a-107">Compression state is encoded as a 16-bit value.</span></span> <span data-ttu-id="6896a-108">Un valor de estado de compresión de formato de compresión \_ \_ None indica que un archivo no está comprimido.</span><span class="sxs-lookup"><span data-stu-id="6896a-108">A compression state value of COMPRESSION\_FORMAT\_NONE indicates that a file is not compressed.</span></span> <span data-ttu-id="6896a-109">Un valor de formato de compresión \_ \_ predeterminado indica que se comprime un archivo con el formato de compresión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6896a-109">A value of COMPRESSION\_FORMAT\_DEFAULT indicates that a file is compressed, using the default compression format.</span></span> <span data-ttu-id="6896a-110">Cualquier otro valor indica que se comprime un archivo con el formato de compresión especificado por el valor de estado de compresión.</span><span class="sxs-lookup"><span data-stu-id="6896a-110">Any other value indicates that a file is compressed, using the compression format specified by the compression state value.</span></span>

<span data-ttu-id="6896a-111">Use el código de control de [**\_ \_ compresión Set Compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) para establecer el estado de compresión de un archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="6896a-111">Use the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code to set the compression state of a file or directory.</span></span> <span data-ttu-id="6896a-112">Esta operación también establece el atributo Compression del archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="6896a-112">This operation also sets the compression attribute of the file or directory.</span></span>

<span data-ttu-id="6896a-113">Al establecer el estado de compresión de un archivo en un valor distinto de cero, se comprime el archivo con el formato de compresión codificado por el valor de estado de compresión.</span><span class="sxs-lookup"><span data-stu-id="6896a-113">Setting the compression state of a file to a nonzero value compresses the file, using the compression format encoded by the compression state value.</span></span> <span data-ttu-id="6896a-114">Al establecer el estado de compresión de un archivo en cero, se descomprime el archivo.</span><span class="sxs-lookup"><span data-stu-id="6896a-114">Setting a file's compression state to zero decompresses the file.</span></span> <span data-ttu-id="6896a-115">Se trata de operaciones sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="6896a-115">These are synchronous operations.</span></span> <span data-ttu-id="6896a-116">El archivo se comprime o se descomprime inmediatamente al establecer su estado de compresión.</span><span class="sxs-lookup"><span data-stu-id="6896a-116">The file is compressed or decompressed immediately when you set its compression state.</span></span>

<span data-ttu-id="6896a-117">Establecer el estado de compresión de un directorio no provoca ninguna compresión o descompresión inmediata.</span><span class="sxs-lookup"><span data-stu-id="6896a-117">Setting a directory's compression state does not cause any immediate compression or decompression.</span></span> <span data-ttu-id="6896a-118">En su lugar, el establecimiento del estado de compresión de un directorio establece un estado de compresión predeterminado que se asignará a todos los archivos y subdirectorios recién creados.</span><span class="sxs-lookup"><span data-stu-id="6896a-118">Instead, setting a directory's compression state sets a default compression state that will be given to all newly created files and subdirectories.</span></span>

 

 
