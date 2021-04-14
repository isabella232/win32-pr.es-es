---
title: Usar el elemento TipoForma
description: Usar el elemento TipoForma
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Web Workshop, TipoForma (elemento)
- diseñar páginas web, TipoForma (elemento)
- Lenguaje de marcado de vectores (VML), elemento TipoForma
- VML (Lenguaje de marcado de vectores), elemento TipoForma
- Vector Graphics, TipoForma (elemento)
- TipoForma (elemento)
- Elementos VML, TipoForma
- Formas VML, elemento TipoForma
- Lenguaje de marcado de vectores (VML), definir formas usadas con frecuencia
- VML (Lenguaje de marcado de vectores), definir formas usadas con frecuencia
- gráficos vectoriales, definir formas usadas con frecuencia
- definir formas usadas con frecuencia
- Formas VML, definir las usadas con frecuencia
- Lenguaje de marcado de vectores (VML), crear instancias de copias de formas
- VML (Lenguaje de marcado de vectores), crear instancias de copias de formas
- gráficos vectoriales, crear instancias de copias de formas
- crear instancias de copias de formas
- Formas VML, crear instancias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa7ec47dde492231e8bcd54f68e4637454613b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488170"
---
# <a name="using-the-shapetype-element"></a>Usar el elemento TipoForma

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

En este tema, se muestra cómo usar el `<shapetype>` elemento para definir sus propias formas usadas con frecuencia y, a continuación, crear una instancia de las formas del TipoForma, o crearlas.

Si desea dibujar muchas formas que tienen las mismas propiedades o similares, sería tedioso si tuviera que escribir repetidamente los mismos atributos de propiedad para cada forma. VML proporciona el `<shapetype>` elemento para que pueda definir un prototipo de una forma. Después, puede usar el `<shape>` elemento para crear instancias de muchas copias de formas del mismo TipoForma.

Puede seguir los tres pasos para definir un TipoForma y, a continuación, crear una instancia de una forma desde la TipoForma:

1.  Escriba un `<shapetype>` elemento y asígnele un nombre especificando el atributo id.
2.  Describa el TipoForma mediante sus atributos o subelementos de propiedad.
3.  Cree una instancia de una forma escribiendo un `<shape>` elemento y haga referencia al atributo de tipo de la forma en el atributo ID del TipoForma.

Por ejemplo, escriba las líneas siguientes para crear un TipoForma denominado "alshape":


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



A continuación, modifique el TipoForma estableciendo algunos atributos de propiedad, como `fillcolor="red" strokecolor="blue"` . O bien, puede usar subelementos dentro del TipoForma, como `<path>` , `<fill>` , `<stroke>` (hablaremos sobre esos subelementos en temas posteriores).


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



A continuación, cree una instancia de una forma a partir de la sección TipoForma "conshape" especificando `type="#MyShape"` , tal y como se muestra en la siguiente representación de VML. Esta forma hereda todas las propiedades del TipoForma ", y se muestra en el cuadro contenedor con un tamaño de 100 a 80.


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



Puede crear una instancia de otra forma desde la sección TipoForma "conshape" especificando `type="#MyShape"` y sobrescribiendo algunas propiedades, como `fillcolor="maroon"` , como se muestra en la siguiente representación VML. Esta forma hereda todas las propiedades de la sección TipoForma "disshape" excepto la propiedad fillColor y se muestra en el cuadro contenedor con un tamaño de 70 a 90.


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



Esta es la representación VML completa del ejemplo anterior:

![\-1.gif tipo1 (477 bytes)](images/type1-1.gif)![\-2.gif tipo1 (471 bytes)](images/type1-2.gif)


```HTML
<body>
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue" coordsize="21600,21600"
path="m10860,2187c10451,1746,9529,1018,9015,730,7865,152,6685,,5415,,4175,
152,2995,575,1967,1305,1150,2187,575,3222,242,4220,,5410,242,6560,575,7597l10860,
21600,20995,7597c21480,6560,21600,5410,21480,4220,21115,3222,20420,2187,19632,
1305,18575,575,17425,152,16275,,15005,,13735,152,12705,730,12176,1018,11254,1746,
10860,2187xe">
</v:shapetype>
<v:shape type="#MyShape" style='width:100;height:80;'/>
<v:shape type="#MyShape" style='width:70;height:90;' fillcolor="maroon"/>
</body>
```





Como ha aprendido, cuando se crea una instancia de una forma a partir de un TipoForma, se heredan todos los atributos de propiedad del TipoForma. Puede sobrescribir algunos o todos los atributos heredados mediante la redefinición de los atributos dentro del `<shape>` elemento. Tenga en cuenta que la herencia es solo un nivel. Esto se debe a que solo un `<shape>` elemento puede hacer referencia a un `<shapetype>` elemento. Un `<shapetype>` elemento no puede hacer referencia A otro `<shapetype>` elemento.

Además, el TipoForma no pertenece a ningún grupo. Por lo tanto, el `<shapetype>` elemento puede aparecer por sí solo o dentro de un `<group>` elemento. Puede tener muchas formas dentro de grupos diferentes que hagan referencia al mismo TipoForma. Si aparece un TipoForma dentro de un grupo, una forma que vive en otro grupo puede seguir haciendo referencia a este TipoForma.

Por ejemplo, en la siguiente representación de VML, Rect1 y Rect2 están en GroupA y Rect3 está en GroupB. Se crean instancias de los tres rectángulos de la forma de TipoForma.


```HTML
<body>
...
<v:shapetype id="MyShape" fillcolor="blue" strokecolor="red"...>
</v:shapetype>

<v:group id="GroupA"...>
<v:shape id="Rect1" type="#MyShape" .../>
<v:shape id="Rect2" type="#MyShape" strokecolor="black".../>
</v:group>

<v:group id="GroupB"...>
<v:shape id="Rect3" type="#MyShape" fillcolor="green".../>
</v:group>
...
</body>
```



Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858387) .

 

 