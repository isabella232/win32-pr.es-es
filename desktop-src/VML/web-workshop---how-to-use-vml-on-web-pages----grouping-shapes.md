---
title: Agrupar formas
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Web Workshop, agrupar formas
- diseñar páginas web, agrupar formas
- Lenguaje de marcado de vectores (VML), agrupar formas
- VML (Lenguaje de marcado de vectores), agrupar formas
- gráficos vectoriales, agrupar formas
- Formas VML, agrupación
- agrupar formas
- Lenguaje de marcado de vectores (VML), elemento Group
- VML (Lenguaje de marcado de vectores), elemento Group
- Vector Graphics, Group (elemento)
- elemento de grupo
- Elementos VML, grupo
- Lenguaje de marcado de vectores (VML), espacio de coordenadas local
- VML (Lenguaje de marcado de vectores), espacio de coordenadas local
- gráficos vectoriales, espacio de coordenadas local
- espacio de coordenadas local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eed282094e2d24d2d27e338b93731eaaa1eec0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078270"
---
# <a name="grouping-shapes"></a><span data-ttu-id="7e6c7-120">Agrupar formas</span><span class="sxs-lookup"><span data-stu-id="7e6c7-120">Grouping Shapes</span></span>

<span data-ttu-id="7e6c7-121">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-121">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7e6c7-122">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-122">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7e6c7-123">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-123">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7e6c7-124">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-124">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7e6c7-125">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7e6c7-125">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7e6c7-126">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7e6c7-126">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7e6c7-127">Como ha aprendido, puede dibujar fácilmente formas individuales mediante VML.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-127">As you've learned, you can easily draw individual shapes by using VML.</span></span> <span data-ttu-id="7e6c7-128">En esta sección, explicaremos las ventajas de agrupar formas juntas y cómo agrupar formas.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-128">In this section, we will explain the benefits of grouping shapes together, and how to group shapes.</span></span>

<span data-ttu-id="7e6c7-129">Si tuviera muchas formas que debían escalarse, moverse o girarse juntas, le resultaría tedioso establecer los atributos individualmente para cada forma.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-129">If you had many shapes that needed to be scaled, moved, or rotated together, you would find it tedious to set the attributes individually for each shape.</span></span> <span data-ttu-id="7e6c7-130">Además, aumentaría el margen de errores.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-130">Plus you would raise your margin for errors.</span></span> <span data-ttu-id="7e6c7-131">Sería mejor si pudiera agrupar las formas y, a continuación, establecer los atributos para todo el grupo.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-131">It would be better if you could group the shapes, and then set the attributes for the entire group.</span></span>

<span data-ttu-id="7e6c7-132">En VML, puede usar el `<group>` elemento para agrupar muchas formas para que se puedan transformar como una unidad.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-132">In VML, you can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span> <span data-ttu-id="7e6c7-133">Por ejemplo, tal y como se muestra en la siguiente representación VML, puede agrupar fácilmente dos formas.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-133">For example, as shown in the following VML representation, you can easily group two shapes together.</span></span>


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



<span data-ttu-id="7e6c7-134">Cuando se agrupan las formas, usan el [espacio de coordenadas local](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) del grupo.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-134">When shapes are grouped, they use the [local coordinate space](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) of the group.</span></span> <span data-ttu-id="7e6c7-135">Por lo tanto, las formas dentro de un grupo se pueden escalar y pasar a la vez.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-135">Therefore, shapes within a group can be scaled and moved together.</span></span> <span data-ttu-id="7e6c7-136">Verá más ejemplos en el tema usar el espacio de coordenadas local.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-136">You will see more examples in the Use Local Coordinate Space topic.</span></span>

<span data-ttu-id="7e6c7-137">Dentro de un grupo, puede tener tantas formas o grupos como desee.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-137">Inside a group, you can have as many shapes or groups as you want.</span></span> <span data-ttu-id="7e6c7-138">Cuando un grupo está dentro de otro grupo, se denomina "grupo anidado".</span><span class="sxs-lookup"><span data-stu-id="7e6c7-138">When a group is inside another group, it is called a "nested group".</span></span> <span data-ttu-id="7e6c7-139">No hay ninguna limitación en los niveles de anidamiento.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-139">There is no limitation on the levels of nesting.</span></span>

<span data-ttu-id="7e6c7-140">Por ejemplo, las líneas siguientes muestran un grupo anidado de tres niveles.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-140">For example, the following lines demonstrate a 3-level nested group.</span></span> <span data-ttu-id="7e6c7-141">Shape3 y Shape4 están en GroupC.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-141">Shape3 and Shape4 are in GroupC.</span></span> <span data-ttu-id="7e6c7-142">Shape2 y GroupC están en GroupB.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-142">Shape2 and GroupC are in GroupB.</span></span> <span data-ttu-id="7e6c7-143">Shape1 y GroupB están en GroupA.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-143">Shape1 and GroupB are in GroupA.</span></span>


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



<span data-ttu-id="7e6c7-144">Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span><span class="sxs-lookup"><span data-stu-id="7e6c7-144">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span></span>

<span data-ttu-id="7e6c7-145">[![volver ](images/top.gif) al principio hacia arriba](#top)</span><span class="sxs-lookup"><span data-stu-id="7e6c7-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="7e6c7-146">Resumen</span><span class="sxs-lookup"><span data-stu-id="7e6c7-146">Summary</span></span>

<span data-ttu-id="7e6c7-147">Puede usar el `<group>` elemento para agrupar muchas formas para que se puedan transformar como una unidad.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-147">You can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span>

 

 