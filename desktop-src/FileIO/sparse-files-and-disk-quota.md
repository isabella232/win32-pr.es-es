---
description: Un archivo disperso afecta a las cuotas de usuario por el tamaño nominal del archivo, no por la cantidad de espacio en disco real asignada.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: Archivos dispersos y cuotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 326780e2b2c5119256272c0d297613d2c32e6e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154604"
---
# <a name="sparse-files-and-disk-quotas"></a><span data-ttu-id="26a27-103">Archivos dispersos y cuotas de disco</span><span class="sxs-lookup"><span data-stu-id="26a27-103">Sparse Files and Disk Quotas</span></span>

<span data-ttu-id="26a27-104">Un archivo disperso afecta a las cuotas de usuario por el tamaño nominal del archivo, no por la cantidad de espacio en disco real asignada.</span><span class="sxs-lookup"><span data-stu-id="26a27-104">A sparse file affects user quotas by the nominal size of the file, not the actual allocated amount of disk space.</span></span> <span data-ttu-id="26a27-105">Es decir, la creación de un archivo de 50 MB con todos los ceros de bytes consume 50 MB de cuota de usuario.</span><span class="sxs-lookup"><span data-stu-id="26a27-105">That is, creating a 50-MB file with all zero bytes consumes 50 MB of that user's quota.</span></span> <span data-ttu-id="26a27-106">Esto significa que, a medida que el usuario escribe datos en el archivo disperso, no necesita preocuparse por superar su límite de cuota máxima, ya que ya se le ha cargado por el espacio.</span><span class="sxs-lookup"><span data-stu-id="26a27-106">This means that as the user writes data to the sparse file, he need not worry about exceeding his hard quota limit, because he has already been charged for the space.</span></span> <span data-ttu-id="26a27-107">Los administradores del sistema no deben contar en el tamaño de un archivo disperso que quede pequeño.</span><span class="sxs-lookup"><span data-stu-id="26a27-107">System administrators should not count on the size of a sparse file remaining small.</span></span> <span data-ttu-id="26a27-108">Por lo tanto, no deben conceder a sus usuarios límites de cuota forzados que superen el espacio físico disponible, a pesar del uso de archivos dispersos.</span><span class="sxs-lookup"><span data-stu-id="26a27-108">Therefore they should not grant their users hard quota limits that exceed the physical space available, despite the use of sparse files.</span></span>

 

 



