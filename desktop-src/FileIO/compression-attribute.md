---
description: En un volumen del sistema de archivos NTFS, cada archivo y directorio tiene un atributo de compresión.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Atributo Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8e86eebe919476851f35f77cf10d6a07035d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913710"
---
# <a name="compression-attribute"></a><span data-ttu-id="55305-103">Atributo Compression</span><span class="sxs-lookup"><span data-stu-id="55305-103">Compression Attribute</span></span>

<span data-ttu-id="55305-104">En un volumen del sistema de archivos NTFS, cada archivo y directorio tiene un *atributo de compresión*.</span><span class="sxs-lookup"><span data-stu-id="55305-104">On an NTFS file system volume, each file and directory has a *compression attribute*.</span></span> <span data-ttu-id="55305-105">Otros sistemas de archivos también pueden implementar un atributo de compresión para archivos y directorios individuales.</span><span class="sxs-lookup"><span data-stu-id="55305-105">Other file systems may also implement a compression attribute for individual files and directories.</span></span>

<span data-ttu-id="55305-106">Puede determinar si un sistema de archivos admite un atributo de compresión para archivos y directorios mediante una llamada a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examinando el indicador de bits de **compresión de \_ archivo \_ de archivo** .</span><span class="sxs-lookup"><span data-stu-id="55305-106">You can determine whether a file system supports a compression attribute for files and directories by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_FILE\_COMPRESSION** bit flag.</span></span>

<span data-ttu-id="55305-107">Utilice la función [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) o [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) para determinar el atributo de compresión de un archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="55305-107">Use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) or [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) function to determine the compression attribute of a file or directory.</span></span>

<span data-ttu-id="55305-108">Si se establece el atributo de compresión de un archivo (**archivo \_ \_ comprimido con atributo**), se comprimen todos los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="55305-108">If a file's compression attribute is set (**FILE\_ATTRIBUTE\_COMPRESSED**), all data in the file is compressed.</span></span> <span data-ttu-id="55305-109">Si el atributo está desactivado, no se comprime ninguno de los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="55305-109">If the attribute is clear, none of the data in the file is compressed.</span></span> <span data-ttu-id="55305-110">No hay ningún estado parcialmente comprimido desde una perspectiva de programación de modo de usuario. el atributo Compression es un indicador booleano simple de estado de compresión.</span><span class="sxs-lookup"><span data-stu-id="55305-110">There is no partially compressed state from a user-mode programming perspective; the compression attribute is a simple Boolean indicator of compression state.</span></span>

<span data-ttu-id="55305-111">El atributo Compression de un directorio proporciona un atributo de compresión predeterminado para los archivos y subdirectorios recién creados.</span><span class="sxs-lookup"><span data-stu-id="55305-111">A directory's compression attribute provides a default compression attribute for newly created files and subdirectories.</span></span> <span data-ttu-id="55305-112">Cuando se llama a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) o a [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) para crear un nuevo archivo o directorio, el nuevo archivo o directorio hereda el atributo Compression de su directorio principal.</span><span class="sxs-lookup"><span data-stu-id="55305-112">When you call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) to create a new file or directory, the new file or directory inherits the compression attribute of its parent directory.</span></span>

<span data-ttu-id="55305-113">Para modificar el atributo de **archivo \_ \_ comprimido** para un archivo o directorio, debe usar la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con el código de control de [**\_ \_ compresión set de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) .</span><span class="sxs-lookup"><span data-stu-id="55305-113">To modify the **FILE\_ATTRIBUTE\_COMPRESSED** attribute for a file or directory, you must use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55305-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55305-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55305-115">**Constantes de atributo de archivo**</span><span class="sxs-lookup"><span data-stu-id="55305-115">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 
