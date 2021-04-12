---
description: Describe cómo los puntos de reanálisis habilitan el comportamiento del sistema de archivos que se deriva del comportamiento que esperan la mayoría de los desarrolladores de Windows.
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Puntos de análisis y operaciones de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1132197cd689157cd9f219afa5bfc1474b587c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278280"
---
# <a name="reparse-points-and-file-operations"></a><span data-ttu-id="74791-103">Puntos de análisis y operaciones de archivo</span><span class="sxs-lookup"><span data-stu-id="74791-103">Reparse Points and File Operations</span></span>

<span data-ttu-id="74791-104">Los *puntos de reanálisis* habilitan el comportamiento del sistema de archivos que se deriva del comportamiento que pueden estar acostumbrados a la mayoría de los desarrolladores de Windows, por lo que es consciente de estos comportamientos cuando la escritura de aplicaciones que manipulan archivos es vital para aplicaciones sólidas y confiables para tener acceso a sistemas de archivos que admiten puntos de análisis.</span><span class="sxs-lookup"><span data-stu-id="74791-104">*Reparse points* enable file system behavior that departs from the behavior most Windows developers may be accustomed to, therefore being aware of these behaviors when writing applications that manipulate files is vital to robust and reliable applications intended to access file systems that support reparse points.</span></span> <span data-ttu-id="74791-105">La extensión de estas consideraciones dependerá de la implementación específica y del comportamiento del filtro del sistema de archivos asociado de un punto de análisis determinado, que puede ser definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="74791-105">The extent of these considerations will depend on the specific implementation and associated file system filter behavior of a particular reparse point, which can be user-defined.</span></span> <span data-ttu-id="74791-106">Para obtener más información, vea [puntos de reanálisis](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="74791-106">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="74791-107">Considere los ejemplos siguientes con respecto a las implementaciones de punto de reanálisis de NTFS, entre las que se incluyen las carpetas montadas, los archivos vinculados y el servidor de almacenamiento remoto de Microsoft:</span><span class="sxs-lookup"><span data-stu-id="74791-107">Consider the following examples regarding NTFS reparse point implementations, which include mounted folders, linked files, and the Microsoft Remote Storage Server:</span></span>

-   <span data-ttu-id="74791-108">Las aplicaciones de copia de seguridad que usan [secuencias de archivos](file-streams.md) deben especificar los **\_ \_ datos de reanálisis de copia de seguridad** en la estructura de la [**\_ secuencia \_ de Win32**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) al realizar copias de seguridad de archivos con puntos de reanálisis.</span><span class="sxs-lookup"><span data-stu-id="74791-108">Backup applications that use [file streams](file-streams.md) should specify **BACKUP\_REPARSE\_DATA** in the [**WIN32\_STREAM\_ID**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) structure when backing up files with reparse points.</span></span>
-   <span data-ttu-id="74791-109">Las aplicaciones que utilizan la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) deben especificar el indicador de **\_ \_ \_ \_ punto de reanálisis** de la marca de archivo al abrir el archivo si es un punto de análisis.</span><span class="sxs-lookup"><span data-stu-id="74791-109">Applications that use the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function should specify the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag when opening the file if it is a reparse point.</span></span> <span data-ttu-id="74791-110">Para obtener más información, vea [crear y abrir archivos](creating-and-opening-files.md).</span><span class="sxs-lookup"><span data-stu-id="74791-110">For more information, see [Creating and Opening Files](creating-and-opening-files.md).</span></span>
-   <span data-ttu-id="74791-111">El proceso de [desfragmentación de archivos](defragmenting-files.md) requiere un tratamiento especial para los puntos de reanálisis.</span><span class="sxs-lookup"><span data-stu-id="74791-111">The process of [defragmenting files](defragmenting-files.md) requires special handling for reparse points.</span></span>
-   <span data-ttu-id="74791-112">Las aplicaciones de detección de virus deben buscar puntos de repetición de análisis que indiquen archivos vinculados.</span><span class="sxs-lookup"><span data-stu-id="74791-112">Virus detection applications should search for reparse points that indicate linked files.</span></span>
-   <span data-ttu-id="74791-113">La mayoría de las aplicaciones deben tomar medidas especiales para los archivos que se han migrado a un almacenamiento a largo plazo, si solo se notifica al usuario que puede tardar algún tiempo en recuperar el archivo.</span><span class="sxs-lookup"><span data-stu-id="74791-113">Most applications should take special actions for files that have been moved to long-term storage, if only to notify the user that it may take a while to retrieve the file.</span></span>
-   <span data-ttu-id="74791-114">La función [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) abrirá el archivo o el punto de reanálisis, en función del uso de la marca de **\_ \_ \_ \_ punto de reanálisis** de la marca de archivo.</span><span class="sxs-lookup"><span data-stu-id="74791-114">The [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) function will either open the file or the reparse point, depending on the use of the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span>
-   <span data-ttu-id="74791-115">Los vínculos simbólicos, como puntos de análisis, tienen ciertas [consideraciones de programación](symbolic-link-programming-considerations.md) específicas para ellos.</span><span class="sxs-lookup"><span data-stu-id="74791-115">Symbolic links, as reparse points, have certain [programming considerations](symbolic-link-programming-considerations.md) specific to them.</span></span>
-   <span data-ttu-id="74791-116">Las actividades de administración de volúmenes para leer los registros del diario de cambios del número de secuencias actualizadas (USN) requieren un tratamiento especial para los puntos de reanálisis cuando se usa el [**\_ registro USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) y se leen las estructuras de [**\_ \_ \_ datos del diario USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) .</span><span class="sxs-lookup"><span data-stu-id="74791-116">Volume management activities for reading update sequence number (USN) change journal records require special handling for reparse points when using the [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**READ\_USN\_JOURNAL\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) structures.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74791-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74791-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74791-118">Determinar si un directorio es una carpeta montada</span><span class="sxs-lookup"><span data-stu-id="74791-118">Determining Whether a Directory Is a Mounted Folder</span></span>](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[<span data-ttu-id="74791-119">Crear carpetas montadas</span><span class="sxs-lookup"><span data-stu-id="74791-119">Creating Mounted Folders</span></span>](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[<span data-ttu-id="74791-120">Efectos simbólicos de los vínculos en las funciones del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="74791-120">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
