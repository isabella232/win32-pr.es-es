---
description: Cómo obtener más espacio libre en disco después de superar la asignación de cuota.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Administración de las cuotas de disco en el nivel de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc130cf925899ccf0a86af20ff6772689ecdfbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668366"
---
# <a name="user-level-administration-of-disk-quotas"></a><span data-ttu-id="25e40-103">Administración de las cuotas de disco en el nivel de usuario</span><span class="sxs-lookup"><span data-stu-id="25e40-103">User-level Administration of Disk Quotas</span></span>

<span data-ttu-id="25e40-104">Las cuotas de disco son transparentes para el usuario.</span><span class="sxs-lookup"><span data-stu-id="25e40-104">Disk quotas are transparent to the user.</span></span> <span data-ttu-id="25e40-105">Cuando un usuario pregunta cuánto espacio hay disponible en un disco, el sistema solo notifica la concesión de cuota disponible que el usuario tiene disponible.</span><span class="sxs-lookup"><span data-stu-id="25e40-105">When a user asks how much space is free on a disk, the system reports only the available quota allowance the user has available.</span></span> <span data-ttu-id="25e40-106">Si el usuario supera esta asignación, el sistema devuelve el error de **\_ disco \_ lleno** , del mismo modo que indicaría que el disco estaba lleno.</span><span class="sxs-lookup"><span data-stu-id="25e40-106">If the user exceeds this allowance, the system returns the **ERROR\_DISK\_FULL** error, just as it would to indicate that the disk was full.</span></span>

<span data-ttu-id="25e40-107">Para obtener más espacio libre en disco después de superar la asignación de cuota, el usuario debe realizar una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="25e40-107">To obtain more free disk space after exceeding the quota allowance, the user must do one of the following:</span></span>

-   <span data-ttu-id="25e40-108">Elimine algunos archivos.</span><span class="sxs-lookup"><span data-stu-id="25e40-108">Delete some files.</span></span>
-   <span data-ttu-id="25e40-109">Haga que otro usuario reclame la propiedad de algunos archivos.</span><span class="sxs-lookup"><span data-stu-id="25e40-109">Have another user claim ownership of some files.</span></span>
-   <span data-ttu-id="25e40-110">Haga que el administrador aumente la concesión de cuota.</span><span class="sxs-lookup"><span data-stu-id="25e40-110">Have the administrator increase the quota allowance.</span></span>

<span data-ttu-id="25e40-111">Los programas que necesitan recuperar la cantidad real de espacio libre en disco pueden llamar a la función [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) y examinar el parámetro *TotalNumberOfFreeBytes* .</span><span class="sxs-lookup"><span data-stu-id="25e40-111">Programs that need to retrieve the actual amount of free disk space can call the [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) function and look at the *TotalNumberOfFreeBytes* parameter.</span></span>

 

 



