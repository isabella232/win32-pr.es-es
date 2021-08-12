---
title: Atributo de Layout-Flow VML
description: Atributo de Layout-Flow VML
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde6937a3f93ff2a462cfc5950c13b7f3910573c54d82449ef705bca4afbb068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599359"
---
# <a name="vml-layout-flow-attribute"></a>Atributo de Layout-Flow VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina el flujo del diseño de texto en un cuadro de texto. Lectura/escritura **Cadena**.

**Se aplica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxis de etiquetas**

<v: *element* style="layout-flow: *expression* ">

**Comentarios:**

Estos valores incluyen:



| Value                  | Descripción                                 |
|------------------------|---------------------------------------------|
| horizontal             | El texto se muestra horizontalmente. Predeterminada.    |
| Vertical               | El texto se muestra verticalmente.               |
| ideografía vertical   | El texto ideográfico se muestra verticalmente.   |
| horizontal-ideographic | El texto ideográfico se muestra horizontalmente. |



 

*Atributo estándar de VML*

**Ejemplo**

El flujo de texto del cuadro de texto fluirá verticalmente.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 