---
title: Distribución de la multisesión de IMAPi
description: IMAPi proporciona a los desarrolladores de aplicaciones la capacidad de crear imágenes del sistema de archivos ISO 9660 y UDF y grabarlas en CD, DVD y Blu-Ray \ 8482; medios ópticos.
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2581672fac78d23a0d2f4e2bc36ee4227adbca1d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104566311"
---
# <a name="imapi-multisession-layout"></a><span data-ttu-id="a9174-103">Distribución de la multisesión de IMAPi</span><span class="sxs-lookup"><span data-stu-id="a9174-103">IMAPI Multisession Layout</span></span>

<span data-ttu-id="a9174-104">IMAPi proporciona a los desarrolladores de aplicaciones la capacidad de crear imágenes del sistema de archivos ISO 9660 y UDF y grabarlas en medios ópticos de CD, DVD y Blu-Ray™.</span><span class="sxs-lookup"><span data-stu-id="a9174-104">IMAPI provides application developers with the ability to create ISO 9660 and UDF file system images and burn them onto CD, DVD and Blu-Ray™ optical media.</span></span> <span data-ttu-id="a9174-105">Con Windows 7, IMAPi proporciona compatibilidad adicional para la grabación de múltiples sesiones en DVD y Blu-Ray™ medios regrabables.</span><span class="sxs-lookup"><span data-stu-id="a9174-105">With Windows 7, IMAPI provides additional support for multisession burning on DVD and Blu-Ray™ rewritable media.</span></span>

<span data-ttu-id="a9174-106">La siguiente documentación detalla el diseño del disco que IMAPi emplea para implementar la multisesión.</span><span class="sxs-lookup"><span data-stu-id="a9174-106">The following documentation details the disc layout that IMAPI utilizes to implement multisession.</span></span> <span data-ttu-id="a9174-107">Esta información debe usarse para garantizar la interoperabilidad entre IMAPi y otro software de grabación, además de permitir que los desarrolladores de este software creen imágenes de disco de múltiples sesiones compatibles con IMAPi.</span><span class="sxs-lookup"><span data-stu-id="a9174-107">This information should be used to ensure interoperability between IMAPI and other burning software as well as allow the developers of this software to create IMAPI-compatible multisession disc images.</span></span>

> [!Note]  
> <span data-ttu-id="a9174-108">Para ver un ejemplo en el que se detalla la creación de un disco de múltiples sesiones, consulte [creación de un disco de múltiples sesiones](creating-a-multisession-disc.md).</span><span class="sxs-lookup"><span data-stu-id="a9174-108">For an example detailing the creation of a multisession disc, see [Creating a Multisession Disc](creating-a-multisession-disc.md).</span></span>

 

## <a name="multisession-on-sequential-media"></a><span data-ttu-id="a9174-109">Multisesión en medios secuenciales</span><span class="sxs-lookup"><span data-stu-id="a9174-109">Multisession on Sequential Media</span></span>

<span data-ttu-id="a9174-110">La implementación de IMAPi de multisesión en medios secuenciales se admite para su uso con los medios CD-R, CD-RW, DVD-R, DVD + R y Blu-Ray™.</span><span class="sxs-lookup"><span data-stu-id="a9174-110">The IMAPI implementation of multisession on sequential media is supported for use with CD-R, CD-RW, DVD-R, DVD+R and Blu-Ray™ media.</span></span> <span data-ttu-id="a9174-111">IMAPi usa el modo de grabación de sesión a la vez para CD-RW y, como resultado, en este escenario, el formato se considera un tipo de medio secuencial.</span><span class="sxs-lookup"><span data-stu-id="a9174-111">IMAPI uses the Session-At-Once recording mode for CD-RW, and as a result, in this scenario, the format is considered a sequential media type.</span></span>

<span data-ttu-id="a9174-112">En un escenario en el que se usa la multisesión en medios secuenciales con UDF, IMAPi escribe las estructuras de delimitador (delimitador de volumen del delimitador UDF-AVDP), las estructuras de volumen (UDF del descriptor de volumen de UDF) y las estructuras de metadatos del sistema de archivos (archivo UDF Set descriptor-FSD) al principio de</span><span class="sxs-lookup"><span data-stu-id="a9174-112">In a scenario involving multisession on sequential media using UDF, IMAPI writes out the anchor structures (UDF Anchor Volume Descriptor Pointer - AVDP), volume structures (UDF Volume Descriptor Sequence - VDS) , and the file system metadata structures (UDF File Set Descriptor - FSD) at the start of every new session as outlined in the following diagram:</span></span>

![Diagrama que muestra la estructura de metadatos del sistema de archivos con el punto de montaje ' Import/F S ' indicado con una flecha roja en el ' delimitador ' de la sesión física 2.](images/multises1.png)

> [!Note]  
> <span data-ttu-id="a9174-114">En esta ilustración se muestra el diseño del disco IMAPi cuando se usa la UDF 2,50 con metadatos redundantes.</span><span class="sxs-lookup"><span data-stu-id="a9174-114">This figure illustrates the IMAPI disc layout when using UDF 2.50 with redundant metadata.</span></span>

 

<span data-ttu-id="a9174-115">Los datos almacenados en medios grabados secuencialmente se componen de varias sesiones físicas.</span><span class="sxs-lookup"><span data-stu-id="a9174-115">The data stored on sequentially recorded media consists of a number of physical sessions.</span></span> <span data-ttu-id="a9174-116">Cada sesión contiene un sistema de archivos completo que representa los datos de usuario como un conjunto de archivos organizados en directorios.</span><span class="sxs-lookup"><span data-stu-id="a9174-116">Each session contains a complete file system representing user data as a set of files organized in directories.</span></span> <span data-ttu-id="a9174-117">Los metadatos del sistema de archivos se componen de varias estructuras de datos organizadas jerárquicamente.</span><span class="sxs-lookup"><span data-stu-id="a9174-117">The file system metadata consists of a number of hierarchically organized data structures.</span></span> <span data-ttu-id="a9174-118">En la parte superior de la jerarquía, se encuentran las estructuras de delimitador (AVDP) ubicadas en direcciones de bloques lógicos predefinidas (LBAs).</span><span class="sxs-lookup"><span data-stu-id="a9174-118">At the top of the hierarchy reside anchor structures (AVDP) located at pre-defined Logical Block Addresses (LBAs).</span></span> <span data-ttu-id="a9174-119">Las estructuras de delimitador especifican las ubicaciones de las siguientes estructuras de nivel que no tienen direcciones predefinidas.</span><span class="sxs-lookup"><span data-stu-id="a9174-119">The anchor structures specify the locations of the next level structures which do not have predefined addresses.</span></span> <span data-ttu-id="a9174-120">El siguiente nivel de jerarquía después de las estructuras de delimitador contiene las estructuras de volumen (VDS) que describen las propiedades del volumen y hacen referencia a las estructuras de metadatos del sistema de archivos (FSD), que a su vez describen archivos y directorios individuales.</span><span class="sxs-lookup"><span data-stu-id="a9174-120">The next level of hierarchy after anchor structures contains the volume structures (VDS) that describe the properties of the volume and referencing the file system metadata structures (FSD), which in turn describe individual files and directories.</span></span>

## <a name="multisession-on-rewritable-media"></a><span data-ttu-id="a9174-121">Multisesión en medios regrabables</span><span class="sxs-lookup"><span data-stu-id="a9174-121">Multisession on Rewritable Media</span></span>

<span data-ttu-id="a9174-122">El enfoque para los medios secuenciales descritos en la sección anterior es incompatible con los medios regrabables (no secuenciales).</span><span class="sxs-lookup"><span data-stu-id="a9174-122">The approach for sequential media outlined in the previous section is incompatible with rewritable (non-sequential) media.</span></span> <span data-ttu-id="a9174-123">Estos formatos de medios incluyen DVD-RW, DVD + RW, DVD-RAM, Blu-Ray™ reescribible y otros medios de escritura aleatorios, como discos de REV Iomega.</span><span class="sxs-lookup"><span data-stu-id="a9174-123">These media formats include DVD-RW, DVD+RW, DVD-RAM, Blu-Ray™ rewritable and other random writable media, such as Iomega REV disks.</span></span> <span data-ttu-id="a9174-124">Los medios regrabables no admiten el concepto de sesiones físicas correspondientes a las sesiones lógicas, que son incrementos individuales confirmados por una aplicación de maestro.</span><span class="sxs-lookup"><span data-stu-id="a9174-124">Rewritable media does not support the concept of physical sessions corresponding to logical sessions, which are individual increments committed by a mastering application.</span></span> <span data-ttu-id="a9174-125">Solo se expone una única sesión física, que es un área que empieza al principio del disco que representa el área completa que tiene la posibilidad de contener varias sesiones lógicas.</span><span class="sxs-lookup"><span data-stu-id="a9174-125">Only a single physical session is exposed, which is an area starting at the beginning of the disc representing the entire addressable area that has the potential to contain multiple logical sessions.</span></span>

> [!Note]  
> <span data-ttu-id="a9174-126">Aunque DVD-RW es una excepción en que admite el concepto de una sesión física en el modo secuencial, esta funcionalidad no es compatible actualmente con IMAPi.</span><span class="sxs-lookup"><span data-stu-id="a9174-126">While DVD-RW is an exception in that it supports the concept of a physical session in the Sequential mode, this capability is currently not supported by IMAPI.</span></span>

 

<span data-ttu-id="a9174-127">Para solucionar la falta de una asignación de uno a uno entre sesiones físicas y lógicas en formatos regrabables, IMAPi actualiza selectivamente las estructuras de delimitador (AVDP) en la *primera* sesión lógica para apuntar a las nuevas estructuras de volumen (VDS) y a las estructuras de metadatos del sistema de archivos (FSD) al principio de la *última* sesión lógica, como se describe en</span><span class="sxs-lookup"><span data-stu-id="a9174-127">To address the lack of one-to-one mapping between physical and logical sessions on rewritable formats, IMAPI selectively updates the anchor structures (AVDP) in the *first* logical session to point to the new volume structures (VDS) and file system metadata structures (FSD) at the beginning of the *last* logical session as outlined in the following diagram:</span></span>

![Diagrama que muestra la estructura de metadatos del sistema de archivos con el punto de montaje ' Import/F S ' indicado con una flecha roja en el ' delimitador ' de la sesión lógica 1.](images/multises2.png)

> [!Note]  
> <span data-ttu-id="a9174-129">En esta ilustración se muestra el diseño del disco IMAPi cuando se usa la UDF 2,50 con metadatos redundantes.</span><span class="sxs-lookup"><span data-stu-id="a9174-129">This figure illustrates the IMAPI disc layout when using UDF 2.50 with redundant metadata.</span></span>

 

<span data-ttu-id="a9174-130">Al agregar una nueva sesión lógica a un disco regrabable, IMAPi primero determina el final de la última sesión lógica mediante el análisis de los metadatos del volumen (VDS).</span><span class="sxs-lookup"><span data-stu-id="a9174-130">When adding a new logical session to a rewritable disc, IMAPI first determines the end of the last logical session by analyzing the volume metadata (VDS).</span></span> <span data-ttu-id="a9174-131">A continuación, IMAPi agrega la nueva sesión lógica, completa con las nuevas estructuras de delimitador (AVDP), volumen (VDS) y de metadatos del sistema de archivos (FSD), contiguas físicamente con la sesión lógica registrada previamente.</span><span class="sxs-lookup"><span data-stu-id="a9174-131">IMAPI then adds the new logical session, complete with new anchor (AVDP), volume (VDS) and file system metadata structures (FSD), physically contiguous with the previously recorded logical session.</span></span> <span data-ttu-id="a9174-132">El último paso requiere que se actualicen las estructuras de delimitador (AVDP) al principio de la primera sesión lógica para que apunten a las estructuras de volumen (VDS) en la *nueva* sesión lógica.</span><span class="sxs-lookup"><span data-stu-id="a9174-132">The final step requires that the anchor structures (AVDP) at the beginning of the first logical session are updated to point to the volume structures (VDS) in the *new* logical session.</span></span> <span data-ttu-id="a9174-133">El resultado operativo es el mismo que con los medios secuenciales.</span><span class="sxs-lookup"><span data-stu-id="a9174-133">The operational result is the same as with sequential media.</span></span>

## <a name="additional-recommendations"></a><span data-ttu-id="a9174-134">Recomendaciones adicionales</span><span class="sxs-lookup"><span data-stu-id="a9174-134">Additional Recommendations</span></span>

-   <span data-ttu-id="a9174-135">**Diseño de partición**</span><span class="sxs-lookup"><span data-stu-id="a9174-135">**Partition Layout**</span></span>

    <span data-ttu-id="a9174-136">Para lograr la compatibilidad con IMAPi, se recomienda que los desarrolladores de software de grabación de terceros usen los diseños de disco descritos en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="a9174-136">To achieve IMAPI compatiblity, it is recommended that third-party burning software developers use the disc layouts outlined in this documentation.</span></span> <span data-ttu-id="a9174-137">Los desarrolladores deben evitar los diseños con particiones del sistema de archivos que ocupen todo el disco, ya que esto requiere la grabación de las aplicaciones para localizar espacio disponible en las particiones existentes siempre que sea necesario anexar datos al disco. A menudo, las aplicaciones de grabación logran esto mediante el uso de marcadores propietarios en el disco para indicar cuánto espacio ocupa realmente los datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="a9174-137">Developers should avoid layouts with file system partitions occupying the entire disc, as this requires recording applications to locate free space within existing partitions whenever data needs to be appended to the disc. Oftentimes, the recording applications accomplish this by utilizing proprietary markers on the disc to indicate how much space is actually occupied by user data.</span></span> <span data-ttu-id="a9174-138">Estos diseños de disco son incompatibles con IMAPi, ya que los marcadores propietarios no se reconocen fuera de la aplicación para la que se crearon.</span><span class="sxs-lookup"><span data-stu-id="a9174-138">Such disc layouts are incompatible with IMAPI as the proprietary markers are not recognized outside of the application they were created for.</span></span>

-   <span data-ttu-id="a9174-139">**Tipo de partición UDF**</span><span class="sxs-lookup"><span data-stu-id="a9174-139">**UDF Partition Type**</span></span>

    <span data-ttu-id="a9174-140">IMAPi usa el tipo de partición UDF de **solo lectura** en su implementación de multisesión en medios regrabables.</span><span class="sxs-lookup"><span data-stu-id="a9174-140">IMAPI uses the **Read-Only** UDF partition type in its implementation of multisession on rewritable media.</span></span> <span data-ttu-id="a9174-141">Los desarrolladores de software de grabación de terceros deben usar el tipo de partición UDF de **solo lectura** para lograr la compatibilidad con la grabación con registro maestro de Windows a través de IMAPI.</span><span class="sxs-lookup"><span data-stu-id="a9174-141">Developers of third-party burning software should use the **Read-Only** UDF partition type to achieve compatiblity with Windows mastered burning via IMAPI.</span></span> <span data-ttu-id="a9174-142">Si se usa otro tipo de partición UDF, como **reescritura** , IMAPI no puede proporcionar compatibilidad con la creación de patrones.</span><span class="sxs-lookup"><span data-stu-id="a9174-142">If another UDF partition type such as **Rewritable** is used, IMAPI cannot provide mastering support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9174-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9174-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9174-144">Creación de un disco de múltiples sesiones</span><span class="sxs-lookup"><span data-stu-id="a9174-144">Creating a Multisession Disc</span></span>](creating-a-multisession-disc.md)
</dt> <dt>

[<span data-ttu-id="a9174-145">**IMultisessionRandomWrite**</span><span class="sxs-lookup"><span data-stu-id="a9174-145">**IMultisessionRandomWrite**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




