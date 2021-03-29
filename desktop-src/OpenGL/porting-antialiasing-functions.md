---
title: Trasladar funciones de suavizado de contorno
description: Trasladar funciones de suavizado de contorno
ms.assetid: 7f79f0fa-4a08-4678-bc73-8611e8d9e91a
keywords:
- Migración de la contabilidad de IRIS y suavizado de contorno
- portabilidad de IRIS GL, antialiasing
- trasladar a OpenGL desde IRIS GL, suavizado de contorno
- Exportación de OpenGL desde IRIS GL, suavizado de contorno
- suavizado de contorno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec2fcae4fe7b6909e00efb0fb892821a5c12765
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419124"
---
# <a name="porting-antialiasing-functions"></a><span data-ttu-id="2c099-108">Trasladar funciones de suavizado de contorno</span><span class="sxs-lookup"><span data-stu-id="2c099-108">Porting Antialiasing Functions</span></span>

<span data-ttu-id="2c099-109">En OpenGL, el modo de subpíxeles está siempre activado, por lo tanto, el **subpíxel** de la función de contabilidad de iris no es necesario y no tiene ningún equivalente de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2c099-109">In OpenGL the subpixel mode is always on, consequently the IRIS GL function **subpixel**(**TRUE**) is not necessary and has no OpenGL equivalent.</span></span> <span data-ttu-id="2c099-110">En los temas siguientes se describen los aspectos del código de suavizado de contorno de la contabilidad de IRIS.</span><span class="sxs-lookup"><span data-stu-id="2c099-110">The following topics describe aspects of porting IRIS GL antialiasing code.</span></span>

-   [<span data-ttu-id="2c099-111">Trasladar código de fusión</span><span class="sxs-lookup"><span data-stu-id="2c099-111">Porting Blending Code</span></span>](porting-blending-code.md)
-   [<span data-ttu-id="2c099-112">Portabilidad de las funciones de prueba de afunction</span><span class="sxs-lookup"><span data-stu-id="2c099-112">Porting afunction Test Functions</span></span>](porting-afunction-test-functions.md)
-   [<span data-ttu-id="2c099-113">Usar funciones de suavizado de contorno</span><span class="sxs-lookup"><span data-stu-id="2c099-113">Using Antialiasing Functions</span></span>](using-antialiasing-functions.md)

 

 




