---
title: Atributo VML V
description: Atributo VML V
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149369"
---
# <a name="vml-v-attribute"></a>Atributo VML V

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define los comandos que componen una ruta de acceso. Lectura/escritura **Cadena**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *elemento* v = " *expresión* " >

**Sintaxis de script**

*Element* . v = "*expresión*"

*expresión* = de *elemento*. v

**Comentarios:**

Invalida el atributo de **ruta de acceso** de una forma. Las coordenadas pueden ser números fijos, números relativos o referencias a fórmulas (usando el formato " @n ", donde n es un número de fórmula; por ejemplo, " @2 " hace referencia a la segunda fórmula de la matriz de fórmulas).

*Atributo estándar de VML*

**Ejemplo**

Se crea un rectángulo mediante el atributo **V** . Tenga en cuenta que se usa una letra minúscula L (comando **lineTo** ) después del primer conjunto de coordenadas delimitadas por comas.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 