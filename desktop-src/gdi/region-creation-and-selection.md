---
description: Una aplicación crea una región mediante una llamada a una función asociada a una forma específica. En la tabla siguiente se muestran las funciones asociadas a cada una de las formas estándar.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Creación y selección de regiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27a7887e41a04a62015fa3fc9d82f5beeb01d6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984835"
---
# <a name="region-creation-and-selection"></a><span data-ttu-id="00351-104">Creación y selección de regiones</span><span class="sxs-lookup"><span data-stu-id="00351-104">Region Creation and Selection</span></span>

<span data-ttu-id="00351-105">Una aplicación crea una región mediante una llamada a una función asociada a una forma específica.</span><span class="sxs-lookup"><span data-stu-id="00351-105">An application creates a region by calling a function associated with a specific shape.</span></span> <span data-ttu-id="00351-106">En la tabla siguiente se muestran las funciones asociadas a cada una de las formas estándar.</span><span class="sxs-lookup"><span data-stu-id="00351-106">The following table shows the function(s) associated with each of the standard shapes.</span></span>



| <span data-ttu-id="00351-107">Forma</span><span class="sxs-lookup"><span data-stu-id="00351-107">Shape</span></span>                                   | <span data-ttu-id="00351-108">Función</span><span class="sxs-lookup"><span data-stu-id="00351-108">Function</span></span>                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00351-109">Región rectangular</span><span class="sxs-lookup"><span data-stu-id="00351-109">Rectangular region</span></span>                      | <span data-ttu-id="00351-110">[**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)</span><span class="sxs-lookup"><span data-stu-id="00351-110">[**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)</span></span> |
| <span data-ttu-id="00351-111">Región rectangular con esquinas redondeadas</span><span class="sxs-lookup"><span data-stu-id="00351-111">Rectangular region with rounded corners</span></span> | [<span data-ttu-id="00351-112">**CreateRoundRectRgn**</span><span class="sxs-lookup"><span data-stu-id="00351-112">**CreateRoundRectRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| <span data-ttu-id="00351-113">Región elíptica</span><span class="sxs-lookup"><span data-stu-id="00351-113">Elliptical region</span></span>                       | <span data-ttu-id="00351-114">[**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [ **CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span><span class="sxs-lookup"><span data-stu-id="00351-114">[**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span></span>                   |
| <span data-ttu-id="00351-115">Región poligonal</span><span class="sxs-lookup"><span data-stu-id="00351-115">Polygonal region</span></span>                        | <span data-ttu-id="00351-116">[**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span><span class="sxs-lookup"><span data-stu-id="00351-116">[**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span></span>                               |



 

<span data-ttu-id="00351-117">Cada función de creación de regiones devuelve un identificador que identifica la nueva región.</span><span class="sxs-lookup"><span data-stu-id="00351-117">Each region creation function returns a handle that identifies the new region.</span></span> <span data-ttu-id="00351-118">Una aplicación puede usar este identificador para seleccionar la región en un contexto de dispositivo llamando a la función [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) y proporcionando este identificador como segundo argumento.</span><span class="sxs-lookup"><span data-stu-id="00351-118">An application can use this handle to select the region into a device context by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function and supplying this handle as the second argument.</span></span> <span data-ttu-id="00351-119">Después de seleccionar una región en un contexto de dispositivo, la aplicación puede realizar varias operaciones en ella.</span><span class="sxs-lookup"><span data-stu-id="00351-119">After a region is selected into a device context, the application can perform various operations on it.</span></span>

 

 



