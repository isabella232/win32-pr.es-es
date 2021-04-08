---
title: Arranque de archivos de imagen de Windows (WimBoot)
description: Arranque de archivos de imagen de Windows (WimBoot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f14ea506226e2c16d771ecec52fa31a8c871b4
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "103797133"
---
# <a name="windows-image-file-boot-wimboot"></a><span data-ttu-id="d0ca1-103">Arranque de archivos de imagen de Windows (WimBoot)</span><span class="sxs-lookup"><span data-stu-id="d0ca1-103">Windows Image File Boot (WimBoot)</span></span>

## <a name="platform"></a><span data-ttu-id="d0ca1-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="d0ca1-104">Platform</span></span>

<span data-ttu-id="d0ca1-105">**Clientes:** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d0ca1-105">**Clients:** Windows 8.1</span></span>  

## <a name="description"></a><span data-ttu-id="d0ca1-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0ca1-106">Description</span></span>

<span data-ttu-id="d0ca1-107">WimBoot es una forma alternativa para que los OEM implementen Windows.</span><span class="sxs-lookup"><span data-stu-id="d0ca1-107">WimBoot is an alternative way for OEMs to deploy Windows.</span></span> <span data-ttu-id="d0ca1-108">Una implementación de WimBoot inicia y ejecuta Windows directamente desde un archivo de imagen de Windows comprimido (WIM).</span><span class="sxs-lookup"><span data-stu-id="d0ca1-108">A WimBoot deployment boots and runs Windows directly out of a compressed Windows Image File (WIM).</span></span> <span data-ttu-id="d0ca1-109">Este archivo WIM es inmutable y el acceso a él lo administra un nuevo controlador de filtro del sistema de archivos (WoF.sys).</span><span class="sxs-lookup"><span data-stu-id="d0ca1-109">This WIM file is immutable, and access to it is managed by a new file system filter driver (WoF.sys).</span></span>

<span data-ttu-id="d0ca1-110">El resultado es una reducción significativa en el espacio en disco necesario para instalar Windows.</span><span class="sxs-lookup"><span data-stu-id="d0ca1-110">The result is a significant reduction in the disk space required to install Windows.</span></span>

## <a name="manifestations"></a><span data-ttu-id="d0ca1-111">Manifestaciones</span><span class="sxs-lookup"><span data-stu-id="d0ca1-111">Manifestations</span></span>

<span data-ttu-id="d0ca1-112">La mayoría de las aplicaciones deben no verse afectadas por WimBoot.</span><span class="sxs-lookup"><span data-stu-id="d0ca1-112">Most applications should be completely unaffected by WimBoot.</span></span> <span data-ttu-id="d0ca1-113">Solo pueden verse afectadas las aplicaciones que accedan a archivos del sistema o que desbloqueen archivos del sistema o archivos previamente cargados para el acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="d0ca1-113">Only applications that access and unlock system files or pre-loaded files for write access may be affected.</span></span> <span data-ttu-id="d0ca1-114">Dado que el WIM es inmutable, las actualizaciones de este (es decir, los archivos del sistema o cargados previamente) simplemente se almacenan en la partición C: \\ .</span><span class="sxs-lookup"><span data-stu-id="d0ca1-114">Since the WIM is immutable, updates to it (that is, system or pre-loaded files) are simply stored on the C:\\ partition.</span></span>

<span data-ttu-id="d0ca1-115">Si una aplicación tiene acceso de escritura desbloqueada para todos los archivos del sistema y los archivos cargados previamente, el ahorro que WimBoot entrega se perdería por completo, ya que todos estos archivos se descomprimen y se colocan en el volumen C: \\ .</span><span class="sxs-lookup"><span data-stu-id="d0ca1-115">If an application unlocked write access for all WIM-backed system and pre-loaded files, the savings that WimBoot delivers would be completely lost, as all of these files would be decompressed and placed on the C:\\ volume.</span></span>

<span data-ttu-id="d0ca1-116">Además, las aplicaciones de copia de seguridad y restauración deben tener en cuenta las implementaciones de WimBoot, ya que el WIM está presente en una partición independiente. es decir, en la copia de seguridad, se \\ deben guardar las particiones C: y Wim y ambas deben restaurarse juntas.</span><span class="sxs-lookup"><span data-stu-id="d0ca1-116">Furthermore, back-up and restore applications need to be aware of WimBoot deployments, as the WIM is present in a separate partition; that is, on back-up, both the C:\\ and WIM partitions must be saved and both must be restored together.</span></span>

## <a name="solution"></a><span data-ttu-id="d0ca1-117">Solución</span><span class="sxs-lookup"><span data-stu-id="d0ca1-117">Solution</span></span>

<span data-ttu-id="d0ca1-118">Se introdujeron nuevas API que permiten a las aplicaciones consultar directamente si un volumen o un archivo determinado están respaldados por un WIM.</span><span class="sxs-lookup"><span data-stu-id="d0ca1-118">New APIs were introduced that allow applications to directly query if a given volume or file is backed by a WIM.</span></span> <span data-ttu-id="d0ca1-119">Esta información permite a las aplicaciones tomar decisiones adecuadas, como abrir estos archivos solo para el acceso de lectura o identificar los volúmenes o las particiones que se deben incluir en la copia de seguridad y la restauración.</span><span class="sxs-lookup"><span data-stu-id="d0ca1-119">This information allows applications to make appropriate decisions, such as opening these files only for read access or to identify volumes/partitions that have to be backed up and restored together.</span></span>

## <a name="compatibility-performance-reliability-or-usability-tests"></a><span data-ttu-id="d0ca1-120">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="d0ca1-120">Compatibility, performance, reliability, or usability tests</span></span>

<span data-ttu-id="d0ca1-121">Los desarrolladores de aplicaciones deben probar su software y sus escenarios correspondientes en un sistema WimBoot, especialmente si estas aplicaciones tienen acceso a archivos del sistema o cargados previamente.</span><span class="sxs-lookup"><span data-stu-id="d0ca1-121">Application developers should test their software and its corresponding scenarios on a WimBoot system, especially if these applications access system or pre-loaded files.</span></span> <span data-ttu-id="d0ca1-122">Se debe prestar especial atención a una reducción significativa del espacio en disco disponible una vez completado un escenario.</span><span class="sxs-lookup"><span data-stu-id="d0ca1-122">Special attention should be paid to a significant reduction in available disk space after a scenario has been completed.</span></span>

 

 




