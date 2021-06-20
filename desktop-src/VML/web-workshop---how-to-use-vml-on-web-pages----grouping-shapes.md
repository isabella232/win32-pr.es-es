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
# <a name="grouping-shapes"></a>Agrupación de formas

En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Como ha aprendido, puede dibujar fácilmente formas individuales mediante VML. En esta sección, explicaremos las ventajas de agrupar formas y cómo agrupar formas.

Si tuviera muchas formas que deban escalarse, moverse o girar juntas, le resultaría tedioso establecer los atributos individualmente para cada forma. Además, aumentaría el margen de errores. Sería mejor agrupar las formas y, a continuación, establecer los atributos para todo el grupo.

En VML, puede usar el elemento para agrupar muchas formas para que se `<group>` puedan transformar como una unidad. Por ejemplo, como se muestra en la siguiente representación de VML, puede agrupar fácilmente dos formas.


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



Cuando las formas se agrupan, usan el [espacio de coordenadas local](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) del grupo. Por lo tanto, las formas dentro de un grupo se pueden escalar y mover juntas. Verá más ejemplos en el tema Usar espacio de coordenadas local.

Dentro de un grupo, puede tener tantas formas o grupos como desee. Cuando un grupo está dentro de otro grupo, se denomina "grupo anidado". No hay ninguna limitación en los niveles de anidamiento.

Por ejemplo, las líneas siguientes muestran un grupo anidado de 3 niveles. Shape3 y Shape4 están en GroupC. Shape2 y GroupC están en GroupB. Shape1 y GroupB están en GroupA.


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

[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)

## <a name="summary"></a>Resumen

Puede usar el elemento para agrupar muchas formas para `<group>` que se puedan transformar como una unidad.

 

 