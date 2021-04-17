---
title: Portabilidad de los conjuntos, enlaces y conjuntos
description: Portabilidad de los conjuntos, enlaces y conjuntos
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- Migración de la contabilidad de IRIS, definiciones
- trasladar de IRIS GL, definiciones
- trasladar a OpenGL desde IRIS GL, definiciones
- Exportación de OpenGL desde IRIS GL, definiciones
- Migración de la contabilidad de IRIS, enlaces
- portabilidad de IRIS GL, enlaces
- trasladar a OpenGL desde IRIS GL, enlaces
- Exportación de OpenGL desde IRIS GL, enlaces
- Migración de la contabilidad de IRIS, conjuntos
- portabilidad de IRIS GL, conjuntos
- trasladar a OpenGL desde IRIS GL, conjuntos
- Exportación de OpenGL desde IRIS GL, conjuntos
- definitions
- enlaza
- conjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f9a88253390ee99f5b5870fd7a09e272f1c549
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665606"
---
# <a name="porting-defs-binds-and-sets"></a><span data-ttu-id="0fad7-118">Portabilidad de los conjuntos, enlaces y conjuntos</span><span class="sxs-lookup"><span data-stu-id="0fad7-118">Porting Defs, Binds, and Sets</span></span>

<span data-ttu-id="0fad7-119">OpenGL no tiene tablas de definiciones almacenadas. no se pueden definir modelos de iluminación, material, texturas, estilos de línea o patrones como objetos independientes como se puede hacer en la contabilidad de IRIS.</span><span class="sxs-lookup"><span data-stu-id="0fad7-119">OpenGL doesn't have tables of stored definitions; you can't define lighting models, material, textures, line styles, or patterns as separate objects as you can in IRIS GL.</span></span> <span data-ttu-id="0fad7-120">Por lo tanto, OpenGL no tiene equivalentes directos a las siguientes funciones de GL de IRIS:</span><span class="sxs-lookup"><span data-stu-id="0fad7-120">Thus OpenGL has no direct equivalents to the following IRIS GL functions:</span></span>

-   <span data-ttu-id="0fad7-121">**Imdef** e **inbind**</span><span class="sxs-lookup"><span data-stu-id="0fad7-121">**Imdef** and **Imbind**</span></span>
-   <span data-ttu-id="0fad7-122">**tevdef** y **tevbind**</span><span class="sxs-lookup"><span data-stu-id="0fad7-122">**tevdef** and **tevbind**</span></span>
-   <span data-ttu-id="0fad7-123">**textdef** y **textbind**</span><span class="sxs-lookup"><span data-stu-id="0fad7-123">**textdef** and **textbind**</span></span>
-   <span data-ttu-id="0fad7-124">**definestyle** y **setStyle**</span><span class="sxs-lookup"><span data-stu-id="0fad7-124">**definestyle** and **setstyle**</span></span>
-   <span data-ttu-id="0fad7-125">**defpattern** y **setpattern**</span><span class="sxs-lookup"><span data-stu-id="0fad7-125">**defpattern** and **setpattern**</span></span>

<span data-ttu-id="0fad7-126">Puede usar listas de visualización de OpenGL para imitar el mecanismo de Def/BIND de IRIS.</span><span class="sxs-lookup"><span data-stu-id="0fad7-126">You can use OpenGL display lists to mimic the IRIS GL def/bind mechanism.</span></span> <span data-ttu-id="0fad7-127">Por ejemplo, aquí se muestra una definición de material en IRIS GL:</span><span class="sxs-lookup"><span data-stu-id="0fad7-127">For example, here is a material definition in IRIS GL:</span></span>


```C++
float mat() = { 
    AMBIENT, .1, .1, .1, 
    DIFFUSE, 0, .369, .165, 
    SPECULAR, .5, .5, .5, 
    SHININESS, 10, 
    LMNULL 
}; 
lmdef(DEFMATERIAL, 1, 0, mat); 
lmbind(MATERIAL, 1);
```



<span data-ttu-id="0fad7-128">El siguiente ejemplo de código OpenGL define el mismo material en una lista de visualización a la que se hace referencia mediante el número de lista definido por el **valor de la función.**</span><span class="sxs-lookup"><span data-stu-id="0fad7-128">The following OpenGL code sample defines the same material in a display list that is referred to by the list number defined by **MYMATERIAL**.</span></span>


```C++
#define MYMATERIAL 10 
 
GLfloat        mat_amb[] = {.1, .1, .1, 1.0}; 
GLfloat        mat_dif[] = {0, .369, .165, 1.0}; 
GLfloat        mat_spec[] = {.5, .5, .5, 1.0}; 
 
glNewList(MYMATERIAL, GL_COMPILE); 
    glMaterialfv(GL_FRONT, GL_AMBIENT, mat_amb); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_dif); 
    glMaterialfv(GL_FRONT, GL_SHININESS, 10); 
glEndList(); 
 
glCallList( MYMATERIAL );
```



 

 




