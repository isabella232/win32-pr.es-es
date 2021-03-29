---
title: ID (atributo, sombra) (VML)
description: ID (atributo, sombra) (VML)
ms.assetid: ca20b6b9-a41c-4073-9178-77eb0f918327
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d51a5917f9ef71e3c4acea7ec1ed2e5cf90aef8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792406"
---
# <a name="id-attribute-shadowvml"></a>ID (atributo, sombra) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica un nombre que proporciona un identificador único para una sombra. Lectura/escritura **Cadena**.

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: ID. de *elemento* = " *expresión* " >

**Sintaxis de script**

*Element* . ID = "*expresión*"

*expresión* = de identificador de *elemento*

**Comentarios:**

Use el **identificador** para hacer referencia a una sombra específica. Una vez que haya creado una sombra y dado un identificador, puede utilizar el nombre de identificador cuando desee manipular la sombra.

*Atributo estándar de VML*

**Ejemplo**

La forma tiene un ID. de sombra denominado "prevaleci".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow id="myshadow" on="True"/>
   </v:shape>
```



 

 