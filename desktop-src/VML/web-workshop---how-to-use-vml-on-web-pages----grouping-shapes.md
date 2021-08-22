---
title: Agrupación de formas
description: En este artículo se describe la agrupación de formas en VML, una característica que está en desuso a partir Windows Internet Explorer 9.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Taller web, agrupación de formas
- diseñar páginas web, agrupar formas
- Lenguaje de marcado de vectores (VML), agrupar formas
- VML (Lenguaje de marcado de vectores), agrupar formas
- gráficos vectoriales, agrupación de formas
- Formas de VML, agrupación
- agrupación de formas
- Lenguaje de marcado de vectores (VML), elemento group
- VML (Lenguaje de marcado de vectores), elemento group
- vector graphics,group element
- elemento de grupo
- Elementos de VML,group
- Lenguaje de marcado de vectores (VML), espacio de coordenadas local
- VML (Lenguaje de marcado de vectores), espacio de coordenadas local
- gráficos vectoriales, espacio de coordenadas local
- espacio de coordenadas local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc9ac6da1d38bb6b30f685ebfd0f5a1d9d6026620a0e0c65366ee021668240a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056963"
---
# <a name="grouping-shapes"></a>Agrupación de formas

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Como ha aprendido, puede dibujar fácilmente formas individuales mediante VML. En esta sección, explicaremos las ventajas de agrupar formas y cómo agrupar formas.

Si tuviera muchas formas que deban escalarse, moverse o girar juntas, le resultaría tedioso establecer los atributos individualmente para cada forma. Además, aumentaría el margen para los errores. Sería mejor si pudiera agrupar las formas y, a continuación, establecer los atributos para todo el grupo.

En VML, puede usar el elemento para agrupar muchas formas para que `<group>` se puedan transformar como una unidad. Por ejemplo, como se muestra en la siguiente representación de VML, puede agrupar fácilmente dos formas.


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



Cuando las formas se agrupan, usan el [espacio de coordenadas local](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) del grupo. Por lo tanto, las formas dentro de un grupo se pueden escalar y mover juntas. Verá más ejemplos en el tema Usar espacio de coordenadas local .

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

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="summary"></a>Resumen

Puede usar el elemento para agrupar muchas formas para `<group>` que se puedan transformar como una unidad.

 

 