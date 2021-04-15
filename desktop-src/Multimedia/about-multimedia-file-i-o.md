---
title: Acerca de la e/s de archivos multimedia
description: Acerca de la e/s de archivos multimedia
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Windows multimedia, e/s de archivos
- multimedia, e/s de archivos
- entrada multimedia, e/s de archivos
- e/s de archivos multimedia, acerca de
- e/s de archivos, acerca de
- entrada y salida (e/s), acerca de
- E/s (entrada y salida), acerca de
- e/s básicas
- formato de archivo de intercambio de recursos (RIFF)
- RIFF (formato de archivo de intercambio de recursos)
- RIFF E/S
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa055411819d719636d2e248ea5c565e3f060d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676163"
---
# <a name="about-multimedia-file-io"></a><span data-ttu-id="70229-114">Acerca de la e/s de archivos multimedia</span><span class="sxs-lookup"><span data-stu-id="70229-114">About Multimedia File I/O</span></span>

<span data-ttu-id="70229-115">La mayoría de las aplicaciones multimedia requieren entrada y salida (e/s) de archivo, es decir, la capacidad de crear, leer y escribir archivos de disco.</span><span class="sxs-lookup"><span data-stu-id="70229-115">Most multimedia applications require file input and output (I/O) — that is, the ability to create, read, and write disk files.</span></span> <span data-ttu-id="70229-116">Los servicios de e/s de archivos multimedia proporcionan e/s de archivos en búfer y no almacenada en búfer y admiten archivos RIFF.</span><span class="sxs-lookup"><span data-stu-id="70229-116">Multimedia file I/O services provide buffered and unbuffered file I/O and support for RIFF files.</span></span> <span data-ttu-id="70229-117">Los servicios son extensibles con procedimientos de e/s personalizados que se pueden compartir entre aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="70229-117">The services are extensible with custom I/O procedures that can be shared among applications.</span></span>

<span data-ttu-id="70229-118">La mayoría de las aplicaciones solo necesitan los servicios básicos de e/s de archivos y los servicios de e/s de archivos RIFF.</span><span class="sxs-lookup"><span data-stu-id="70229-118">Most applications need only the basic file I/O services and the RIFF file I/O services.</span></span> <span data-ttu-id="70229-119">Las aplicaciones sensibles al rendimiento de e/s de archivos, como las aplicaciones que transmiten datos de un disco compacto en tiempo real, pueden optimizar el rendimiento mediante el uso de servicios para acceder directamente al búfer de e/s de archivos.</span><span class="sxs-lookup"><span data-stu-id="70229-119">Applications sensitive to file I/O performance, such as applications that stream data from compact disc in real time, can optimize performance by using services to directly access the file I/O buffer.</span></span> <span data-ttu-id="70229-120">Las aplicaciones que tienen acceso a sistemas de almacenamiento personalizados, como archivos de archivos y bases de datos, pueden proporcionar su propio procedimiento de e/s que lee y escribe elementos del sistema de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="70229-120">Applications that access custom storage systems, such as file archives and databases, can provide their own I/O procedure that reads and writes elements of the storage system.</span></span>

 

 




