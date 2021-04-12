---
title: Formatos de disco
description: IMAPi admite tres formatos de sistema de archivos ISO 9660, Joliet y UDF.
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9b4d4c5c5b6aa3e0c4c96598486a531c297b61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357125"
---
# <a name="disc-formats"></a><span data-ttu-id="dccb9-103">Formatos de disco</span><span class="sxs-lookup"><span data-stu-id="dccb9-103">Disc Formats</span></span>

<span data-ttu-id="dccb9-104">IMAPi admite tres formatos de sistema de archivos: [ISO 9660](#iso-9660), [Joliet](#joliet)y [UDF](#universal-disk-format-udf).</span><span class="sxs-lookup"><span data-stu-id="dccb9-104">IMAPI supports three file system formats: [ISO 9660](#iso-9660), [Joliet](#joliet), and [UDF](#universal-disk-format-udf).</span></span>

## <a name="iso-9660"></a><span data-ttu-id="dccb9-105">ISO 9660</span><span class="sxs-lookup"><span data-stu-id="dccb9-105">ISO 9660</span></span>

<span data-ttu-id="dccb9-106">El formato ISO 9660 es el sistema de archivos estándar original para los discos de datos de CD.</span><span class="sxs-lookup"><span data-stu-id="dccb9-106">The ISO 9660 format is the original standard file system for CD data discs.</span></span> <span data-ttu-id="dccb9-107">El formato se reconoce en varios sistemas operativos, como MSDOS, el Mac OS, UNIX y el sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="dccb9-107">The format is recognized on several operating systems, including MSDOS, the Mac OS, UNIX, and the Windows operating system.</span></span> <span data-ttu-id="dccb9-108">El formato ISO 9660 se publica mediante el Organización internacional de normalización (ISO).</span><span class="sxs-lookup"><span data-stu-id="dccb9-108">The ISO 9660 format is published by the International Organization for Standardization (ISO).</span></span>

<span data-ttu-id="dccb9-109">El formato comienza en el sector 16 con el encabezado Volume, CD0001; a continuación se muestra el resto del encabezado.</span><span class="sxs-lookup"><span data-stu-id="dccb9-109">The format begins at sector 16 with the volume header, CD0001; the remainder of the header follows.</span></span> <span data-ttu-id="dccb9-110">Otros formatos derivados también comienzan en el sector 16, pero usan otra cadena para el encabezado de volumen.</span><span class="sxs-lookup"><span data-stu-id="dccb9-110">Other derived formats also begin at sector 16, but use another string for the volume header.</span></span> <span data-ttu-id="dccb9-111">Por ejemplo, los discos de sierra alta usan la cadena CD-ROM0001 y el formato interactivo de disco compacto usa CD-I0001.</span><span class="sxs-lookup"><span data-stu-id="dccb9-111">For example, High Sierra discs use the string CD-ROM0001 and Compact Disc Interactive format uses CD-I0001.</span></span>

<span data-ttu-id="dccb9-112">El encabezado apunta a las áreas del disco donde se almacenan los nombres de archivo en formato ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="dccb9-112">The header points to areas of the disc that store the file names in ISO 9660 format.</span></span> <span data-ttu-id="dccb9-113">La Convención de nomenclatura de archivos y directorios consta de 8 caracteres, un punto y 3 más caracteres.</span><span class="sxs-lookup"><span data-stu-id="dccb9-113">The file and directory naming convention consists of 8 characters, a period, and 3 more characters.</span></span> <span data-ttu-id="dccb9-114">Esta es la misma Convención de nomenclatura usada por el sistema operativo MSDOS.</span><span class="sxs-lookup"><span data-stu-id="dccb9-114">This is the same naming convention used by the MSDOS operating system.</span></span>

<span data-ttu-id="dccb9-115">Los encabezados adicionales del sistema de archivos, para formatos como Joliet y UDF, pueden coexistir en un disco sin que ello afecte a la legibilidad del formato ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="dccb9-115">Additional file system headers, for formats such as Joliet and UDF, can co-exist on a disc without affecting the readability of the ISO 9660 format.</span></span> <span data-ttu-id="dccb9-116">Después de los índices, un conjunto de archivos de datos ocupa el disco. Los índices de cada sistema de archivos hacen referencia de forma independiente a los archivos de datos del disco.</span><span class="sxs-lookup"><span data-stu-id="dccb9-116">After the indexes, a set of data files occupy the disc. The indexes for each file system independently reference data files on the disc.</span></span>

<span data-ttu-id="dccb9-117">La especificación ISO 9660 define tres niveles de formato:</span><span class="sxs-lookup"><span data-stu-id="dccb9-117">The ISO 9660 specification defines three levels of the format:</span></span>

-   <span data-ttu-id="dccb9-118">El nivel 1 define los nombres de archivo para usar el formato de caracteres 8,3.</span><span class="sxs-lookup"><span data-stu-id="dccb9-118">Level 1 defines file names to use the 8.3 character format.</span></span>
-   <span data-ttu-id="dccb9-119">El nivel 2 permite nombres de archivo más largos, como se encuentra en las plataformas DOS. XX, MacIntosh y UNIX.</span><span class="sxs-lookup"><span data-stu-id="dccb9-119">Level 2 permits longer file names, as found on DOS 6.xx, MacIntosh, and UNIX platforms.</span></span>
-   <span data-ttu-id="dccb9-120">El nivel 3 permite que los datos intercalados y los archivos de audio mejoren el rendimiento de la recuperación (reproducción).</span><span class="sxs-lookup"><span data-stu-id="dccb9-120">Level 3 allows interleaved data and audio files to improve retrieval (playback) performance.</span></span> <span data-ttu-id="dccb9-121">Este nivel también quita el límite de 2 GB de archivo.</span><span class="sxs-lookup"><span data-stu-id="dccb9-121">This level also removes the 2GB file limit.</span></span> <span data-ttu-id="dccb9-122">Este nivel **no** es compatible con la API de masterización de imágenes.</span><span class="sxs-lookup"><span data-stu-id="dccb9-122">This level is **not** supported by the Image Mastering API.</span></span>

<span data-ttu-id="dccb9-123">Los discos DVD también pueden usar ISO 9660; sin embargo, el sistema de archivos UDF es el sistema de archivos más frecuente que se usa con los medios DVD.</span><span class="sxs-lookup"><span data-stu-id="dccb9-123">DVD discs can also use ISO 9660; however, the UDF file system is the most prevalent file system used with DVD media.</span></span>

## <a name="joliet"></a><span data-ttu-id="dccb9-124">Joliet</span><span class="sxs-lookup"><span data-stu-id="dccb9-124">Joliet</span></span>

<span data-ttu-id="dccb9-125">El formato Joliet es un derivado de ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="dccb9-125">The Joliet format is a derivative of ISO 9660.</span></span> <span data-ttu-id="dccb9-126">Este formato escribe el índice del sistema de archivos Joliet en la imagen de disco, además del índice del sistema de archivos ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="dccb9-126">This format writes the Joliet file system index to the disc image in addition to the ISO 9660 file system index.</span></span>

<span data-ttu-id="dccb9-127">El índice de Joliet proporciona las siguientes mejoras en el índice del sistema de archivos:</span><span class="sxs-lookup"><span data-stu-id="dccb9-127">The Joliet index provides the following improvements to the file system index:</span></span>

-   <span data-ttu-id="dccb9-128">Reconoce los nombres de archivo largos hasta 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="dccb9-128">Recognizes long file names up to 32 characters.</span></span>
-   <span data-ttu-id="dccb9-129">Distingue entre mayúsculas y minúsculas en los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="dccb9-129">Distinguishes between upper and lower case letters in the file names.</span></span>
-   <span data-ttu-id="dccb9-130">Admite caracteres Unicode en el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="dccb9-130">Supports Unicode characters in the filename.</span></span>

<span data-ttu-id="dccb9-131">El encabezado de formato Joliet comienza en el sector 17 del disco.</span><span class="sxs-lookup"><span data-stu-id="dccb9-131">The Joliet format header begins at sector 17 of the disc.</span></span>

<span data-ttu-id="dccb9-132">Dado que el formato Joliet conserva el sistema de archivos ISO 9660 en un disco, se conserva la compatibilidad con dispositivos compatibles con ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="dccb9-132">Because the Joliet format preserves the ISO 9660 file system on a disc, compatibility with ISO 9660-compliant devices is retained.</span></span>

## <a name="universal-disk-format-udf"></a><span data-ttu-id="dccb9-133">Formato de disco universal (UDF)</span><span class="sxs-lookup"><span data-stu-id="dccb9-133">Universal Disk Format (UDF)</span></span>

<span data-ttu-id="dccb9-134">El formato de disco universal (UDF) es un sistema de archivos más reciente desarrollado para medios ópticos por la Asociación de tecnología de almacenamiento óptico (OSTA).</span><span class="sxs-lookup"><span data-stu-id="dccb9-134">The Universal Disk Format (UDF) is a newer file system developed for optical media by the Optical Storage Technology Association (OSTA).</span></span> <span data-ttu-id="dccb9-135">UDF es un formato portátil reconocido por varios sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="dccb9-135">UDF is a portable format that is recognized by several operating systems.</span></span> <span data-ttu-id="dccb9-136">UDF reemplaza a ISO 9660 como el nuevo estándar, especialmente con medios de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="dccb9-136">UDF is replacing ISO 9660 as the new standard, especially with read/write media.</span></span>

<span data-ttu-id="dccb9-137">Entre las características de UDF se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="dccb9-137">Features of UDF include the following:</span></span>

-   <span data-ttu-id="dccb9-138">Admite medios con un tamaño máximo de 2 TB.</span><span class="sxs-lookup"><span data-stu-id="dccb9-138">Supports media up to 2TB in size.</span></span>
-   <span data-ttu-id="dccb9-139">Es compatible con Flash, discos Iomega REV y discos CD-MRW.</span><span class="sxs-lookup"><span data-stu-id="dccb9-139">Supports flash media, Iomega REV discs, and CD-MRW discs.</span></span>
-   <span data-ttu-id="dccb9-140">Almacena archivos con una longitud inferior a 2 KB en el bloque de entrada del archivo.</span><span class="sxs-lookup"><span data-stu-id="dccb9-140">Stores files less than 2 KB in length in the File Entry block.</span></span>
-   <span data-ttu-id="dccb9-141">Admite archivos de hasta 2 TB con nombres de archivo, con un máximo de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="dccb9-141">Supports files up to 2TB with filenames as long as 255 characters.</span></span>
-   <span data-ttu-id="dccb9-142">Admite un amplio conjunto de atributos de archivo que se adaptan a los distintos sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="dccb9-142">Supports a rich set of file attributes that suit various operating systems.</span></span>
-   <span data-ttu-id="dccb9-143">Admite un formato de puente en el que todos los formatos ISO 9660, Joliet y UDF residan en el mismo disco. Se usa en aplicaciones de vídeo, como DVD-video, DVD + VR y DVD-VR.</span><span class="sxs-lookup"><span data-stu-id="dccb9-143">Supports a bridge format where ISO 9660, Joliet, and UDF formats all reside on the same disc. This is used in video applications, such as DVD-Video, DVD+VR, and DVD-VR.</span></span>
-   <span data-ttu-id="dccb9-144">Admite secuencias con nombre y archivos ' en tiempo real '.</span><span class="sxs-lookup"><span data-stu-id="dccb9-144">Supports named streams and 'Real-Time' files.</span></span>

 

 




