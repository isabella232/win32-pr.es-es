---
title: Dibujar formas básicas
description: En este artículo se describe el dibujo de formas básicas en VML, una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Taller web, dibujar formas
- diseñar páginas web, dibujar formas
- Lenguaje de marcado de vectores (VML),dibujar formas
- VML (Lenguaje de marcado de vectores),dibujar formas
- gráficos vectoriales, dibujar formas
- dibujar formas
- Formas de VML, dibujo
- Lenguaje de marcado de vectores (VML),XML
- VML (Lenguaje de marcado de vectores),XML
- gráficos vectoriales, XML
- Lenguaje de marcado de vectores (VML),CSS2
- VML (Lenguaje de marcado de vectores),CSS2
- gráficos vectoriales, CSS2
- Lenguaje de marcado de vectores (VML),elements
- VML (Lenguaje de marcado de vectores),elements
- gráficos vectoriales, elementos
- Elementos VML, dibujar formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00701e8ac77bd5bda7156c04ca25427d131646bf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407738"
---
# <a name="drawing-basic-shapes"></a>Dibujar formas básicas

En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

En este tema, mostraremos lo fácil que es dibujar una forma mediante VML.

Para crear un óvalo rojo en una página web, como se muestra en la siguiente imagen, puede dibujar el óvalo mediante una herramienta de edición gráfica, guardar el dibujo como mapa de bits e insertar el mapa de bits en la página web:

![oval1.gif (627 bytes)](images/oval1.gif)

Como alternativa, puede usar VML para dibujar gráficos. En el ejemplo anterior, puede escribir las siguientes líneas en la región de `<BODY>` la página web para dibujar el óvalo rojo:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





`<v:...>` y `</v:...>` son la etiqueta de inicio y la etiqueta final en la [sintaxis XML](#xml-structure).`style='width:100pt; height:75pt'` proporciona [información de CSS](#css-information). **oval** y **fillcolor**="red" son [elementos VML.](#vml-elements)

Puede modificar los gráficos simplemente cambiando sus atributos de propiedad en VML. En el ejemplo anterior, si cambia a , como se muestra en la siguiente representación `fillcolor="red"` `fillcolor="blue"` de VML, el óvalo rojo cambiará a azul:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





Los exploradores que admiten VML pueden representar y mostrar los gráficos representados en VML sin tener que descargar archivos de imagen independientes. La mayoría de los gráficos representados en VML se representan más rápido en los exploradores y requieren menos espacio en disco y tiempo de descarga.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="xml-structure"></a>Estructura XML

VmL tiene formato según las reglas de lenguaje de marcado extensible (XML). Cualquier analizador XML estándar puede analizar VML y entregar los datos resultantes a un procesador específico de VML. Para que los exploradores sepan cómo entregar datos a un procesador específico de VML, debe escribir información como espacios de nombres y objetos [personalizados](web-workshop---how-to-use-vml-on-web-pages----appendix.md) [incrustados.](web-workshop---how-to-use-vml-on-web-pages----appendix.md) A continuación, puede usar VML para escribir gráficos en la `<BODY>` región como hizo en el ejemplo anterior.

El `"v:"` prefijo de cada etiqueta XML identifica la etiqueta como VML. El `"v:"` prefijo de la región debe ser coherente con `<BODY>` `<html xmlns:v="...">` .

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="css-information"></a>Información de CSS

VML usa [Hojas de estilo CSS nivel 2 (CSS2) para](https://www.w3.org/TR/PR-CSS2/) determinar el tamaño de los gráficos y colocar los gráficos en una página web. En el ejemplo anterior, especificamos el tamaño del óvalo como 100 puntos (ancho) por 75 puntos (alto) ( `style='width:100pt;height:75pt'` ).

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="vml-elements"></a>Elementos VML

En el ejemplo anterior, se usó un elemento predefinido vml `<oval>` para dibujar un óvalo. A continuación, se usa el atributo de propiedad **fillcolor** del `<oval>` elemento para rellenar el óvalo con rojo.

Según la sección Etiquetas de [inicio,](https://www.w3.org/TR/REC-xml#sec-starttags) Etiquetas finales y etiquetas Empty-Element de la especificación [XML 1.0,](https://www.w3.org/TR/REC-xml)las etiquetas de elemento vacío se pueden usar para cualquier elemento que no tenga contenido. Por ejemplo, como se muestra en la siguiente representación de VML, no hay contenido (sub element) dentro del `<oval>` elemento. (Tenga en cuenta **que el estilo** **y el color de relleno** son los atributos del `<oval>` elemento; no son sub-elementos).


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



Por lo tanto, puede usar la etiqueta empty-element, como se muestra en la siguiente representación de VML, para representar lo mismo que la línea anterior.


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="summary"></a>Resumen

Puede usar VML para dibujar gráficos en una página web y, a continuación, personalizar esos gráficos simplemente cambiando sus atributos de propiedad. Además, la mayoría de los gráficos representados en VML se representan más rápido en los exploradores y toman menos tiempo de descarga y espacio en disco.

 

 