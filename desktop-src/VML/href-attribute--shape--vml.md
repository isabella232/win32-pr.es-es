---
title: HRef (atributo, forma) (VML)
description: HRef (atributo, forma) (VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078278"
---
# <a name="href-attribute-shapevml"></a>HRef (atributo, forma) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define una dirección URL para una forma. Al hacer clic en la forma, el explorador cargará la dirección URL. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* href = " *expresión* " >

**Sintaxis de script**

*Element* . href = "*expresión*"

*expresión* = de *elemento*. href

**Comentarios:**

El atributo **href** es similar al atributo **href** de HTML estándar de los delimitadores.

El uso de **href** facilita la creación de botones interesantes en una página web.

*Atributo estándar de VML*

**Ejemplo**

Cuando se hace clic en el rectángulo, el explorador carga la Página principal de Microsoft Corporation.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



[Ejemplo del atributo href](/previous-versions/bb229672(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 