---
title: ID (atributo, Stroke) (VML)
description: ID (atributo, Stroke) (VML)
ms.assetid: 584b0e90-9d66-471b-a1d2-33a236c2ed8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efc9cfda1b7ddb359812d9ad28b37b851315da8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792405"
---
# <a name="id-attribute-strokevml"></a>ID (atributo, Stroke) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Nombre que proporciona un identificador único para un trazo. Lectura/escritura **Cadena**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: ID. de *elemento* = " *expresión* " >

**Sintaxis de script**

*Element* . ID = "*expresión*"

*expresión* = de identificador de *elemento*

**Comentarios:**

Use el **identificador** para hacer referencia a un trazo específico. Una vez que haya creado un trazo y dado un identificador, puede utilizar el nombre de identificador cuando desee manipular el trazo.

*Atributo estándar de VML*

**Ejemplo**

La forma tiene un ID. de trazo denominado "Stroke".


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke id="mystroke"/>
   </v:shape>
```



 

 