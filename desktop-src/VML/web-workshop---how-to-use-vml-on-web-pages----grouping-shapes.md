---
title: Agrupación de formas
description: En este artículo se describe la agrupación de formas en VML, una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Taller web, agrupación de formas
- diseñar páginas web, agrupar formas
- Lenguaje de marcado de vectores (VML), agrupar formas
- VML (Lenguaje de marcado de vectores), agrupación de formas
- gráficos vectoriales, formas de agrupación
- Formas de VML, agrupación
- agrupación de formas
- Lenguaje de marcado de vectores (VML), elemento group
- VML (Lenguaje de marcado de vectores), elemento group
- gráficos vectoriales, elemento group
- elemento de grupo
- Elementos de VML, group
- Lenguaje de marcado de vectores (VML), espacio de coordenadas local
- VML (Lenguaje de marcado de vectores),espacio de coordenadas local
- gráficos vectoriales, espacio de coordenadas local
- espacio de coordenadas local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e0c3073f55d23c15734b5d5ddfa886e7291530
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407708"
---
# <a name="grouping-shapes"></a><span data-ttu-id="01edf-119">Agrupación de formas</span><span class="sxs-lookup"><span data-stu-id="01edf-119">Grouping Shapes</span></span>

<span data-ttu-id="01edf-120">En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="01edf-120">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="01edf-121">Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="01edf-121">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="01edf-122">A partir de diciembre de 2011, este tema se archivó.</span><span class="sxs-lookup"><span data-stu-id="01edf-122">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="01edf-123">Como resultado, ya no se mantiene activamente.</span><span class="sxs-lookup"><span data-stu-id="01edf-123">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="01edf-124">Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="01edf-124">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="01edf-125">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="01edf-125">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="01edf-126">Como ha aprendido, puede dibujar fácilmente formas individuales mediante VML.</span><span class="sxs-lookup"><span data-stu-id="01edf-126">As you've learned, you can easily draw individual shapes by using VML.</span></span> <span data-ttu-id="01edf-127">En esta sección, explicaremos las ventajas de agrupar formas y cómo agrupar formas.</span><span class="sxs-lookup"><span data-stu-id="01edf-127">In this section, we will explain the benefits of grouping shapes together, and how to group shapes.</span></span>

<span data-ttu-id="01edf-128">Si tuviera muchas formas que deban escalarse, moverse o girar juntas, le resultaría tedioso establecer los atributos individualmente para cada forma.</span><span class="sxs-lookup"><span data-stu-id="01edf-128">If you had many shapes that needed to be scaled, moved, or rotated together, you would find it tedious to set the attributes individually for each shape.</span></span> <span data-ttu-id="01edf-129">Además, aumentaría el margen de errores.</span><span class="sxs-lookup"><span data-stu-id="01edf-129">Plus you would raise your margin for errors.</span></span> <span data-ttu-id="01edf-130">Sería mejor agrupar las formas y, a continuación, establecer los atributos para todo el grupo.</span><span class="sxs-lookup"><span data-stu-id="01edf-130">It would be better if you could group the shapes, and then set the attributes for the entire group.</span></span>

<span data-ttu-id="01edf-131">En VML, puede usar el elemento para agrupar muchas formas para que se `<group>` puedan transformar como una unidad.</span><span class="sxs-lookup"><span data-stu-id="01edf-131">In VML, you can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span> <span data-ttu-id="01edf-132">Por ejemplo, como se muestra en la siguiente representación de VML, puede agrupar fácilmente dos formas.</span><span class="sxs-lookup"><span data-stu-id="01edf-132">For example, as shown in the following VML representation, you can easily group two shapes together.</span></span>


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



<span data-ttu-id="01edf-133">Cuando las formas se agrupan, usan el [espacio de coordenadas local](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) del grupo.</span><span class="sxs-lookup"><span data-stu-id="01edf-133">When shapes are grouped, they use the [local coordinate space](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) of the group.</span></span> <span data-ttu-id="01edf-134">Por lo tanto, las formas dentro de un grupo se pueden escalar y mover juntas.</span><span class="sxs-lookup"><span data-stu-id="01edf-134">Therefore, shapes within a group can be scaled and moved together.</span></span> <span data-ttu-id="01edf-135">Verá más ejemplos en el tema Usar espacio de coordenadas local.</span><span class="sxs-lookup"><span data-stu-id="01edf-135">You will see more examples in the Use Local Coordinate Space topic.</span></span>

<span data-ttu-id="01edf-136">Dentro de un grupo, puede tener tantas formas o grupos como desee.</span><span class="sxs-lookup"><span data-stu-id="01edf-136">Inside a group, you can have as many shapes or groups as you want.</span></span> <span data-ttu-id="01edf-137">Cuando un grupo está dentro de otro grupo, se denomina "grupo anidado".</span><span class="sxs-lookup"><span data-stu-id="01edf-137">When a group is inside another group, it is called a "nested group".</span></span> <span data-ttu-id="01edf-138">No hay ninguna limitación en los niveles de anidamiento.</span><span class="sxs-lookup"><span data-stu-id="01edf-138">There is no limitation on the levels of nesting.</span></span>

<span data-ttu-id="01edf-139">Por ejemplo, las líneas siguientes muestran un grupo anidado de 3 niveles.</span><span class="sxs-lookup"><span data-stu-id="01edf-139">For example, the following lines demonstrate a 3-level nested group.</span></span> <span data-ttu-id="01edf-140">Shape3 y Shape4 están en GroupC.</span><span class="sxs-lookup"><span data-stu-id="01edf-140">Shape3 and Shape4 are in GroupC.</span></span> <span data-ttu-id="01edf-141">Shape2 y GroupC están en GroupB.</span><span class="sxs-lookup"><span data-stu-id="01edf-141">Shape2 and GroupC are in GroupB.</span></span> <span data-ttu-id="01edf-142">Shape1 y GroupB están en GroupA.</span><span class="sxs-lookup"><span data-stu-id="01edf-142">Shape1 and GroupB are in GroupA.</span></span>


```HTML
<body>
   <v:group id="GroupA"...>
      <v:shape id="Shape1"...></v:shape>
      <v:group id="GroupB"...>
         <v:shape id="Shape2"...></v:shape>
         <v:group id="GroupC"...>
            <v:shape id="Shape3"...></v:shape>
            <v:shape id="Shape4"...></v:shape>
         </v:group>
      </v:group>
   </v:group>
</body>
```



<span data-ttu-id="01edf-143">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span><span class="sxs-lookup"><span data-stu-id="01edf-143">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span></span>

<span data-ttu-id="01edf-144">[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)</span><span class="sxs-lookup"><span data-stu-id="01edf-144">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="01edf-145">Resumen</span><span class="sxs-lookup"><span data-stu-id="01edf-145">Summary</span></span>

<span data-ttu-id="01edf-146">Puede usar el elemento para agrupar muchas formas para `<group>` que se puedan transformar como una unidad.</span><span class="sxs-lookup"><span data-stu-id="01edf-146">You can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span>

 

 