---
description: Hay disponible una comprobación de redundancia cíclica (CRC) de archivos con Windows Installer.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: Comprobación de CRC durante una instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e03bb6754b0259aa8b27333c8137408e7dc956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277984"
---
# <a name="crc-checking-during-an-installation"></a><span data-ttu-id="74357-103">Comprobación de CRC durante una instalación</span><span class="sxs-lookup"><span data-stu-id="74357-103">CRC Checking During an Installation</span></span>

<span data-ttu-id="74357-104">Hay disponible una comprobación de redundancia cíclica (CRC) de archivos con Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="74357-104">A Cyclic Redundancy Check (CRC) of files is available with Windows Installer.</span></span> <span data-ttu-id="74357-105">La comprobación de CRC es un mecanismo de comprobación de errores, similar a una suma de comprobación, que permite que una aplicación determine si se ha modificado la información de un archivo.</span><span class="sxs-lookup"><span data-stu-id="74357-105">CRC checking is an error-checking mechanism, similar to a checksum, that enables an application to determine whether the information in a file has been modified.</span></span> <span data-ttu-id="74357-106">Una vez que la Windows Installer termina de copiar un archivo, obtiene un valor CRC de los archivos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="74357-106">After the Windows Installer finishes copying a file, it gets a CRC value from both the source and destination files.</span></span> <span data-ttu-id="74357-107">El instalador comprueba el CRC original marcado en el archivo y lo compara con la CRC calculada a partir de la copia.</span><span class="sxs-lookup"><span data-stu-id="74357-107">The installer checks the original CRC stamped into the file and compares this to the CRC calculated from the copy.</span></span> <span data-ttu-id="74357-108">Se produce un error en la comprobación de CRC si el valor CRC original no es NULL y es diferente del CRC calculado en la copia.</span><span class="sxs-lookup"><span data-stu-id="74357-108">The CRC check fails if the original CRC value is non-null and is different from the CRC calculated on the copy.</span></span> <span data-ttu-id="74357-109">Si el CRC original es null, no se realiza ninguna comprobación.</span><span class="sxs-lookup"><span data-stu-id="74357-109">If the original CRC is null, no check occurs.</span></span>

<span data-ttu-id="74357-110">El Windows Installer realiza una comprobación de CRC en un archivo en los casos siguientes:</span><span class="sxs-lookup"><span data-stu-id="74357-110">The Windows Installer does a CRC check on a file in the following cases:</span></span>

-   <span data-ttu-id="74357-111">Si se establece la [propiedad MSICHECKCRCS](msicheckcrcs.md) y **msidbFileAttributesChecksum** se incluye en el campo Attributes del registro del archivo en la [tabla File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="74357-111">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md).</span></span> <span data-ttu-id="74357-112">El instalador realiza la comprobación de CRC una vez después de instalar, duplicar o mover el archivo.</span><span class="sxs-lookup"><span data-stu-id="74357-112">The installer does the CRC check once after installing, duplicating, or moving the file.</span></span>
-   <span data-ttu-id="74357-113">Si se establece la [propiedad MSICHECKCRCS](msicheckcrcs.md) y **msidbFileAttributesChecksum** se incluye en el campo Attributes del registro del archivo en la [tabla File](file-table.md), el instalador realiza una comprobación CRC después de aplicar la revisión del archivo.</span><span class="sxs-lookup"><span data-stu-id="74357-113">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check after patching the file.</span></span>
-   <span data-ttu-id="74357-114">Si el **msidbFileAttributesChecksum** se incluye en el campo atributos del registro del archivo en la [tabla de archivos](file-table.md), el instalador realiza una comprobación de CRC antes de enlazar las imágenes.</span><span class="sxs-lookup"><span data-stu-id="74357-114">If the **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check before binding images.</span></span>

<span data-ttu-id="74357-115">Si se produce un error en la comprobación antes de enlazar una imagen, el instalador informa de los dos errores siguientes en el archivo de registro y continúa con la instalación sin enlazar el archivo.</span><span class="sxs-lookup"><span data-stu-id="74357-115">If the check fails before binding an image, the installer reports the following two errors in the log file and continues the installation without binding the file.</span></span>



| <span data-ttu-id="74357-116">Código</span><span class="sxs-lookup"><span data-stu-id="74357-116">Code</span></span> | <span data-ttu-id="74357-117">Message</span><span class="sxs-lookup"><span data-stu-id="74357-117">Message</span></span>                                               |
|------|-------------------------------------------------------|
| <span data-ttu-id="74357-118">2941</span><span class="sxs-lookup"><span data-stu-id="74357-118">2941</span></span> | <span data-ttu-id="74357-119">No se puede calcular la CRC del archivo \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="74357-119">Unable to compute the CRC for file \[2\].</span></span>             |
| <span data-ttu-id="74357-120">2942</span><span class="sxs-lookup"><span data-stu-id="74357-120">2942</span></span> | <span data-ttu-id="74357-121">La acción BindImage no se ejecutó en el \[ \] archivo 2.</span><span class="sxs-lookup"><span data-stu-id="74357-121">BindImage action has not been executed on \[2\] file.</span></span> |



 

<span data-ttu-id="74357-122">Si se produce un error en la comprobación después de copiar, duplicar o revisar un archivo sin comprimir, el instalador informa del siguiente error.</span><span class="sxs-lookup"><span data-stu-id="74357-122">If the check fails after an uncompressed file had been copied, duplicated, or patched, the installer reports the following error.</span></span> <span data-ttu-id="74357-123">También se muestra este error si se produce un error en la comprobación después de copiar un archivo comprimido.</span><span class="sxs-lookup"><span data-stu-id="74357-123">This error is also reported if the check fails after a compressed file is copied.</span></span> <span data-ttu-id="74357-124">Si el archivo tiene el atributo **msidbFileAttributesVital** , el archivo se considera vital para la instalación y el usuario obtiene la opción de Reintentar o cancelar la instalación.</span><span class="sxs-lookup"><span data-stu-id="74357-124">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the user gets the option to retry or cancel the installation.</span></span> <span data-ttu-id="74357-125">Si el archivo está marcado como no vital en la columna atributos de la [tabla archivo](file-table.md), el usuario puede omitir el error y continuar, reintentar o cancelar la instalación.</span><span class="sxs-lookup"><span data-stu-id="74357-125">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user may ignore the error and continue, retry, or cancel the installation.</span></span>



| <span data-ttu-id="74357-126">Código</span><span class="sxs-lookup"><span data-stu-id="74357-126">Code</span></span> | <span data-ttu-id="74357-127">Message</span><span class="sxs-lookup"><span data-stu-id="74357-127">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="74357-128">1331</span><span class="sxs-lookup"><span data-stu-id="74357-128">1331</span></span> | <span data-ttu-id="74357-129">No se pudo copiar correctamente el \[ \] archivo 2: error de CRC.</span><span class="sxs-lookup"><span data-stu-id="74357-129">Failed to correctly copy \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="74357-130">Tenga en cuenta que solo se mueven los archivos sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="74357-130">Note that only uncompressed files are moved.</span></span> <span data-ttu-id="74357-131">Si se produce un error en la comprobación después de que se mueva un archivo sin comprimir, el instalador muestra el siguiente error.</span><span class="sxs-lookup"><span data-stu-id="74357-131">If the check fails after an uncompressed file is moved, the installer displays the following error.</span></span> <span data-ttu-id="74357-132">Si el archivo tiene el atributo **msidbFileAttributesVital** , el archivo se considera vital para la instalación y se produce un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="74357-132">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="74357-133">Si el archivo está marcado como no vital en la columna atributos de la [tabla archivo](file-table.md), el usuario obtiene la opción de cancelar o omitir el error y continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="74357-133">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="74357-134">Código</span><span class="sxs-lookup"><span data-stu-id="74357-134">Code</span></span> | <span data-ttu-id="74357-135">Message</span><span class="sxs-lookup"><span data-stu-id="74357-135">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="74357-136">1332</span><span class="sxs-lookup"><span data-stu-id="74357-136">1332</span></span> | <span data-ttu-id="74357-137">No se pudo quitar correctamente el \[ \] archivo 2: error de CRC.</span><span class="sxs-lookup"><span data-stu-id="74357-137">Failed to correctly move \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="74357-138">Si se produce un error en la comprobación después de revisar un archivo sin comprimir, el instalador muestra el siguiente error.</span><span class="sxs-lookup"><span data-stu-id="74357-138">If the check fails after an uncompressed file is patched, the installer displays the following error.</span></span> <span data-ttu-id="74357-139">Si el archivo tiene el atributo **msidbFileAttributesVital** , el archivo se considera vital para la instalación y se produce un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="74357-139">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="74357-140">Si el archivo está marcado como no vital en la columna atributos de la [tabla archivo](file-table.md), el usuario obtiene la opción de cancelar o omitir el error y continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="74357-140">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="74357-141">Código</span><span class="sxs-lookup"><span data-stu-id="74357-141">Code</span></span> | <span data-ttu-id="74357-142">Message</span><span class="sxs-lookup"><span data-stu-id="74357-142">Message</span></span>                                          |
|------|--------------------------------------------------|
| <span data-ttu-id="74357-143">1333</span><span class="sxs-lookup"><span data-stu-id="74357-143">1333</span></span> | <span data-ttu-id="74357-144">No se pudo revisar correctamente el \[ \] archivo 2: error de CRC.</span><span class="sxs-lookup"><span data-stu-id="74357-144">Failed to correctly patch \[2\] file: CRC error.</span></span> |



 

 

 



