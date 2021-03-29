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
# <a name="grouping-shapes"></a>Agrupar formas

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Como ha aprendido, puede dibujar fácilmente formas individuales mediante VML. En esta sección, explicaremos las ventajas de agrupar formas juntas y cómo agrupar formas.

Si tuviera muchas formas que debían escalarse, moverse o girarse juntas, le resultaría tedioso establecer los atributos individualmente para cada forma. Además, aumentaría el margen de errores. Sería mejor si pudiera agrupar las formas y, a continuación, establecer los atributos para todo el grupo.

En VML, puede usar el `<group>` elemento para agrupar muchas formas para que se puedan transformar como una unidad. Por ejemplo, tal y como se muestra en la siguiente representación VML, puede agrupar fácilmente dos formas.


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



Cuando se agrupan las formas, usan el [espacio de coordenadas local](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) del grupo. Por lo tanto, las formas dentro de un grupo se pueden escalar y pasar a la vez. Verá más ejemplos en el tema usar el espacio de coordenadas local.

Dentro de un grupo, puede tener tantas formas o grupos como desee. Cuando un grupo está dentro de otro grupo, se denomina "grupo anidado". No hay ninguna limitación en los niveles de anidamiento.

Por ejemplo, las líneas siguientes muestran un grupo anidado de tres niveles. Shape3 y Shape4 están en GroupC. Shape2 y GroupC están en GroupB. Shape1 y GroupB están en GroupA.


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



Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858388) .

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="summary"></a>Resumen

Puede usar el `<group>` elemento para agrupar muchas formas para que se puedan transformar como una unidad.

 

 