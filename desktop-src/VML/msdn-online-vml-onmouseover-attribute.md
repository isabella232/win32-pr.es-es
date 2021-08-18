---
title: Atributo OnMouseOver de VML
description: Atributo OnMouseOver de VML
ms.assetid: 68f0fa7a-0d22-4ede-8404-e007296960e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d2bb65864987988996cfad710360fd908a5248c11857e8df1eb5a941b1b895b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999135"
---
# <a name="vml-onmouseover-attribute"></a>Atributo OnMouseOver de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Desencadena un evento del mouse para una forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* onmouseover=" *expression* ">

**Comentarios:**

Se genera un evento "mouseover" cuando el puntero del mouse está en la forma. El valor se genera mediante la palabra clave **this** (como referencia al objeto ) seguida de la sintaxis del modelo de objetos. Por ejemplo, para cambiar el color de relleno a rojo, use lo siguiente:

onmouseover="this.fillcolor='red'"

Observe el uso de comillas simples y dobles para desactivar la expresión.

*Atributo estándar de VML*

**Ejemplo**

Cuando el puntero del mouse está en la forma, el color de relleno pasará de rojo a verde.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20"
   onmouseover='this.fillcolor="green"'>
   </v:rect>
```



[Ejemplo de atributo OnMouseOver](/previous-versions/bb264088(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 