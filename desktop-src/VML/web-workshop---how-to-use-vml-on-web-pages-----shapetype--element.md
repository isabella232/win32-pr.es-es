---
title: Usar el elemento Shapetype
description: Usar el elemento Shapetype
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Taller web, elemento shapetype
- diseñar páginas web, elemento shapetype
- Lenguaje de marcado de vectores (VML),elemento shapetype
- VML (Lenguaje de marcado de vectores),elemento shapetype
- vector graphics,shapetype element
- elemento shapetype
- Elementos VML,shapetype
- VmL shapes,shapetype element
- Lenguaje de marcado de vectores (VML), definir formas usadas con frecuencia
- VML (Lenguaje de marcado de vectores), definición de formas usadas con frecuencia
- gráficos vectoriales, definición de formas usadas con frecuencia
- definir formas usadas con frecuencia
- Formas de VML, definición de uso frecuente
- Lenguaje de marcado de vectores (VML), crear instancias de copias de formas
- VML (Lenguaje de marcado de vectores), creación de instancias de copias de formas
- gráficos vectoriales, creación de instancias de copias de formas
- crear instancias de copias de formas
- Formas de VML, creación de instancias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d815d9f5f911e1a34d558496881ae606819d328a501c635ff463a84f2926ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512659"
---
# <a name="using-the-shapetype-element"></a>Usar el elemento Shapetype

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

En este tema, se ilustrará cómo usar el elemento para definir sus propias formas usadas con frecuencia y, a continuación, crear instancias de formas a partir del `<shapetype>` tipo de forma.

Si quisiera dibujar muchas formas que tengan las mismas propiedades o propiedades similares, sería tedioso si tuviera que escribir repetidamente los mismos atributos de propiedad para cada forma. VML proporciona el `<shapetype>` elemento para que pueda definir un prototipo de una forma. A continuación, puede usar el elemento para crear instancias de muchas `<shape>` copias de formas del mismo tipo de forma.

Puede seguir los tres pasos para definir un tipo de forma y, a continuación, crear una instancia de una forma a partir del tipo de forma:

1.  Escriba un `<shapetype>` elemento y asízcále un nombre especificando el atributo id.
2.  Describa el tipo de forma mediante sus atributos de propiedad o sub-elementos.
3.  Cree una instancia de una forma escribiendo un elemento y haga referencia al atributo type de la forma al atributo `<shape>` id del tipo de forma.

Por ejemplo, escriba las líneas siguientes para crear un tipo de forma denominado "MyShape":


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



A continuación, modifique el tipo de forma estableciendo algunos atributos de propiedad, como `fillcolor="red" strokecolor="blue"` . O bien, puede usar sub-elementos dentro del tipo de forma, como , , (hablaremos sobre esos `<path>` `<fill>` `<stroke>` sub-elementos en temas posteriores).


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



A continuación, cree una instancia de una forma a partir del tipo de forma "MyShape" especificando , como se muestra `type="#MyShape"` en la siguiente representación de VML. Esta forma hereda todas las propiedades del tipo de forma "MyShape" y se muestra dentro de su cuadro de contenido con un tamaño de 100 por 80.


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



Puede crear instancias de otra forma a partir del tipo de forma "MyShape" especificando y sobrescribiendo algunas propiedades, como , como se muestra en la siguiente representación `type="#MyShape"` `fillcolor="maroon"` de VML. Esta forma hereda todas las propiedades del tipo de forma "MyShape", excepto la propiedad fillcolor, y se muestra dentro de su cuadro de contenido con un tamaño de 70 por 90.


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



Esta es la representación completa de VML del ejemplo anterior:

![type1 \-1.gif (477 bytes)](images/type1-1.gif)![type1 \-2.gif (471 bytes)](images/type1-2.gif)


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





Como ha aprendido, cuando se crea una instancia de una forma a partir de un tipo de forma, hereda todos los atributos de propiedad del tipo de forma. Puede sobrescribir algunos o todos los atributos heredados mediante la redefinición de los atributos dentro del `<shape>` elemento . Tenga en cuenta que la herencia es solo un nivel. Esto se debe a que solo `<shape>` un elemento puede hacer referencia a un elemento `<shapetype>` . Un `<shapetype>` elemento no puede hacer referencia a otro `<shapetype>` elemento.

Además, un tipo de forma no pertenece a ningún grupo. Por lo tanto, `<shapetype>` el elemento puede aparecer por sí mismo o dentro de un elemento `<group>` . Puede tener muchas formas dentro de grupos diferentes que hacen referencia al mismo tipo de forma. Si aparece un tipo de forma dentro de un grupo, una forma que se encuentra en otro grupo todavía puede hacer referencia a este tipo de forma.

Por ejemplo, en la siguiente representación de VML, Rect1 y Rect2 están en GroupA y Rect3 en GroupB. Se crea una instancia de los tres rectángulos a partir del tipo de forma MyShape.


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

 

 