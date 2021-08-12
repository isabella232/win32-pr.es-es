---
title: Atributo inset de VML
description: Atributo inset de VML
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1d4b44756034a3ebc7e46e1cdda43042f347e58cb87c02b00c90a14320a40f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600241"
---
# <a name="vml-inset-attribute"></a>Atributo inset de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica los valores de margen interno para el texto del cuadro de texto. Lectura/escritura **Cadena**.

**Se aplica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxis de etiquetas**

<v: *element* inset=" *expression* ">

**Sintaxis de script**

*Element* .inset="*expression*"

*expresión* = *elemento*.inset

**Comentarios:**

El valor de margen de texto interno se especifica como una cadena que contiene cuatro valores, cada uno separado por comas o espacios. Los valores miden el conjunto de los bordes izquierdo, superior, derecho e inferior del cuadro especificado por el atributo [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) de **Path**. Los valores que faltan se establecen en el valor predeterminado, que es "0.1in, 0.05in, 0.1in, 0.05in".

En el caso de las formas giradas en exploradores que no admiten la rotación, el cuadro de límite se ajustará al múltiplo más cercano de 90 grados.

*Atributo estándar de VML*

**Ejemplo**

El cuadro de texto tendrá un margen de conjunto de 10 píxeles.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 