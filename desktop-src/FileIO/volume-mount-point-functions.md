---
description: Funciones que se usan para administrar carpetas montadas.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Funciones de carpeta montada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e984b9bee902f11af9d7b2b956ea0681cd6e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360815"
---
# <a name="mounted-folder-functions"></a><span data-ttu-id="73ac5-103">Funciones de carpeta montada</span><span class="sxs-lookup"><span data-stu-id="73ac5-103">Mounted Folder Functions</span></span>

<span data-ttu-id="73ac5-104">Las funciones de carpeta montada se pueden dividir en tres grupos: funciones de uso general, funciones usadas para buscar volúmenes y funciones que se usan para examinar un volumen en busca de carpetas montadas.</span><span class="sxs-lookup"><span data-stu-id="73ac5-104">The mounted folder functions can be divided into three groups: general-purpose functions, functions used to scan for volumes, and functions used to scan a volume for mounted folders.</span></span>

## <a name="general-purpose-mounted-folder-functions"></a><span data-ttu-id="73ac5-105">General-Purpose funciones de carpeta montada</span><span class="sxs-lookup"><span data-stu-id="73ac5-105">General-Purpose Mounted Folder Functions</span></span>



| <span data-ttu-id="73ac5-106">Función</span><span class="sxs-lookup"><span data-stu-id="73ac5-106">Function</span></span>                                                                     | <span data-ttu-id="73ac5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="73ac5-107">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73ac5-108">**DeleteVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="73ac5-108">**DeleteVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | <span data-ttu-id="73ac5-109">Elimina una letra de unidad o una carpeta montada.</span><span class="sxs-lookup"><span data-stu-id="73ac5-109">Deletes a drive letter or mounted folder.</span></span>                                                                                                                   |
| [<span data-ttu-id="73ac5-110">**GetVolumeNameForVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="73ac5-110">**GetVolumeNameForVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | <span data-ttu-id="73ac5-111">Recupera la ruta de acceso de GUID de volumen para el volumen asociado al punto de montaje de volumen especificado (letra de unidad, ruta de acceso de GUID de volumen o carpeta montada).</span><span class="sxs-lookup"><span data-stu-id="73ac5-111">Retrieves the volume GUID path for the volume that is associated with the specified volume mount point (drive letter, volume GUID path, or mounted folder).</span></span> |
| [<span data-ttu-id="73ac5-112">**GetVolumePathName**</span><span class="sxs-lookup"><span data-stu-id="73ac5-112">**GetVolumePathName**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | <span data-ttu-id="73ac5-113">Recupera la carpeta montada que está asociada con el volumen especificado.</span><span class="sxs-lookup"><span data-stu-id="73ac5-113">Retrieves the mounted folder that is associated with the specified volume.</span></span>                                                                                  |
| [<span data-ttu-id="73ac5-114">**SetVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="73ac5-114">**SetVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | <span data-ttu-id="73ac5-115">Asocia un volumen con una letra de unidad o un directorio de otro volumen.</span><span class="sxs-lookup"><span data-stu-id="73ac5-115">Associates a volume with a drive letter or a directory on another volume.</span></span>                                                                                   |



 

## <a name="volume-scanning-functions"></a><span data-ttu-id="73ac5-116">Funciones de Volume-Scanning</span><span class="sxs-lookup"><span data-stu-id="73ac5-116">Volume-Scanning Functions</span></span>



| <span data-ttu-id="73ac5-117">Función</span><span class="sxs-lookup"><span data-stu-id="73ac5-117">Function</span></span>                                   | <span data-ttu-id="73ac5-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="73ac5-118">Description</span></span>                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73ac5-119">**FindFirstVolume**</span><span class="sxs-lookup"><span data-stu-id="73ac5-119">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | <span data-ttu-id="73ac5-120">Devuelve el nombre de un volumen de un equipo.</span><span class="sxs-lookup"><span data-stu-id="73ac5-120">Returns the name of a volume on a computer.</span></span> <span data-ttu-id="73ac5-121">[**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) se usa para empezar a enumerar los volúmenes de un equipo.</span><span class="sxs-lookup"><span data-stu-id="73ac5-121">[**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) is used to begin enumerating the volumes of a computer.</span></span> |
| [<span data-ttu-id="73ac5-122">**FindNextVolume**</span><span class="sxs-lookup"><span data-stu-id="73ac5-122">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | <span data-ttu-id="73ac5-123">Continúa una búsqueda de volumen iniciada por una llamada a [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span><span class="sxs-lookup"><span data-stu-id="73ac5-123">Continues a volume search started by a call to [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span>                                                     |
| [<span data-ttu-id="73ac5-124">**FindVolumeClose**</span><span class="sxs-lookup"><span data-stu-id="73ac5-124">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | <span data-ttu-id="73ac5-125">Cierra una búsqueda de volúmenes.</span><span class="sxs-lookup"><span data-stu-id="73ac5-125">Closes a search for volumes.</span></span>                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a><span data-ttu-id="73ac5-126">Funciones de examen de carpetas montadas</span><span class="sxs-lookup"><span data-stu-id="73ac5-126">Mounted Folder Scanning Functions</span></span>



| <span data-ttu-id="73ac5-127">Función</span><span class="sxs-lookup"><span data-stu-id="73ac5-127">Function</span></span>                                                       | <span data-ttu-id="73ac5-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="73ac5-128">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73ac5-129">**FindFirstVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="73ac5-129">**FindFirstVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | <span data-ttu-id="73ac5-130">Recupera el nombre de una carpeta montada en el volumen especificado.</span><span class="sxs-lookup"><span data-stu-id="73ac5-130">Retrieves the name of a mounted folder on the specified volume.</span></span> <span data-ttu-id="73ac5-131">[**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) se usa para empezar a examinar las carpetas montadas en un volumen.</span><span class="sxs-lookup"><span data-stu-id="73ac5-131">[**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) is used to begin scanning the mounted folders on a volume.</span></span> |
| [<span data-ttu-id="73ac5-132">**FindNextVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="73ac5-132">**FindNextVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | <span data-ttu-id="73ac5-133">Continúa una búsqueda de carpeta montada iniciada por una llamada a [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).</span><span class="sxs-lookup"><span data-stu-id="73ac5-133">Continues a mounted folder search started by a call to [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).</span></span>                                                                    |
| [<span data-ttu-id="73ac5-134">**FindVolumeMountPointClose**</span><span class="sxs-lookup"><span data-stu-id="73ac5-134">**FindVolumeMountPointClose**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | <span data-ttu-id="73ac5-135">Cierra una búsqueda de carpetas montadas.</span><span class="sxs-lookup"><span data-stu-id="73ac5-135">Closes a search for mounted folders.</span></span>                                                                                                                                                      |



 

 

 



