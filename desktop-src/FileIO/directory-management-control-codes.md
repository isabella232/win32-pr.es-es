---
description: Códigos de control que se usan con la compresión y descompresión de archivos y con puntos de reanálisis.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Códigos de control de administración de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0463860e3c899178ec5b8f9d44bd05cf4278e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912313"
---
# <a name="directory-management-control-codes"></a><span data-ttu-id="5d9f6-103">Códigos de control de administración de directorios</span><span class="sxs-lookup"><span data-stu-id="5d9f6-103">Directory Management Control Codes</span></span>

<span data-ttu-id="5d9f6-104">Los siguientes códigos de control se usan con la [compresión y descompresión de archivos](file-compression-and-decompression.md).</span><span class="sxs-lookup"><span data-stu-id="5d9f6-104">The following control codes are used with [file compression and decompression](file-compression-and-decompression.md).</span></span>



| <span data-ttu-id="5d9f6-105">Código de control</span><span class="sxs-lookup"><span data-stu-id="5d9f6-105">Control Code</span></span>                                             | <span data-ttu-id="5d9f6-106">Significado</span><span class="sxs-lookup"><span data-stu-id="5d9f6-106">Meaning</span></span>                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d9f6-107">**compresión de FSCTL \_ obtener \_**</span><span class="sxs-lookup"><span data-stu-id="5d9f6-107">**FSCTL\_GET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | <span data-ttu-id="5d9f6-108">Recupera el estado de compresión actual de un archivo o directorio en un volumen cuyo sistema de archivos admite la compresión por secuencia.</span><span class="sxs-lookup"><span data-stu-id="5d9f6-108">Retrieves the current compression state of a file or directory on a volume whose file system supports per-stream compression.</span></span><br/>    |
| [<span data-ttu-id="5d9f6-109">**\_configuración de \_ compresión de FSCTL**</span><span class="sxs-lookup"><span data-stu-id="5d9f6-109">**FSCTL\_SET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | <span data-ttu-id="5d9f6-110">Establece el estado de compresión de un archivo o directorio en un volumen cuyo sistema de archivos admite la compresión por archivo y por directorio.</span><span class="sxs-lookup"><span data-stu-id="5d9f6-110">Sets the compression state of a file or directory on a volume whose file system supports per-file and per-directory compression.</span></span><br/> |



 

<span data-ttu-id="5d9f6-111">Los siguientes códigos de control se utilizan con [puntos de repetición de análisis](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="5d9f6-111">The following control codes are used with [reparse points](reparse-points.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5d9f6-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5d9f6-112">In this section</span></span>



| <span data-ttu-id="5d9f6-113">Código de control</span><span class="sxs-lookup"><span data-stu-id="5d9f6-113">Control Code</span></span>                                                                   | <span data-ttu-id="5d9f6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d9f6-114">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d9f6-115">**\_punto de \_ reanálisis de eliminación de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="5d9f6-115">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | <span data-ttu-id="5d9f6-116">Elimina un punto de análisis del archivo o directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="5d9f6-116">Deletes a reparse point from the specified file or directory.</span></span><br/>                                              |
| [<span data-ttu-id="5d9f6-117">**\_punto de \_ repetición de análisis de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="5d9f6-117">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | <span data-ttu-id="5d9f6-118">Recupera los datos del punto de reanálisis asociados al archivo o directorio identificado por el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="5d9f6-118">Retrieves the reparse point data associated with the file or directory identified by the specified handle.</span></span><br/> |
| [<span data-ttu-id="5d9f6-119">**\_grupo de \_ análisis de conjunto de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="5d9f6-119">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | <span data-ttu-id="5d9f6-120">Establece un punto de repetición de análisis en un archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="5d9f6-120">Sets a reparse point on a file or directory.</span></span><br/>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="5d9f6-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d9f6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d9f6-122">Códigos de control de administración de archivos</span><span class="sxs-lookup"><span data-stu-id="5d9f6-122">File Management Control Codes</span></span>](file-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="5d9f6-123">Códigos de control de administración del volumen</span><span class="sxs-lookup"><span data-stu-id="5d9f6-123">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

