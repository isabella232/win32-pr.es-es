---
title: Dibujar formas básicas
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Web Workshop, dibujar formas
- diseñar páginas web, dibujar formas
- Lenguaje de marcado de vectores (VML), dibujar formas
- VML (Lenguaje de marcado de vectores), dibujar formas
- gráficos vectoriales, dibujar formas
- dibujar formas
- Formas VML, dibujo
- Lenguaje de marcado de vectores (VML), XML
- VML (Lenguaje de marcado de vectores), XML
- gráficos vectoriales, XML
- Lenguaje de marcado de vectores (VML), CSS2
- VML (Lenguaje de marcado de vectores), CSS2
- gráficos vectoriales, CSS2
- Lenguaje de marcado de vectores (VML), elementos
- VML (Lenguaje de marcado de vectores), elementos
- gráficos vectoriales, elementos
- Elementos VML, dibujar formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7ab25fc9310750c9f49c5978a063c76639ec4bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488167"
---
# <a name="drawing-basic-shapes"></a>Dibujar formas básicas

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

En este tema, explicaremos lo fácil que es dibujar una forma mediante VML.

Para crear un óvalo rojo en una página web, como se muestra en la siguiente imagen, puede dibujar el óvalo mediante una herramienta de edición de gráficos, guardar el dibujo como mapa de bits y, a continuación, insertar el mapa de bits en la página web:

![oval1.gif (627 bytes)](images/oval1.gif)

Como alternativa, puede usar VML para dibujar gráficos. En el ejemplo anterior, puede escribir las líneas siguientes en la `<BODY>` región de la página web para dibujar el óvalo rojo:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





`<v:...>` y `</v:...>` son la etiqueta inicial y la etiqueta final en la [sintaxis XML](#xml-structure).`style='width:100pt; height:75pt'` proporciona [información de CSS](#css-information). **oval** y **fillColor**= "red" son [elementos VML](#vml-elements).

Puede modificar los gráficos simplemente cambiando sus atributos de propiedad en VML. En el ejemplo anterior, si cambia `fillcolor="red"` a `fillcolor="blue"` , como se muestra en la representación VML siguiente, el óvalo rojo cambiará a azul:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





Los exploradores que admiten VML pueden representar y mostrar los gráficos representados en VML sin tener que descargar archivos de imagen independientes. La mayoría de los gráficos representados en VML se representan más rápido en los exploradores y requieren menos espacio en disco y tiempo de descarga.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="xml-structure"></a>Estructura XML

VML está formateado de acuerdo con las reglas de lenguaje de marcado extensible (XML). Cualquier analizador XML estándar puede analizar VML y entregar los datos resultantes a un procesador específico de VML. Para que los exploradores sepan cómo entregar los datos a un procesador específico de VML, debe escribir información como [espacios de nombres](web-workshop---how-to-use-vml-on-web-pages----appendix.md) y [objetos personalizados incrustados](web-workshop---how-to-use-vml-on-web-pages----appendix.md). Después, puede usar VML para escribir gráficos en la `<BODY>` región tal como hizo en el ejemplo anterior.

El `"v:"` prefijo en cada etiqueta XML identifica la etiqueta como VML. El `"v:"` Prefijo de la `<BODY>` región debe ser coherente con `<html xmlns:v="...">` .

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="css-information"></a>Información de CSS

VML usa [hojas de estilo CSS, nivel 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) para determinar el tamaño de los gráficos y colocar los gráficos en una página web. En el ejemplo anterior, se especifica el tamaño del óvalo como 100 puntos (ancho) en 75 puntos (alto) ( `style='width:100pt;height:75pt'` ).

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="vml-elements"></a>Elementos VML

En el ejemplo anterior, usamos un elemento predefinido VML `<oval>` para dibujar un óvalo. Después usamos el atributo **fillColor** Property del `<oval>` elemento para rellenar el óvalo con color rojo.

En función de las etiquetas de [Inicio, las etiquetas de cierre y Empty-Element](https://www.w3.org/TR/REC-xml#sec-starttags) sección de etiquetas de [XML 1,0](https://www.w3.org/TR/REC-xml), las etiquetas de elementos vacíos se pueden usar para cualquier elemento que no tenga contenido. Por ejemplo, tal y como se muestra en la siguiente representación VML, no hay contenido (subelemento) dentro del `<oval>` elemento. (Observe que el **estilo** y el **fillColor** son los atributos del `<oval>` elemento; no son elementos secundarios).


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



Por lo tanto, puede usar la etiqueta de elemento vacío, tal como se muestra en la siguiente representación de VML, para representar lo mismo que la línea anterior.


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="summary"></a>Resumen

Puede usar VML para dibujar gráficos en una página web y, a continuación, personalizar esos gráficos simplemente cambiando sus atributos de propiedad. Además, la mayoría de los gráficos representados en VML se representan más rápido en los exploradores y tardan menos tiempo en descargarse y en el espacio en disco.

 

 