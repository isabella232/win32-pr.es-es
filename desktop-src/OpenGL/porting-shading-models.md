---
title: Trasladar modelos de sombreado
description: Al igual que IRIS GL, OpenGL permite cambiar entre el sombreado suave (Gouraud) y el sombreado plano. En la tabla siguiente se enumeran las funciones de sombreado y interpolación de la contabilidad de IRIS y sus funciones de OpenGL equivalentes.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- Migración de la contabilidad de IRIS, sombreado
- portabilidad de IRIS GL, sombreado
- trasladar a OpenGL desde IRIS GL, sombreado
- Exportación de OpenGL desde IRIS GL, sombreado
- sombreado suave
- Sombreado Gouraud
- sombreado plano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124bb002f6f133b4d47dd40e1a0e8738c512ce99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357354"
---
# <a name="porting-shading-models"></a><span data-ttu-id="4f5b0-111">Trasladar modelos de sombreado</span><span class="sxs-lookup"><span data-stu-id="4f5b0-111">Porting Shading Models</span></span>

<span data-ttu-id="4f5b0-112">Al igual que IRIS GL, OpenGL permite cambiar entre el sombreado suave (Gouraud) y el sombreado plano.</span><span class="sxs-lookup"><span data-stu-id="4f5b0-112">Like IRIS GL, OpenGL lets you switch between smooth (Gouraud) shading and flat shading.</span></span> <span data-ttu-id="4f5b0-113">En la tabla siguiente se enumeran las funciones de sombreado y interpolación de la contabilidad de IRIS y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="4f5b0-113">The following table lists the IRIS GL shading and dithering functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="4f5b0-114">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="4f5b0-114">IRIS GL function</span></span>                                   | <span data-ttu-id="4f5b0-115">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="4f5b0-115">OpenGL function</span></span>                                                                                    | <span data-ttu-id="4f5b0-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4f5b0-116">Meaning</span></span>                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="4f5b0-117">**shademodel**(plano)</span><span class="sxs-lookup"><span data-stu-id="4f5b0-117">**shademodel**(FLAT)</span></span>                               | <span data-ttu-id="4f5b0-118">[**glShadeModel**](glshademodel.md) (GL \_ plano)</span><span class="sxs-lookup"><span data-stu-id="4f5b0-118">[**glShadeModel**](glshademodel.md) ( GL\_FLAT )</span></span>                                                  | <span data-ttu-id="4f5b0-119">Realiza un sombreado plano.</span><span class="sxs-lookup"><span data-stu-id="4f5b0-119">Does flat shading.</span></span>           |
| <span data-ttu-id="4f5b0-120">**shademodel**(GOURAUD)</span><span class="sxs-lookup"><span data-stu-id="4f5b0-120">**shademodel**(GOURAUD)</span></span>                            | <span data-ttu-id="4f5b0-121">**glShadeModel**(GL \_ Smooth)</span><span class="sxs-lookup"><span data-stu-id="4f5b0-121">**glShadeModel**( GL\_SMOOTH )</span></span>                                                                     | <span data-ttu-id="4f5b0-122">Suaviza el sombreado.</span><span class="sxs-lookup"><span data-stu-id="4f5b0-122">Does smooth shading.</span></span>         |
| <span data-ttu-id="4f5b0-123">**getsm**</span><span class="sxs-lookup"><span data-stu-id="4f5b0-123">**getsm**</span></span>                                          | <span data-ttu-id="4f5b0-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ modelo de sombreado de contabilidad \_ )</span><span class="sxs-lookup"><span data-stu-id="4f5b0-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SHADE\_MODEL )</span></span>      | <span data-ttu-id="4f5b0-125">Devuelve el modelo de sombra actual.</span><span class="sxs-lookup"><span data-stu-id="4f5b0-125">Returns current shade model.</span></span> |
| <span data-ttu-id="4f5b0-126">interpolación de **interpolación (DT** \_ en) (DT  \_ OFF)</span><span class="sxs-lookup"><span data-stu-id="4f5b0-126">**dither**(DT\_ON) **dither**(DT\_OFF)</span></span> <br/> | <span data-ttu-id="4f5b0-127">[**glEnable**](glenable.md) (interpolación en contab. \_ )[**glDisable**](gldisable.md)( \_ interpolación de contabilidad)</span><span class="sxs-lookup"><span data-stu-id="4f5b0-127">[**glEnable**](glenable.md) ( GL\_DITHER )[**glDisable**](gldisable.md)( GL\_DITHER )</span></span><br/> | <span data-ttu-id="4f5b0-128">Activa o desactiva el tramado.</span><span class="sxs-lookup"><span data-stu-id="4f5b0-128">Turns dithering on/off.</span></span>      |



 

<span data-ttu-id="4f5b0-129">??</span><span class="sxs-lookup"><span data-stu-id="4f5b0-129">??</span></span>

 

 





