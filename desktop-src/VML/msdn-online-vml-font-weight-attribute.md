---
title: Atributo de Font-Weight VML
description: Atributo de Font-Weight VML
ms.assetid: d7b2b0c5-b5cf-4e7d-bbca-c554d12bf97e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e4de8a1bb4132c75d4520dcacc661fbbc97eef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420927"
---
# <a name="vml-font-weight-attribute"></a>Atributo de Font-Weight VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el grosor de las letras de la fuente. Lectura/escritura **Cadena**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *Element* style = "font-weight: *Expression* " >

**Sintaxis de script**

*Element* . Style. FontWeight = "*expresión*"

*expresión* = de *Element*. Style. FontWeight

**Comentarios:**

Los valores son los mismos que los atributos de estilo HTML estándar. Estos valores incluyen:



| Value   | Descripción                                                                 |
|---------|-----------------------------------------------------------------------------|
| normal  | Normal. Predeterminada.                                                            |
| negrita    | Negrita.                                                                       |
| bolder  | Más pesado que normal.                                                        |
| lighter | Más claro que normal.                                                        |
| 100     | Al menos tan ligero como el peso 200.                                        |
| 200     | Al menos como negrita como el peso 100 y al menos tan ligero como el peso 300. |
| 300     | Al menos como negrita como el peso 200 y al menos tan ligero como el peso 400. |
| 400     | Normal.                                                                     |
| 500     | Al menos como negrita como el peso 400 y al menos tan ligero como el peso 600. |
| 600     | Al menos como negrita como el peso 500 y al menos tan ligero como el peso 700. |
| 700     | Negrita.                                                                       |
| 800     | Al menos como negrita como el peso 700 y al menos tan ligero como el peso 900. |
| 900     | Al menos como negrita como el peso 800.                                         |



 

*Atributo estándar de VML*

**Ejemplo**

El espesor de la fuente está en negrita.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal bold 36pt Arial"/>
   </v:line>
```



 

 