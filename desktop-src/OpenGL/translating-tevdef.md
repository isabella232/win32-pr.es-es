---
title: Traducción de tevdef
description: El siguiente ejemplo de código es una definición de entorno de textura de la contabilidad de IRIS que especifica el \_ parámetro Decal Texture-Environment.
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- Migración de la contabilidad de IRIS, textura
- portabilidad de IRIS GL, textura
- trasladar a OpenGL desde IRIS GL, textura
- Exportación de OpenGL desde IRIS GL, textura
- textura
- Migración de la contabilidad de IRIS, tevdef
- portabilidad de IRIS GL, tevdef
- migración a OpenGL desde IRIS GL, tevdef
- Exportación de OpenGL desde IRIS GL, tevdef
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac2610d1467adb6faa1ea105fc8e8734bfb9c4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994544"
---
# <a name="translating-tevdef"></a><span data-ttu-id="b41a4-113">Traducción de tevdef</span><span class="sxs-lookup"><span data-stu-id="b41a4-113">Translating tevdef</span></span>

<span data-ttu-id="b41a4-114">El siguiente ejemplo de código es una definición de entorno de textura de la contabilidad de IRIS que especifica el \_ parámetro Decal Texture-Environment:</span><span class="sxs-lookup"><span data-stu-id="b41a4-114">The following code example is an IRIS GL texture-environment definition that specifies the TV\_DECAL texture-environment parameter:</span></span>


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



<span data-ttu-id="b41a4-115">y el mismo código traducido a OpenGL:</span><span class="sxs-lookup"><span data-stu-id="b41a4-115">and the same code translated to OpenGL:</span></span>


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



<span data-ttu-id="b41a4-116">En la tabla siguiente se enumeran los parámetros de entorno de textura GL de IRIS y sus parámetros de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="b41a4-116">The following table lists the IRIS GL texture-environment parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="b41a4-117">Parámetro de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="b41a4-117">IRIS GL parameter</span></span>     | <span data-ttu-id="b41a4-118">Parámetro de OpenGL</span><span class="sxs-lookup"><span data-stu-id="b41a4-118">OpenGL parameter</span></span>             |
|-----------------------|------------------------------|
| <span data-ttu-id="b41a4-119">TV \_ modular</span><span class="sxs-lookup"><span data-stu-id="b41a4-119">TV\_MODULATE</span></span>          | <span data-ttu-id="b41a4-120">\_modular GL</span><span class="sxs-lookup"><span data-stu-id="b41a4-120">GL\_MODULATE</span></span>                 |
| <span data-ttu-id="b41a4-121">Calcomanía de TV \_</span><span class="sxs-lookup"><span data-stu-id="b41a4-121">TV\_DECAL</span></span>             | <span data-ttu-id="b41a4-122">\_marcas GL</span><span class="sxs-lookup"><span data-stu-id="b41a4-122">GL\_DECAL</span></span>                    |
| <span data-ttu-id="b41a4-123">TV \_ Blend</span><span class="sxs-lookup"><span data-stu-id="b41a4-123">TV\_BLEND</span></span>             | <span data-ttu-id="b41a4-124">fusión de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="b41a4-124">GL\_BLEND</span></span>                    |
| <span data-ttu-id="b41a4-125">COLOR de TV \_</span><span class="sxs-lookup"><span data-stu-id="b41a4-125">TV\_COLOR</span></span>             | <span data-ttu-id="b41a4-126">\_color de textura de libro de contabilidad \_ \_</span><span class="sxs-lookup"><span data-stu-id="b41a4-126">GL\_TEXTURE\_ENV\_COLOR</span></span>      |
| <span data-ttu-id="b41a4-127">TV \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="b41a4-127">TV\_ALPHA</span></span>             | <span data-ttu-id="b41a4-128">No es equivalente de OpenGL directo.</span><span class="sxs-lookup"><span data-stu-id="b41a4-128">No direct OpenGL equivalent.</span></span> |
| <span data-ttu-id="b41a4-129">\_selección de componentes de TV \_</span><span class="sxs-lookup"><span data-stu-id="b41a4-129">TV\_COMPONENT\_SELECT</span></span> | <span data-ttu-id="b41a4-130">No es equivalente de OpenGL directo.</span><span class="sxs-lookup"><span data-stu-id="b41a4-130">No direct OpenGL equivalent.</span></span> |



 

<span data-ttu-id="b41a4-131">Para obtener más información sobre los parámetros de entorno de textura, vea [**glTexEnv**](gltexenv-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b41a4-131">For more information about texture-environment parameters, see [**glTexEnv**](gltexenv-functions.md).</span></span>

 

 




