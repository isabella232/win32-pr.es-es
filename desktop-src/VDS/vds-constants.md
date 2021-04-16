---
description: Constantes de VDS
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: Constantes de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9979cd4416b5305c61f6275612422b1f4cfe43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678384"
---
# <a name="vds-constants"></a><span data-ttu-id="cfbdc-103">Constantes de VDS</span><span class="sxs-lookup"><span data-stu-id="cfbdc-103">VDS Constants</span></span>

<span data-ttu-id="cfbdc-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cfbdc-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="cfbdc-105">Las constantes de VDS se clasifican como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="cfbdc-105">VDS constants are categorized as follows:</span></span>

-   [<span data-ttu-id="cfbdc-106">Constantes de estado de objetos</span><span class="sxs-lookup"><span data-stu-id="cfbdc-106">Object Status Constants</span></span>](#object-status-constants)
-   [<span data-ttu-id="cfbdc-107">Constantes de sugerencias de automagic</span><span class="sxs-lookup"><span data-stu-id="cfbdc-107">Automagic Hints Constants</span></span>](#automagic-hints-constants)
-   [<span data-ttu-id="cfbdc-108">Constantes misceláneas</span><span class="sxs-lookup"><span data-stu-id="cfbdc-108">Miscellaneous Constants</span></span>](#miscellaneous-constants)

### <a name="object-status-constants"></a><span data-ttu-id="cfbdc-109">Constantes de estado de objetos</span><span class="sxs-lookup"><span data-stu-id="cfbdc-109">Object Status Constants</span></span>



| <span data-ttu-id="cfbdc-110">Constante</span><span class="sxs-lookup"><span data-stu-id="cfbdc-110">Constant</span></span>           | <span data-ttu-id="cfbdc-111">Value</span><span class="sxs-lookup"><span data-stu-id="cfbdc-111">Value</span></span> |
|--------------------|-------|
| <span data-ttu-id="cfbdc-112">ESTADO \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="cfbdc-112">STATUS\_UNKNOWN</span></span>    | <span data-ttu-id="cfbdc-113">0</span><span class="sxs-lookup"><span data-stu-id="cfbdc-113">0</span></span>     |
| <span data-ttu-id="cfbdc-114">ESTADO \_ en línea</span><span class="sxs-lookup"><span data-stu-id="cfbdc-114">STATUS\_ONLINE</span></span>     | <span data-ttu-id="cfbdc-115">1</span><span class="sxs-lookup"><span data-stu-id="cfbdc-115">1</span></span>     |
| <span data-ttu-id="cfbdc-116">ESTADO \_ no \_ listo</span><span class="sxs-lookup"><span data-stu-id="cfbdc-116">STATUS\_NOT\_READY</span></span> | <span data-ttu-id="cfbdc-117">2</span><span class="sxs-lookup"><span data-stu-id="cfbdc-117">2</span></span>     |
| <span data-ttu-id="cfbdc-118">ESTADO \_ sin \_ medios</span><span class="sxs-lookup"><span data-stu-id="cfbdc-118">STATUS\_NO\_MEDIA</span></span>  | <span data-ttu-id="cfbdc-119">3</span><span class="sxs-lookup"><span data-stu-id="cfbdc-119">3</span></span>     |
| <span data-ttu-id="cfbdc-120">ESTADO \_ sin conexión</span><span class="sxs-lookup"><span data-stu-id="cfbdc-120">STATUS\_OFFLINE</span></span>    | <span data-ttu-id="cfbdc-121">4</span><span class="sxs-lookup"><span data-stu-id="cfbdc-121">4</span></span>     |
| <span data-ttu-id="cfbdc-122">error de estado \_</span><span class="sxs-lookup"><span data-stu-id="cfbdc-122">STATUS\_FAILED</span></span>     | <span data-ttu-id="cfbdc-123">5</span><span class="sxs-lookup"><span data-stu-id="cfbdc-123">5</span></span>     |
| <span data-ttu-id="cfbdc-124">falta el estado \_</span><span class="sxs-lookup"><span data-stu-id="cfbdc-124">STATUS\_MISSING</span></span>    | <span data-ttu-id="cfbdc-125">6</span><span class="sxs-lookup"><span data-stu-id="cfbdc-125">6</span></span>     |



 

### <a name="automagic-hints-constants"></a><span data-ttu-id="cfbdc-126">Constantes de sugerencias de automagic</span><span class="sxs-lookup"><span data-stu-id="cfbdc-126">Automagic Hints Constants</span></span>



| <span data-ttu-id="cfbdc-127">Constante</span><span class="sxs-lookup"><span data-stu-id="cfbdc-127">Constant</span></span>                               | <span data-ttu-id="cfbdc-128">Value</span><span class="sxs-lookup"><span data-stu-id="cfbdc-128">Value</span></span>   |
|----------------------------------------|---------|
| <span data-ttu-id="cfbdc-129">sugerencia de VDS \_ \_ MOSTLYREADS</span><span class="sxs-lookup"><span data-stu-id="cfbdc-129">VDS\_HINT\_MOSTLYREADS</span></span>                 | <span data-ttu-id="cfbdc-130">0x0002L</span><span class="sxs-lookup"><span data-stu-id="cfbdc-130">0x0002L</span></span> |
| <span data-ttu-id="cfbdc-131">sugerencia de VDS \_ \_ OPTIMIZEFORSEQUENTIALREADS</span><span class="sxs-lookup"><span data-stu-id="cfbdc-131">VDS\_HINT\_OPTIMIZEFORSEQUENTIALREADS</span></span>  | <span data-ttu-id="cfbdc-132">0x0004L</span><span class="sxs-lookup"><span data-stu-id="cfbdc-132">0x0004L</span></span> |
| <span data-ttu-id="cfbdc-133">sugerencia de VDS \_ \_ OPTIMIZEFORSEQUENTIALWRITES</span><span class="sxs-lookup"><span data-stu-id="cfbdc-133">VDS\_HINT\_OPTIMIZEFORSEQUENTIALWRITES</span></span> | <span data-ttu-id="cfbdc-134">0x0008L</span><span class="sxs-lookup"><span data-stu-id="cfbdc-134">0x0008L</span></span> |
| <span data-ttu-id="cfbdc-135">sugerencia de VDS \_ \_ REMAPENABLED</span><span class="sxs-lookup"><span data-stu-id="cfbdc-135">VDS\_HINT\_REMAPENABLED</span></span>                | <span data-ttu-id="cfbdc-136">0x0020L</span><span class="sxs-lookup"><span data-stu-id="cfbdc-136">0x0020L</span></span> |
| <span data-ttu-id="cfbdc-137">sugerencia de VDS \_ \_ WRITETHROUGHCACHINGENABLED</span><span class="sxs-lookup"><span data-stu-id="cfbdc-137">VDS\_HINT\_WRITETHROUGHCACHINGENABLED</span></span>  | <span data-ttu-id="cfbdc-138">0x0040L</span><span class="sxs-lookup"><span data-stu-id="cfbdc-138">0x0040L</span></span> |
| <span data-ttu-id="cfbdc-139">sugerencia de VDS \_ \_ HARDWARECHECKSUMENABLED</span><span class="sxs-lookup"><span data-stu-id="cfbdc-139">VDS\_HINT\_HARDWARECHECKSUMENABLED</span></span>     | <span data-ttu-id="cfbdc-140">0x0080L</span><span class="sxs-lookup"><span data-stu-id="cfbdc-140">0x0080L</span></span> |
| <span data-ttu-id="cfbdc-141">sugerencia de VDS \_ \_ ISYANKABLE</span><span class="sxs-lookup"><span data-stu-id="cfbdc-141">VDS\_HINT\_ISYANKABLE</span></span>                  | <span data-ttu-id="cfbdc-142">0x0100L</span><span class="sxs-lookup"><span data-stu-id="cfbdc-142">0x0100L</span></span> |



 

### <a name="miscellaneous-constants"></a><span data-ttu-id="cfbdc-143">Constantes misceláneas</span><span class="sxs-lookup"><span data-stu-id="cfbdc-143">Miscellaneous Constants</span></span>



| <span data-ttu-id="cfbdc-144">Constante</span><span class="sxs-lookup"><span data-stu-id="cfbdc-144">Constant</span></span>                     | <span data-ttu-id="cfbdc-145">Value</span><span class="sxs-lookup"><span data-stu-id="cfbdc-145">Value</span></span>      |
|------------------------------|------------|
| <span data-ttu-id="cfbdc-146">\_ \_ prioridad mínima de regeneración de VDS \_</span><span class="sxs-lookup"><span data-stu-id="cfbdc-146">VDS\_REBUILD\_PRIORITY\_MIN</span></span>  | <span data-ttu-id="cfbdc-147">0x0001L</span><span class="sxs-lookup"><span data-stu-id="cfbdc-147">0x0001L</span></span>    |
| <span data-ttu-id="cfbdc-148">\_información del \_ LUN de VDS de ver \_</span><span class="sxs-lookup"><span data-stu-id="cfbdc-148">VER\_VDS\_LUN\_INFORMATION</span></span>   | <span data-ttu-id="cfbdc-149">1</span><span class="sxs-lookup"><span data-stu-id="cfbdc-149">1</span></span>          |
| <span data-ttu-id="cfbdc-150">longitud máxima de \_ ComputerName \_</span><span class="sxs-lookup"><span data-stu-id="cfbdc-150">MAX\_COMPUTERNAME\_LENGTH</span></span>    | <span data-ttu-id="cfbdc-151">15</span><span class="sxs-lookup"><span data-stu-id="cfbdc-151">15</span></span>         |
| <span data-ttu-id="cfbdc-152">longitud máxima del \_ PROVIDERNAME \_</span><span class="sxs-lookup"><span data-stu-id="cfbdc-152">MAX\_PROVIDERNAME\_LENGTH</span></span>    | <span data-ttu-id="cfbdc-153">200</span><span class="sxs-lookup"><span data-stu-id="cfbdc-153">200</span></span>        |
| <span data-ttu-id="cfbdc-154">longitud máxima de \_ VERSIONSTRING \_</span><span class="sxs-lookup"><span data-stu-id="cfbdc-154">MAX\_VERSIONSTRING\_LENGTH</span></span>   | <span data-ttu-id="cfbdc-155">16</span><span class="sxs-lookup"><span data-stu-id="cfbdc-155">16</span></span>         |
| <span data-ttu-id="cfbdc-156">\_prop. letra de unidad \_</span><span class="sxs-lookup"><span data-stu-id="cfbdc-156">DRIVE\_LETTER\_PROP</span></span>          | <span data-ttu-id="cfbdc-157">N/D</span><span class="sxs-lookup"><span data-stu-id="cfbdc-157">N/A</span></span>        |
| <span data-ttu-id="cfbdc-158">tamaño máximo del \_ nombre de FS \_ \_</span><span class="sxs-lookup"><span data-stu-id="cfbdc-158">MAX\_FS\_NAME\_SIZE</span></span>          | <span data-ttu-id="cfbdc-159">8</span><span class="sxs-lookup"><span data-stu-id="cfbdc-159">8</span></span>          |
| <span data-ttu-id="cfbdc-160">\_IDX de miembro no válido \_</span><span class="sxs-lookup"><span data-stu-id="cfbdc-160">INVALID\_MEMBER\_IDX</span></span>         | <span data-ttu-id="cfbdc-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="cfbdc-161">0xFFFFFFFF</span></span> |
| <span data-ttu-id="cfbdc-162">\_longitud de \_ nombre de partición GPT \_</span><span class="sxs-lookup"><span data-stu-id="cfbdc-162">GPT\_PARTITION\_NAME\_LENGTH</span></span> | <span data-ttu-id="cfbdc-163">36</span><span class="sxs-lookup"><span data-stu-id="cfbdc-163">36</span></span>         |
| <span data-ttu-id="cfbdc-164">\_ruta de acceso máxima</span><span class="sxs-lookup"><span data-stu-id="cfbdc-164">MAX\_PATH</span></span>                    | <span data-ttu-id="cfbdc-165">260</span><span class="sxs-lookup"><span data-stu-id="cfbdc-165">260</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cfbdc-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cfbdc-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfbdc-167">Referencia de VDS</span><span class="sxs-lookup"><span data-stu-id="cfbdc-167">VDS Reference</span></span>](vds-reference.md)
</dt> </dl>

 

 
