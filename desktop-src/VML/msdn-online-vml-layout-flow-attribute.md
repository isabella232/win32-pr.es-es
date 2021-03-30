---
title: Atributo de Layout-Flow VML
description: Atributo de Layout-Flow VML
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e437e31043afcf7fba4967076a861c9bca86477
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995417"
---
# <a name="vml-layout-flow-attribute"></a>Atributo de Layout-Flow VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina el flujo del diseño de texto en un cuadro de texto. Lectura/escritura **Cadena**.

**Se aplica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxis de etiquetas**

<v: *Element* style = "layout-Flow: *Expression* " >

**Comentarios:**

Estos valores incluyen:



| Value                  | Descripción                                 |
|------------------------|---------------------------------------------|
| horizontal             | El texto se muestra horizontalmente. Predeterminada.    |
| vertical               | El texto se muestra verticalmente.               |
| ideográfica vertical   | El texto ideográfico se muestra verticalmente.   |
| ideográfico horizontal | El texto ideográfico se muestra horizontalmente. |



 

*Atributo estándar de VML*

**Ejemplo**

El flujo de texto en el cuadro de texto se fluirá verticalmente.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 