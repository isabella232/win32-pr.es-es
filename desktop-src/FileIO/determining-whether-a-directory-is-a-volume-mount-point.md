---
description: Cómo determinar si un directorio especificado es una carpeta montada.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Determinar si un directorio es una carpeta montada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7492a3114ff0c9c9ce0685c6d3e2b94724457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912314"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a><span data-ttu-id="9145f-103">Determinar si un directorio es una carpeta montada</span><span class="sxs-lookup"><span data-stu-id="9145f-103">Determining Whether a Directory Is a Mounted Folder</span></span>

<span data-ttu-id="9145f-104">Resulta útil para determinar si un directorio es una carpeta montada cuando, por ejemplo, se usa una aplicación de copia de seguridad o de búsqueda que está limitada a un volumen.</span><span class="sxs-lookup"><span data-stu-id="9145f-104">It is useful to determine whether a directory is a mounted folder when, for example, you are using a backup or search application that is limited to one volume.</span></span> <span data-ttu-id="9145f-105">Este tipo de aplicación puede obtener información sobre varios volúmenes si usa funciones como [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para crear carpetas montadas para los demás volúmenes del volumen en el que la aplicación está limitada.</span><span class="sxs-lookup"><span data-stu-id="9145f-105">Such an application can reach information on multiple volumes if you use functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) to create mounted folders for the other volumes on the volume that the application is limited to.</span></span> <span data-ttu-id="9145f-106">Para obtener más información, vea [crear carpetas montadas](mounting-and-dismounting-a-volume.md).</span><span class="sxs-lookup"><span data-stu-id="9145f-106">For more information, see [Creating Mounted Folders](mounting-and-dismounting-a-volume.md).</span></span>

<span data-ttu-id="9145f-107">Para determinar si un directorio especificado es una carpeta montada, llame primero a la función [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) e inspeccione la marca de **\_ \_ \_ punto de reanálisis del atributo de archivo** en el valor devuelto para ver si el directorio tiene un punto de análisis asociado.</span><span class="sxs-lookup"><span data-stu-id="9145f-107">To determine if a specified directory is a mounted folder, first call the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function and inspect the **FILE\_ATTRIBUTE\_REPARSE\_POINT** flag in the return value to see if the directory has an associated reparse point.</span></span> <span data-ttu-id="9145f-108">Si es así, utilice las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) y [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) para obtener la etiqueta de reanálisis en el miembro **dwReserved0** de la estructura de [**\_ \_ datos de búsqueda de Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) .</span><span class="sxs-lookup"><span data-stu-id="9145f-108">If it does, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) functions to obtain the reparse tag in the **dwReserved0** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="9145f-109">Para determinar si el punto de reanálisis es una carpeta montada (y no otra forma de punto de análisis), compruebe si el valor de la etiqueta es igual al punto de montaje de la **\_ etiqueta de reanálisis \_ \_ \_ de e/s**.</span><span class="sxs-lookup"><span data-stu-id="9145f-109">To determine if the reparse point is a mounted folder (and not some other form of reparse point), test whether the tag value equals the value **IO\_REPARSE\_TAG\_MOUNT\_POINT**.</span></span> <span data-ttu-id="9145f-110">Para obtener más información, vea [puntos de reanálisis](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="9145f-110">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="9145f-111">Para obtener el volumen de destino de una carpeta montada, utilice la función [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .</span><span class="sxs-lookup"><span data-stu-id="9145f-111">To obtain the target volume of a mounted folder, use the [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) function.</span></span>

<span data-ttu-id="9145f-112">De forma similar, puede determinar si un punto de análisis es un vínculo simbólico comprobando si el valor de etiqueta es el **\_ \_ \_ SYMLINK de etiqueta de reanálisis de e/s**.</span><span class="sxs-lookup"><span data-stu-id="9145f-112">In a similar manner, you can determine if a reparse point is a symbolic link by testing whether the tag value is **IO\_REPARSE\_TAG\_SYMLINK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9145f-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9145f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9145f-114">**Constantes de atributo de archivo**</span><span class="sxs-lookup"><span data-stu-id="9145f-114">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 



