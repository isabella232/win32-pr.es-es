---
description: La tabla de archivos maestros (MFT) almacena la información necesaria para recuperar archivos de una partición NTFS.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Tabla de archivos maestros (notas del desarrollador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae8656a44b6dadd7d4ff601ddc64623935f5881
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998091"
---
# <a name="master-file-table"></a><span data-ttu-id="18d86-103">Tabla de archivos maestros</span><span class="sxs-lookup"><span data-stu-id="18d86-103">Master File Table</span></span>

<span data-ttu-id="18d86-104">\[Este documento solo se aplica a la versión 3 de los volúmenes NTFS.\]</span><span class="sxs-lookup"><span data-stu-id="18d86-104">\[This document applies only to version 3 of NTFS volumes.\]</span></span>

<span data-ttu-id="18d86-105">La tabla de archivos maestros (MFT) almacena la información necesaria para recuperar archivos de una partición NTFS.</span><span class="sxs-lookup"><span data-stu-id="18d86-105">The master file table (MFT) stores the information required to retrieve files from an NTFS partition.</span></span>

<span data-ttu-id="18d86-106">Un archivo puede tener uno o más registros MFT y puede contener uno o más atributos.</span><span class="sxs-lookup"><span data-stu-id="18d86-106">A file may have one or more MFT records, and can contain one or more attributes.</span></span> <span data-ttu-id="18d86-107">En NTFS, una referencia de archivo es la referencia de segmento MFT del registro de archivo base.</span><span class="sxs-lookup"><span data-stu-id="18d86-107">In NTFS, a file reference is the MFT segment reference of the base file record.</span></span> <span data-ttu-id="18d86-108">Para obtener más información, [**consulte \_ \_ referencia de segmentos de MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="18d86-108">For more information, see [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

<span data-ttu-id="18d86-109">La MFT contiene segmentos de registro de archivos; los primeros 16 están reservados para archivos especiales, como los siguientes:</span><span class="sxs-lookup"><span data-stu-id="18d86-109">The MFT contains file record segments; the first 16 of these are reserved for special files, such as the following:</span></span>

-   <span data-ttu-id="18d86-110">0: MFT ($Mft)</span><span class="sxs-lookup"><span data-stu-id="18d86-110">0: MFT ($Mft)</span></span>
-   <span data-ttu-id="18d86-111">5: directorio raíz ( \\ )</span><span class="sxs-lookup"><span data-stu-id="18d86-111">5: root directory (\\)</span></span>
-   <span data-ttu-id="18d86-112">6: archivo de asignación de clúster de volumen ($Bitmap)</span><span class="sxs-lookup"><span data-stu-id="18d86-112">6: volume cluster allocation file ($Bitmap)</span></span>
-   <span data-ttu-id="18d86-113">8: archivo de clúster incorrecto ($BadClus)</span><span class="sxs-lookup"><span data-stu-id="18d86-113">8: bad-cluster file ($BadClus)</span></span>

<span data-ttu-id="18d86-114">Cada segmento de registro de archivo comienza con un encabezado de segmento de registro de archivo.</span><span class="sxs-lookup"><span data-stu-id="18d86-114">Each file record segment starts with a file record segment header.</span></span> <span data-ttu-id="18d86-115">Para obtener más información, [**consulte \_ \_ \_ encabezado de segmento de registro de archivo**](file-record-segment-header.md).</span><span class="sxs-lookup"><span data-stu-id="18d86-115">For more information, see [**FILE\_RECORD\_SEGMENT\_HEADER**](file-record-segment-header.md).</span></span> <span data-ttu-id="18d86-116">Cada segmento de registro de archivo va seguido de uno o varios atributos.</span><span class="sxs-lookup"><span data-stu-id="18d86-116">Each file record segment is followed by one or more attributes.</span></span> <span data-ttu-id="18d86-117">Cada atributo comienza con un encabezado de registro de atributo.</span><span class="sxs-lookup"><span data-stu-id="18d86-117">Each attribute starts with an attribute record header.</span></span> <span data-ttu-id="18d86-118">Para obtener más información, consulte [**Attribute \_ Record \_ Header**](attribute-record-header.md).</span><span class="sxs-lookup"><span data-stu-id="18d86-118">For more information, see [**ATTRIBUTE\_RECORD\_HEADER**](attribute-record-header.md).</span></span> <span data-ttu-id="18d86-119">El registro del atributo incluye el tipo de atributo (como $DATA o $BITMAP), un nombre opcional y el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="18d86-119">The attribute record includes the attribute type (such as $DATA or $BITMAP), an optional name, and the attribute value.</span></span> <span data-ttu-id="18d86-120">El flujo de datos de usuario es un atributo, al igual que todos los flujos.</span><span class="sxs-lookup"><span data-stu-id="18d86-120">The user data stream is an attribute, as are all streams.</span></span> <span data-ttu-id="18d86-121">La lista de atributos finaliza con 0xFFFFFFFF ($END).</span><span class="sxs-lookup"><span data-stu-id="18d86-121">The attribute list is terminated with 0xFFFFFFFF ($END).</span></span>

<span data-ttu-id="18d86-122">A continuación se muestran algunos atributos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="18d86-122">The following are some example attributes.</span></span>

-   <span data-ttu-id="18d86-123">El archivo de $Mft contiene un atributo de $DATA sin nombre que es la secuencia de segmentos de registro de MFT, en orden.</span><span class="sxs-lookup"><span data-stu-id="18d86-123">The $Mft file contains an unnamed $DATA attribute that is the sequence of MFT record segments, in order.</span></span>
-   <span data-ttu-id="18d86-124">El archivo de $Mft contiene un atributo de $BITMAP sin nombre que indica qué registros de MFT están en uso.</span><span class="sxs-lookup"><span data-stu-id="18d86-124">The $Mft file contains an unnamed $BITMAP attribute that indicates which MFT records are in use.</span></span>
-   <span data-ttu-id="18d86-125">El archivo de $Bitmap contiene un atributo de $DATA sin nombre que indica qué clústeres están en uso.</span><span class="sxs-lookup"><span data-stu-id="18d86-125">The $Bitmap file contains an unnamed $DATA attribute that indicates which clusters are in use.</span></span>
-   <span data-ttu-id="18d86-126">El archivo de $BadClus contiene un atributo de $DATA denominado $BAD que contiene una entrada que corresponde a cada clúster incorrecto.</span><span class="sxs-lookup"><span data-stu-id="18d86-126">The $BadClus file contains a $DATA attribute named $BAD that contains an entry that corresponds to each bad cluster.</span></span>

<span data-ttu-id="18d86-127">Cuando no hay más espacio para almacenar los atributos en el segmento de registro de archivo, los segmentos de registro de archivos adicionales se asignan y se insertan en el primer segmento de registro de archivo (o base) en un atributo denominado lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="18d86-127">When there is no more space for storing attributes in the file record segment, additional file record segments are allocated and inserted in the first (or base) file record segment in an attribute called the attribute list.</span></span> <span data-ttu-id="18d86-128">La lista de atributos indica dónde se puede encontrar cada atributo asociado al archivo.</span><span class="sxs-lookup"><span data-stu-id="18d86-128">The attribute list indicates where each attribute associated with the file can be found.</span></span> <span data-ttu-id="18d86-129">Esto incluye todos los atributos del registro de archivo base, excepto la propia lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="18d86-129">This includes all attributes in the base file record, except for the attribute list itself.</span></span> <span data-ttu-id="18d86-130">Para obtener más información, [**consulte \_ \_ entrada**](attribute-list-entry.md)de la lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="18d86-130">For more information, see [**ATTRIBUTE\_LIST\_ENTRY**](attribute-list-entry.md).</span></span>

<span data-ttu-id="18d86-131">Entre las estructuras relacionadas con MFT se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="18d86-131">Structures related to the MFT include the following:</span></span>

-   [<span data-ttu-id="18d86-132">**\_entrada de lista de atributos \_**</span><span class="sxs-lookup"><span data-stu-id="18d86-132">**ATTRIBUTE\_LIST\_ENTRY**</span></span>](attribute-list-entry.md)
-   [<span data-ttu-id="18d86-133">**\_encabezado de registro de atributo \_**</span><span class="sxs-lookup"><span data-stu-id="18d86-133">**ATTRIBUTE\_RECORD\_HEADER**</span></span>](attribute-record-header.md)
-   [<span data-ttu-id="18d86-134">**nombre de archivo \_**</span><span class="sxs-lookup"><span data-stu-id="18d86-134">**FILE\_NAME**</span></span>](file-name.md)
-   [<span data-ttu-id="18d86-135">**\_encabezado de \_ segmento de registro de archivo \_**</span><span class="sxs-lookup"><span data-stu-id="18d86-135">**FILE\_RECORD\_SEGMENT\_HEADER**</span></span>](file-record-segment-header.md)
-   [<span data-ttu-id="18d86-136">**\_referencia de segmento de MFT \_**</span><span class="sxs-lookup"><span data-stu-id="18d86-136">**MFT\_SEGMENT\_REFERENCE**</span></span>](mft-segment-reference.md)
-   [<span data-ttu-id="18d86-137">**encabezado de varios \_ sectores \_**</span><span class="sxs-lookup"><span data-stu-id="18d86-137">**MULTI\_SECTOR\_HEADER**</span></span>](multi-sector-header.md)
-   [<span data-ttu-id="18d86-138">**\_información estándar**</span><span class="sxs-lookup"><span data-stu-id="18d86-138">**STANDARD\_INFORMATION**</span></span>](standard-information.md)

## <a name="related-topics"></a><span data-ttu-id="18d86-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="18d86-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="18d86-140">[Referencia técnica de NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="18d86-140">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

 
