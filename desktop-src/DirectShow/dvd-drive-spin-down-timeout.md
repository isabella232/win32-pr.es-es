---
description: Tiempo de espera de la unidad de DVD
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: Tiempo de espera de la unidad de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda6853830ee7289e529d029c78fe4e56e4a0e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906761"
---
# <a name="dvd-drive-spin-down-timeout"></a><span data-ttu-id="810fb-103">Tiempo de espera de la unidad de DVD</span><span class="sxs-lookup"><span data-stu-id="810fb-103">DVD Drive Spin Down Timeout</span></span>

<span data-ttu-id="810fb-104">En equipos portátiles, para conservar la duración de la batería, puede ser deseable reducir el tiempo que una unidad de DVD seguirá girando después de que el usuario haya pausado la reproducción.</span><span class="sxs-lookup"><span data-stu-id="810fb-104">On laptop computers, to conserve battery life it may be desirable to reduce the length of time that a DVD drive will continue to spin after the user has paused playback.</span></span> <span data-ttu-id="810fb-105">De forma predeterminada, el navegador de DVD mantiene el disco girando durante dos minutos.</span><span class="sxs-lookup"><span data-stu-id="810fb-105">By default, the DVD Navigator keeps the disc spinning for two minutes.</span></span> <span data-ttu-id="810fb-106">Este valor se puede modificar en el registro de Windows con esta clave:</span><span class="sxs-lookup"><span data-stu-id="810fb-106">This value can be modified in the Windows Registry under this key:</span></span>


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



<span data-ttu-id="810fb-107">where</span><span class="sxs-lookup"><span data-stu-id="810fb-107">where</span></span>


```
Sec
```



<span data-ttu-id="810fb-108">es el tiempo de espera en segundos.</span><span class="sxs-lookup"><span data-stu-id="810fb-108">is the spin down time in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="810fb-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="810fb-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="810fb-110">Apéndices</span><span class="sxs-lookup"><span data-stu-id="810fb-110">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 



