---
title: Atributo de clase VML
description: Atributo de clase VML
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94bdc723ba9be335afc43023ab89b88834c55474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995419"
---
# <a name="vml-class-attribute"></a>Atributo de clase VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Hace referencia a una definición de un estilo CSS. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* Class = " *expresión* " >

**Sintaxis de script**

*Element* . className = "*expresión*"

*expresión* = de *elemento*. ClassName

**Comentarios:**

El atributo **Class** es similar al atributo de **clase** HTML estándar que se usa con hojas de estilos CSS.

Tenga en cuenta que **className** se usa en lugar de la **clase** para el scripting. Tenga en cuenta también que para el scripting, **className** solo se puede leer; Si se cambia el valor de **className** , no se cambiará la representación de la forma.

*Atributo estándar de VML*

**Vea también**

[Forma](shape-element--vml.md)

**Ejemplo**

Una clase para el **ancho** se crea con el estilo


```HTML
   .narrowstyle {width:50;height:100}
```



A continuación, se hace referencia al ancho incluyendo el estilo. Tenga en cuenta que el ancho andheight no está definido en el atributo de **estilo** , pero lo definirá el estilo.


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



Tenga en cuenta que la **clase** solo se aplica a los atributos de tipo CSS.

 

 