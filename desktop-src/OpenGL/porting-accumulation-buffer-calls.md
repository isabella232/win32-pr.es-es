---
title: Trasladar llamadas del búfer de acumulación
description: Debe asignar el búfer de acumulación solicitando el formato de píxel adecuado con la función auxInitDisplayMode o ChoosePixelFormat de OpenGL.
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- Migración de la contabilidad de IRIS, búferes de acumulación
- portabilidad de IRIS GL, búferes de acumulación
- portabilidad a OpenGL desde IRIS GL, búferes de acumulación
- Exportación de OpenGL desde IRIS GL, búferes de acumulación
- búferes de acumulación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca91cb3ba35535ba2470297070dffc932a1c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269427"
---
# <a name="porting-accumulation-buffer-calls"></a><span data-ttu-id="4468b-108">Trasladar llamadas del búfer de acumulación</span><span class="sxs-lookup"><span data-stu-id="4468b-108">Porting Accumulation Buffer Calls</span></span>

<span data-ttu-id="4468b-109">Debe asignar el búfer de acumulación solicitando el formato de píxel adecuado con la función **auxInitDisplayMode** o [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4468b-109">You must allocate your accumulation buffer by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function.</span></span> <span data-ttu-id="4468b-110">En la tabla siguiente se enumeran las funciones de contabilidad de IRIS que afectan al búfer de acumulación y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="4468b-110">The following table lists IRIS GL functions that affect the accumulation buffer and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="4468b-111">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="4468b-111">IRIS GL function</span></span>       | <span data-ttu-id="4468b-112">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="4468b-112">OpenGL function</span></span>                                       | <span data-ttu-id="4468b-113">Significado</span><span class="sxs-lookup"><span data-stu-id="4468b-113">Meaning</span></span>                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="4468b-114">**acsize**</span><span class="sxs-lookup"><span data-stu-id="4468b-114">**acsize**</span></span>             | <span data-ttu-id="4468b-115">**auxInitDisplayMode** o **ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="4468b-115">**auxInitDisplayMode** or **ChoosePixelFormat**</span></span>       | <span data-ttu-id="4468b-116">Especifica el número de bitplanes por componente de color en el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="4468b-116">Specifies number of bitplanes per color component in the accumulation buffer.</span></span> |
| <span data-ttu-id="4468b-117">**acbuf**</span><span class="sxs-lookup"><span data-stu-id="4468b-117">**acbuf**</span></span>              | [<span data-ttu-id="4468b-118">**glAccum**</span><span class="sxs-lookup"><span data-stu-id="4468b-118">**glAccum**</span></span>](glaccum.md)                            | <span data-ttu-id="4468b-119">Funciona en el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="4468b-119">Operates on the accumulation buffer.</span></span>                                          |
|                        | [<span data-ttu-id="4468b-120">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="4468b-120">**glClearAccum**</span></span>](glclearaccum.md)                  | <span data-ttu-id="4468b-121">Establece valores claros para el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="4468b-121">Sets clear values for accumulation buffer.</span></span>                                    |
| <span data-ttu-id="4468b-122">**acbuf**(AC \_ claro)</span><span class="sxs-lookup"><span data-stu-id="4468b-122">**acbuf**( AC\_CLEAR )</span></span> | <span data-ttu-id="4468b-123">[**glClear**](glclear.md) (bit de búfer de la acumulación de GL \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="4468b-123">[**glClear**](glclear.md) ( GL\_ACCUM\_BUFFER\_BIT )</span></span> | <span data-ttu-id="4468b-124">Borra el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="4468b-124">Clears the accumulation buffer.</span></span>                                               |



 

<span data-ttu-id="4468b-125">En la tabla siguiente se enumeran los parámetros de **acbuf** de la contabilidad de iris junto con los parámetros de [**glAccum**](glaccum.md) de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="4468b-125">The following table lists the IRIS GL **acbuf** parameters along with the equivalent OpenGL [**glAccum**](glaccum.md) parameters.</span></span>



| <span data-ttu-id="4468b-126">Parámetro de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="4468b-126">IRIS GL parameter</span></span>     | <span data-ttu-id="4468b-127">Parámetro de OpenGL</span><span class="sxs-lookup"><span data-stu-id="4468b-127">OpenGL parameter</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="4468b-128">acumulación de AC \_</span><span class="sxs-lookup"><span data-stu-id="4468b-128">AC\_ACCUMULATE</span></span>        | <span data-ttu-id="4468b-129">LIBRO \_ acumulado</span><span class="sxs-lookup"><span data-stu-id="4468b-129">GL\_ACCUM</span></span>        |
| <span data-ttu-id="4468b-130">acumulación de AC \_ Clear \_</span><span class="sxs-lookup"><span data-stu-id="4468b-130">AC\_CLEAR\_ACCUMULATE</span></span> | <span data-ttu-id="4468b-131">carga en contab. \_</span><span class="sxs-lookup"><span data-stu-id="4468b-131">GL\_LOAD</span></span>         |
| <span data-ttu-id="4468b-132">retorno de CA \_</span><span class="sxs-lookup"><span data-stu-id="4468b-132">AC\_RETURN</span></span>            | <span data-ttu-id="4468b-133">devolución de GL \_</span><span class="sxs-lookup"><span data-stu-id="4468b-133">GL\_RETURN</span></span>       |
| <span data-ttu-id="4468b-134">AC \_ mult</span><span class="sxs-lookup"><span data-stu-id="4468b-134">AC\_MULT</span></span>              | <span data-ttu-id="4468b-135">\_mult</span><span class="sxs-lookup"><span data-stu-id="4468b-135">GL\_MULT</span></span>         |
| <span data-ttu-id="4468b-136">\_Agregar AC</span><span class="sxs-lookup"><span data-stu-id="4468b-136">AC\_ADD</span></span>               | <span data-ttu-id="4468b-137">\_Agregar GL</span><span class="sxs-lookup"><span data-stu-id="4468b-137">GL\_ADD</span></span>          |



 

 

 




