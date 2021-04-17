---
title: La nueva API permite que las aplicaciones envíen sugerencias "recortar y desasignar" a los medios de almacenamiento
description: La nueva API permite que las aplicaciones envíen \ 0034; TRIM y desasignar \ 0034; sugerencias para medios de almacenamiento
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e043c1188bda790b4ed151e8a79e1f7b4c6f0f9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105695774"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a><span data-ttu-id="0dc01-103">La nueva API permite que las aplicaciones envíen sugerencias "recortar y desasignar" a los medios de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="0dc01-103">New API allows apps to send "TRIM and Unmap" hints to storage media</span></span>

## <a name="platforms"></a><span data-ttu-id="0dc01-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="0dc01-104">Platforms</span></span>

<span data-ttu-id="0dc01-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="0dc01-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="0dc01-106">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0dc01-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="0dc01-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0dc01-107">Description</span></span>

<span data-ttu-id="0dc01-108">Las sugerencias de recorte notifican a la unidad que ciertos sectores que anteriormente se asignaron ya no son necesarios para la aplicación y se pueden purgar.</span><span class="sxs-lookup"><span data-stu-id="0dc01-108">TRIM hints notify the drive that certain sectors that previously were allocated are no longer needed by the app and can be purged.</span></span> <span data-ttu-id="0dc01-109">Normalmente se usa cuando una aplicación realiza asignaciones de espacio grande a través de un archivo y, a continuación, administra automáticamente las asignaciones en el archivo (por ejemplo, archivos de disco duro virtual).</span><span class="sxs-lookup"><span data-stu-id="0dc01-109">This is typically used when an app makes large space allocations via a file and then self-manages the allocations to the file (for example, Virtual Hard Disk files).</span></span>

<span data-ttu-id="0dc01-110">**¿Qué es TRIM?**</span><span class="sxs-lookup"><span data-stu-id="0dc01-110">**What is TRIM?**</span></span>

<span data-ttu-id="0dc01-111">Las unidades de estado sólido (SSD) suelen ser dispositivos con bloqueo en bloque basado en memoria Flash. Esto significa que cuando se escriben datos en la SSD, no se puede sobrescribir en su lugar y se deben escribir en otro lugar hasta que el bloque se pueda recolectar como elemento no utilizado.</span><span class="sxs-lookup"><span data-stu-id="0dc01-111">Solid state drives (SSDs) are typically flash memory based block-erased devices; this means that when data is written to the SSD, it cannot be over-written in place and must be written elsewhere until the block can be garbage collected.</span></span> <span data-ttu-id="0dc01-112">Dado que SSD no tiene ningún mecanismo interno para determinar que se han quitado determinados bloques y que se necesitan otros.</span><span class="sxs-lookup"><span data-stu-id="0dc01-112">Since the SSD has no internal mechanism for determining that certain blocks are removed and others are needed.</span></span> <span data-ttu-id="0dc01-113">La única vez que SSD puede marcar un sector como ' sucio ' es cuando está sobrescrito.</span><span class="sxs-lookup"><span data-stu-id="0dc01-113">The only time the SSD can mark a sector ‘dirty’ is when it is over-written.</span></span> <span data-ttu-id="0dc01-114">En otros casos, como cuando se elimina un archivo, el SSD conserva estos sectores, ya que la eliminación se realiza solo como un cambio en la tabla de archivos maestros (MFT) y no como una operación para todos los sectores del archivo.</span><span class="sxs-lookup"><span data-stu-id="0dc01-114">In other cases, such as when a file is deleted, the SSD retains these sectors because the deletion is performed as a master file table (MFT) change only, and not as an operation to all the sectors of the file.</span></span> <span data-ttu-id="0dc01-115">En Windows 7, se presentó una forma estándar de comunicarse con SSD sobre sectores que no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="0dc01-115">In Windows 7, we introduced a standard way of communicating with SSDs about sectors that are not needed any more.</span></span> <span data-ttu-id="0dc01-116">Este comando se define en la [especificación T13](https://www.t13.org/Standards/Default.aspx?DocumentType=3) como el comando Trim. NTFS envía el comando TRIM para algunas operaciones en línea normales, como "DeleteFile".</span><span class="sxs-lookup"><span data-stu-id="0dc01-116">This command is defined in the [T13 specification](https://www.t13.org/Standards/Default.aspx?DocumentType=3) as the TRIM command; NTFS sends the TRIM command for some normal inline operations such as “deletefile.”</span></span>

<span data-ttu-id="0dc01-117">**Otros usos de TRIM en el mundo de almacenamiento**</span><span class="sxs-lookup"><span data-stu-id="0dc01-117">**Other uses of TRIM in the storage world**</span></span>

<span data-ttu-id="0dc01-118">Como las SSD, las redes de área de almacenamiento (San) y las nuevas implementaciones de espacios de software de características de Windows 8 usan sugerencias de comando de recorte para administrar sus espacios en entornos con aprovisionamiento fino.</span><span class="sxs-lookup"><span data-stu-id="0dc01-118">Like SSDs, storage area networks (SANs) and the new Windows 8 feature Software Spaces implementations consume TRIM command hints to manage their spaces in thinly provisioned environments.</span></span> <span data-ttu-id="0dc01-119">Las San y los espacios de software asignan regiones de almacenamiento en tamaños que son mayores que los sectores o clústeres (desde 1 MB a 1 GB).</span><span class="sxs-lookup"><span data-stu-id="0dc01-119">SANs and Software Spaces allocate regions of storage in sizes that are greater than sectors or clusters (anywhere from 1MB to 1GB).</span></span> <span data-ttu-id="0dc01-120">Cuando reciben sugerencias de recorte para su tamaño de asignación (o mayor que el tamaño de asignación), la SAN o SSD puede anular la asignación de una región para liberar espacio para otros archivos.</span><span class="sxs-lookup"><span data-stu-id="0dc01-120">When they receive TRIM hints for its allocation size (or greater than the allocation size), the SAN/SSD can de-allocate a region to free up the space for other files.</span></span> <span data-ttu-id="0dc01-121">Normalmente pasan por todas las sugerencias de recorte al medio subyacente (SSD o HDD) para que puedan consumir el espacio liberado según corresponda.</span><span class="sxs-lookup"><span data-stu-id="0dc01-121">They typically pass through all TRIM hints to the underlying media (SSD or HDD) so that they can consume the freed up space as appropriate.</span></span> <span data-ttu-id="0dc01-122">Normalmente no mueven los datos a las regiones de anulación de asignación, ni realizan un seguimiento de las áreas de recorte a regiones desasignadas (cuando la región está vacía).</span><span class="sxs-lookup"><span data-stu-id="0dc01-122">They do not typically move data around to de-allocate regions, nor do they keep track of TRIM areas to de-allocated regions (when the region is empty).</span></span>

<span data-ttu-id="0dc01-123">Las redes San con aprovisionamiento fino usan las sugerencias de recorte que se les pasan para ayudar a reducir la superficie general de almacenamiento físico, lo que reduce el costo.</span><span class="sxs-lookup"><span data-stu-id="0dc01-123">Thinly provisioned SANs use the TRIM hints that are passed to them to help reduce the overall physical storage footprint, hence reducing cost.</span></span> <span data-ttu-id="0dc01-124">La [especificación de SCSI de T10](https://www.t10.org) define el comando "desasignar" (similar al comando Trim); Aquí el comando es aplicable a todos los tipos de almacenamiento, incluidos HDD, SSD y otros.</span><span class="sxs-lookup"><span data-stu-id="0dc01-124">The [T10 SCSI specification](https://www.t10.org) defines the ‘Unmap’ command (similar to the TRIM command); here the command is applicable to all kinds of storage including HDDs, SSDs, and others.</span></span> <span data-ttu-id="0dc01-125">El comando desasignar ayuda a quitar los bloques físicos de la asignación de la SAN.</span><span class="sxs-lookup"><span data-stu-id="0dc01-125">The UnMap command helps to remove physical blocks from the SAN’s allocation.</span></span>

## <a name="how-to-use-the-new-api"></a><span data-ttu-id="0dc01-126">Cómo usar la nueva API</span><span class="sxs-lookup"><span data-stu-id="0dc01-126">How to use the new API</span></span>


```
#define FSCTL_FILE_LEVEL_TRIM CTL_CODE(FILE_DEVICE_FILE_SYSTEM, 130, METHOD_BUFFERED, FILE_WRITE_DATA)

Where 
typedef struct _EXTENT_PAIR {
    ULONGLONG Offset;
    ULONGLONG Length;
} EXTENT_PAIR, *PEXTENT_PAIR;

typedef struct _FILE_LEVEL_TRIM {
    //
    // A count of how many Offset:Length pairs are given
    //
    DWORD PairCount;
    //
    // All the pairs.
    //
    EXTENT_PAIR Pairs[1];
} FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM;
```



<span data-ttu-id="0dc01-127">El recorte de archivos se pasa a través del búfer si es posible o de forma asincrónica (no almacenada en búfer) al recorte del comando DSM de IOCTL del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0dc01-127">File TRIM is passed via the buffer if possible or asynchronously (non-buffered) to the Device IOCTL DSM command TRIM.</span></span> <span data-ttu-id="0dc01-128">Esto se asigna al comando de recorte para dispositivos ATA y al comando desasociar para dispositivos SCSI.</span><span class="sxs-lookup"><span data-stu-id="0dc01-128">This is mapped to the TRIM command for ATA devices and UnMap command for SCSI devices.</span></span> <span data-ttu-id="0dc01-129">El código de recorte de archivos envía las regiones una por una, tal y como se especifica en las extensiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="0dc01-129">The file TRIM code sends the regions one-by-one as specified by the extents above.</span></span>

<span data-ttu-id="0dc01-130">El recorte de archivos no espera las devoluciones del dispositivo, ya que los comandos de recorte y desasignación se definen como sugerencias para los medios de almacenamiento subyacentes y los códigos de retorno no se esperan.</span><span class="sxs-lookup"><span data-stu-id="0dc01-130">File TRIM does not wait for returns from the device, because the TRIM and Unmap commands are defined as hints to the underlying storage media and return codes are not expected.</span></span>

<span data-ttu-id="0dc01-131">**Flujo de trabajo de un extremo a otro:**</span><span class="sxs-lookup"><span data-stu-id="0dc01-131">**End-to-end workflow:**</span></span>

1.  <span data-ttu-id="0dc01-132">Recorte del archivo de llamadas</span><span class="sxs-lookup"><span data-stu-id="0dc01-132">Call File Trim</span></span>
    1.  <span data-ttu-id="0dc01-133">El recorte de archivos examina las entradas en busca de errores</span><span class="sxs-lookup"><span data-stu-id="0dc01-133">File TRIM examines inputs for errors</span></span>
    2.  <span data-ttu-id="0dc01-134">El recorte de archivos divide las extensiones en regiones de LCN</span><span class="sxs-lookup"><span data-stu-id="0dc01-134">File TRIM breaks up the extents into LCN regions</span></span>
    3.  <span data-ttu-id="0dc01-135">El recorte de archivo se redondea hacia arriba y hacia abajo para las regiones no alineadas que se pasan a TRIM</span><span class="sxs-lookup"><span data-stu-id="0dc01-135">File TRIM rounds up and down for mis-aligned regions that are passed into TRIM</span></span>
    4.  <span data-ttu-id="0dc01-136">El recorte de archivos purga las entradas de la memoria caché que están relacionadas con las áreas de recorte</span><span class="sxs-lookup"><span data-stu-id="0dc01-136">File TRIM purges entries in the cache that relate to the TRIM areas</span></span>
    5.  <span data-ttu-id="0dc01-137">El recorte de archivos supera IOCTL \_ DSM (Trim) por región</span><span class="sxs-lookup"><span data-stu-id="0dc01-137">File TRIM passes IOCTL\_DSM (Trim) per region</span></span>
2.  <span data-ttu-id="0dc01-138">Errores o devoluciones de recorte de archivos</span><span class="sxs-lookup"><span data-stu-id="0dc01-138">File TRIM returns or errors</span></span>
    1.  <span data-ttu-id="0dc01-139">La comprobación de errores se realiza en la validez de la entrada</span><span class="sxs-lookup"><span data-stu-id="0dc01-139">Error checking is done on input validity</span></span>
    2.  <span data-ttu-id="0dc01-140">Si solo algunas de las extensiones son válidas, se devuelve un error para la llamada de API completa</span><span class="sxs-lookup"><span data-stu-id="0dc01-140">If only some of the extents are valid, one error is returned for the complete API call</span></span>

<span data-ttu-id="0dc01-141">**Casos de uso**</span><span class="sxs-lookup"><span data-stu-id="0dc01-141">**Use cases**</span></span>

<span data-ttu-id="0dc01-142">**Disco duro virtual (VHD) de consumidor montado en una SSD:**</span><span class="sxs-lookup"><span data-stu-id="0dc01-142">**Consumer virtual hard disk (VHD) mounted on an SSD:**</span></span>

<span data-ttu-id="0dc01-143">El disco duro virtual se monta inicialmente en un medio sin usar "Clean".</span><span class="sxs-lookup"><span data-stu-id="0dc01-143">The VHD is initially mounted on ‘clean’ unused media.</span></span> <span data-ttu-id="0dc01-144">A medida que se usa el disco duro virtual, el disco duro virtual consume partes de los medios de almacenamiento para los archivos, etc. Cuando elimina archivos en el medio de almacenamiento, estos archivos no se quitan de la SSD, ya que el disco duro virtual completo se almacena como un archivo en la SSD.</span><span class="sxs-lookup"><span data-stu-id="0dc01-144">As the VHD is used, the VHD consumes parts of the storage media for files, etc. When it deletes files in the storage media, these files are not removed from the SSD since the complete VHD is stored as one file on the SSD.</span></span> <span data-ttu-id="0dc01-145">El entorno de Hyper-V llama al recorte de archivos para todas las regiones que se eliminan cuando se produce delete-file en el entorno de VHD.</span><span class="sxs-lookup"><span data-stu-id="0dc01-145">The Hyper-V environment calls File TRIM for all regions that are deleted when delete-file occurs in the VHD environment.</span></span> <span data-ttu-id="0dc01-146">Los \_ recortes de archivo se traducen a la SSD para que se pueda optimizar el rendimiento de SSD.</span><span class="sxs-lookup"><span data-stu-id="0dc01-146">The File\_TRIMs are translated to the SSD so that the SSD performance can be optimized.</span></span>

<span data-ttu-id="0dc01-147">**VHD de consumidor montado en una SAN con aprovisionamiento fino:**</span><span class="sxs-lookup"><span data-stu-id="0dc01-147">**Consumer VHD mounted on a thinly provisioned SAN:**</span></span>

<span data-ttu-id="0dc01-148">El disco duro virtual se monta inicialmente en una losa mínima de un entorno con aprovisionamiento fino.</span><span class="sxs-lookup"><span data-stu-id="0dc01-148">The VHD is initially mounted on one minimum slab of a thinly provisioned environment.</span></span> <span data-ttu-id="0dc01-149">A medida que los archivos se almacenan en el disco duro virtual, la superficie de almacenamiento del disco duro virtual crece en múltiplos de bloques.</span><span class="sxs-lookup"><span data-stu-id="0dc01-149">As files are stored in the VHD, the storage footprint of the VHD grows in multiples of slabs.</span></span> <span data-ttu-id="0dc01-150">Cuando se quitan archivos en el disco duro virtual, Hyper-V llama al recorte de archivos en \_ la red San de aprovisionamiento fino subyacente.</span><span class="sxs-lookup"><span data-stu-id="0dc01-150">When files are removed in the VHD, the Hyper-V calls File\_TRIM to the underlying thinly provisioned SAN.</span></span> <span data-ttu-id="0dc01-151">Si los recortes son mayores que la granularidad de los bloques, la SAN puede quitar ahora una losa y, por tanto, reducir la superficie del VHD en esa SAN.</span><span class="sxs-lookup"><span data-stu-id="0dc01-151">If the TRIMs are bigger than the SLAB granularity, the SAN can now remove a SLAB and hence reduce the footprint of the VHD on that SAN.</span></span>

<span data-ttu-id="0dc01-152">Si el disco duro virtual reside en un servidor basado en Windows 8, el optimizador de almacenamiento también enviará recortes para reducir la superficie de la losa del VHD desde el VHD montado.</span><span class="sxs-lookup"><span data-stu-id="0dc01-152">If the VHD is resident on a Windows 8 based server, the Storage Optimizer will also send TRIMs to reduce the slab footprint of the VHD from within the mounted VHD.</span></span>

## <a name="tests"></a><span data-ttu-id="0dc01-153">Pruebas</span><span class="sxs-lookup"><span data-stu-id="0dc01-153">Tests</span></span>

<span data-ttu-id="0dc01-154">No hay ninguna API comparable en las versiones anteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0dc01-154">There are no comparable APIs in earlier operating system releases.</span></span> <span data-ttu-id="0dc01-155">No debería haber ningún impacto en el rendimiento de la propia API real, aunque el medio de almacenamiento (si se implementa correctamente) puede mostrar un mejor rendimiento de escritura.</span><span class="sxs-lookup"><span data-stu-id="0dc01-155">There should be no performance impact from the actual API itself, though the storage media (if implemented correctly) can show better write performance.</span></span> <span data-ttu-id="0dc01-156">La API debe usarse con sumo cuidado; solo se deben pasar las extensiones que ya no sean necesarias, ya que esas extensiones se quitarán permanentemente de los medios de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="0dc01-156">The API should be used very carefully; only extents that are no longer needed should be passed down as those extents will be permanently removed from the storage media.</span></span>

## <a name="resources"></a><span data-ttu-id="0dc01-157">Recursos</span><span class="sxs-lookup"><span data-stu-id="0dc01-157">Resources</span></span>

-   [<span data-ttu-id="0dc01-158">Especificación de T13</span><span class="sxs-lookup"><span data-stu-id="0dc01-158">T13 specification</span></span>](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [<span data-ttu-id="0dc01-159">Especificación de SCSI de T10</span><span class="sxs-lookup"><span data-stu-id="0dc01-159">T10 SCSI specification</span></span>](https://www.t10.org/)

 

 




