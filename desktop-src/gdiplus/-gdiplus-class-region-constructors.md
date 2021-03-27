---
description: En este tema se enumeran los constructores de la clase region. Para obtener una lista de clases completa, vea region (clase).
ms.assetid: 94f4971c-defa-43e0-a0c0-4000557b0a5c
title: Constructores region. Region
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 98663587fab3722d689c9d34578d60daad922a2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156212"
---
# <a name="regionregion-constructors"></a><span data-ttu-id="ee9ec-104">Constructores region. Region</span><span class="sxs-lookup"><span data-stu-id="ee9ec-104">Region.Region constructors</span></span>

<span data-ttu-id="ee9ec-105">En este tema se enumeran los constructores de la clase [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) .</span><span class="sxs-lookup"><span data-stu-id="ee9ec-105">This topic lists the constructors of the [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) class.</span></span> <span data-ttu-id="ee9ec-106">Para obtener una lista de clases completa, vea **Region (clase**).</span><span class="sxs-lookup"><span data-stu-id="ee9ec-106">For a complete class listing, see **Region Class**.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ee9ec-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="ee9ec-107">Overload list</span></span>



| <span data-ttu-id="ee9ec-108">Constructor</span><span class="sxs-lookup"><span data-stu-id="ee9ec-108">Constructor</span></span>                                                                 | <span data-ttu-id="ee9ec-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee9ec-109">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee9ec-110">[**Región (HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span><span class="sxs-lookup"><span data-stu-id="ee9ec-110">[**Region(HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span></span>                  | <span data-ttu-id="ee9ec-111">Crea una región que es idéntica a la región especificada por un identificador a una región de GDI.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-111">Creates a region that is identical to the region that is specified by a handle to a GDI region.</span></span><br/>                                                                                       |
| <span data-ttu-id="ee9ec-112">[**Region (Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span><span class="sxs-lookup"><span data-stu-id="ee9ec-112">[**Region(Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span></span>            | <span data-ttu-id="ee9ec-113">Crea una región definida por un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-113">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="ee9ec-114">[**Región (RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="ee9ec-114">[**Region(RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span></span>          | <span data-ttu-id="ee9ec-115">Crea una región definida por un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-115">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="ee9ec-116">[**Region (BYTE \* , int)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span><span class="sxs-lookup"><span data-stu-id="ee9ec-116">[**Region(BYTE\*,INT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span></span> | <span data-ttu-id="ee9ec-117">Crea una región definida por los datos obtenidos de otra región.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-117">Creates a region that is defined by data obtained from another region.</span></span> <br/>                                                                                                               |
| <span data-ttu-id="ee9ec-118">[**Region (GraphicsPath \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span><span class="sxs-lookup"><span data-stu-id="ee9ec-118">[**Region(GraphicsPath\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span></span>        | <span data-ttu-id="ee9ec-119">Crea una región definida por una ruta de acceso (un objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) ) y tiene un modo de relleno que se encuentra en el objeto **GraphicsPath** .</span><span class="sxs-lookup"><span data-stu-id="ee9ec-119">Creates a region that is defined by a path (a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object) and has a fill mode that is contained in the **GraphicsPath** object.</span></span><br/> |
| <span data-ttu-id="ee9ec-120">[**Región ()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span><span class="sxs-lookup"><span data-stu-id="ee9ec-120">[**Region()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span></span>                           | <span data-ttu-id="ee9ec-121">Crea una región que es infinita.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-121">Creates a region that is infinite.</span></span> <span data-ttu-id="ee9ec-122">Éste es el constructor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-122">This is the default constructor.</span></span> <br/>                                                                                                                  |



 

 
