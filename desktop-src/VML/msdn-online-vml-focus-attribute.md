---
title: Atributo de foco de VML
description: Atributo de foco de VML
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b60eeb9ff379c8006cbb9068b6b78c8f24490ecf2fd15573b5b224a9ee1208ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057873"
---
# <a name="vml-focus-attribute"></a>Atributo de foco de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el centro de un relleno de degradado lineal. Lectura/escritura **Accionario**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* focus=" *expression* ">

**Sintaxis de script**

*element* .focus="*expression*"

*expresión* = *elemento*.focus

**Comentarios:**

Define la posición inicial central de la mezcla. Los valores oscilan entre 100 % y -100 %. El valor predeterminado es 0. Un valor de 100 % (o -100 %) desplazará el foco para que la dirección de la mezcla se revierta (en efecto, invierta **Color** y **Color2).** Un valor del 50 % cambiará la mezcla para que **Color** esté en ambos extremos y **Color2** en el centro. Un valor de -50 % cambiará la mezcla para que **Color2** esté en ambos extremos y **Color** esté en el centro.

*Atributo estándar de VML*

**Ejemplo**

El foco de degradado del relleno se desplaza para que el rojo **(Color)** sea una banda en el centro de la forma y que la parte superior e inferior sea azul **(Color2).**


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 