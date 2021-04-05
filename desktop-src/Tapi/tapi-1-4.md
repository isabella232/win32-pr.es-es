---
description: TAPI 1,4 agregó varias API, mensajes, constantes y elementos de estructura a la especificación 1,3.
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32f4320043ada2e2ae5477a698bde63f28d2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001923"
---
# <a name="tapi-14"></a><span data-ttu-id="bd41d-103">TAPI 1,4</span><span class="sxs-lookup"><span data-stu-id="bd41d-103">TAPI 1.4</span></span>

<span data-ttu-id="bd41d-104">TAPI 1,4 agregó varias API, mensajes, constantes y elementos de estructura a la especificación 1,3.</span><span class="sxs-lookup"><span data-stu-id="bd41d-104">TAPI 1.4 added a number of APIs, messages, constants, and structure elements to the 1.3 specification.</span></span> <span data-ttu-id="bd41d-105">TAPI 1,4 solo admite profesionales de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="bd41d-105">TAPI 1.4 supports only 16-bit TSPs.</span></span> <span data-ttu-id="bd41d-106">Sin embargo, permite desarrollar aplicaciones de 32 bits sin tener que preocuparse por las limitaciones de Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="bd41d-106">However, it does allow 32-bit applications to be developed without having to worry about the limitations of 16-bit Windows.</span></span>

<span data-ttu-id="bd41d-107">Los archivos de encabezado TAPI y TSPI se utilizan para desarrollar ambas aplicaciones tanto para TAPI 1,4 como para TAPI 2. x.</span><span class="sxs-lookup"><span data-stu-id="bd41d-107">The TAPI and TSPI header files are used to develop both applications for both TAPI 1.4 and TAPI 2.x.</span></span> <span data-ttu-id="bd41d-108">Aunque no hubo muchos cambios en las estructuras entre estas dos especificaciones, hubo cambios en la API (específicamente, compatibilidad con Unicode) que hacen que sea muy importante tener en cuenta que los encabezados se compilan de forma diferente, dependiendo de la constante de la \_ versión actual de TAPI \_ .</span><span class="sxs-lookup"><span data-stu-id="bd41d-108">While there were not many changes to the structures between these two specifications, there were changes to the API (specifically, Unicode support) that make it very important to note that the headers compile differently, depending on the TAPI\_CURRENT\_VERSION constant.</span></span> <span data-ttu-id="bd41d-109">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="bd41d-109">For example:</span></span>

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> <span data-ttu-id="bd41d-110">La \_ \_ versión actual de TAPI debe definirse para todas las aplicaciones TAPI.</span><span class="sxs-lookup"><span data-stu-id="bd41d-110">TAPI\_CURRENT\_VERSION should be defined for all TAPI applications.</span></span> <span data-ttu-id="bd41d-111">Aunque no es estrictamente necesario para el desarrollo de TAPI 2. x, pueden producirse cambios futuros para requerir este problema.</span><span class="sxs-lookup"><span data-stu-id="bd41d-111">While it is not strictly necessary for TAPI 2.x development, future changes could occur to require this.</span></span>

 

 

 



