---
title: Consideraciones sobre la programación de puntos de control
description: Los desarrolladores que crean aplicaciones basadas en UPnP (o puntos de control) deben usar estas aplicaciones desde un cliente de APARTMENTTHREADED de coinit \_ . Existen problemas conocidos al usar la API de punto de control de un \_ cliente multiproceso de coinit que se ejecuta bajo estrés.
ms.assetid: a5d79a29-4192-40af-b75d-a31f1f46149c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76955177f9fc0c3b164d84998547c1afdfbfb4bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903734"
---
# <a name="control-point-programming-considerations"></a><span data-ttu-id="be836-104">Consideraciones sobre la programación de puntos de control</span><span class="sxs-lookup"><span data-stu-id="be836-104">Control Point Programming Considerations</span></span>

<span data-ttu-id="be836-105">Los desarrolladores que crean aplicaciones basadas en UPnP (o puntos de control) deben usar estas aplicaciones desde un cliente de APARTMENTTHREADED de coinit \_ .</span><span class="sxs-lookup"><span data-stu-id="be836-105">Developers who create UPnP-based applications (or control points) must use these applications from a COINIT\_APARTMENTTHREADED client.</span></span> <span data-ttu-id="be836-106">Existen problemas conocidos al usar la API de punto de control de un \_ cliente multiproceso de coinit que se ejecuta bajo estrés.</span><span class="sxs-lookup"><span data-stu-id="be836-106">There are known problems when using the Control Point API from a COINIT\_MULTITHREADED client running under stress.</span></span>

 

 




