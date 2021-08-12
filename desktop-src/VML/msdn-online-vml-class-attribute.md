---
title: Atributo de clase VML
description: Atributo de clase VML
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ada95b56430dacd09801a9aaa200c92abab064bbbb5732b369372de63c34de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602192"
---
# <a name="vml-class-attribute"></a>Atributo de clase VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Hace referencia a una definición de un estilo CSS. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* class=" *expression* ">

**Sintaxis de script**

*element* .classname="*expression*"

*expresión* = *element*.classname

**Comentarios:**

El **atributo de** clase es similar al atributo de clase HTML estándar que se usa con hojas de estilos CSS. 

Tenga en cuenta **que classname** se usa en lugar de **la clase para** el scripting. Tenga en cuenta también que para el scripting, **el nombre de** clase solo se puede leer; Cambiar el valor de **classname** no cambiará la representación de la forma.

*Atributo estándar de VML*

**Vea también**

[Forma](shape-element--vml.md)

**Ejemplo**

Se crea una **clase para width** con el estilo


```HTML
   .narrowstyle {width:50;height:100}
```



A continuación, se hace referencia al ancho incluyendo el estilo . Tenga en cuenta que el ancho y la vista no están definidos en el atributo **de** estilo, pero se definirán mediante el estilo.


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



Tenga en **cuenta que La** clase solo se aplica a los atributos de tipo CSS.

 

 