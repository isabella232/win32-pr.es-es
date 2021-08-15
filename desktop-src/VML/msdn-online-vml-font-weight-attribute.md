---
title: Atributo de Font-Weight VML
description: Atributo de Font-Weight VML
ms.assetid: d7b2b0c5-b5cf-4e7d-bbca-c554d12bf97e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14dd5edb3fed869390edeff514471359162ee39fd1d78796af3d2a260c96bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754646"
---
# <a name="vml-font-weight-attribute"></a>Atributo de Font-Weight VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el grosor de las letras de la fuente. Lectura/escritura **Cadena**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* style="font-weight: *expression* ">

**Sintaxis de script**

*element* .style.fontweight="*expression*"

*expresión* = *elemento*.style.fontweight

**Comentarios:**

Los valores son los mismos que los atributos de estilo HTML estándar. Estos valores incluyen:



| Valor   | Descripción                                                                 |
|---------|-----------------------------------------------------------------------------|
| normal  | Normal. Predeterminada.                                                            |
| negrita    | Negrita.                                                                       |
| bolder  | Más pesado de lo normal.                                                        |
| lighter | Más ligera de lo normal.                                                        |
| 100     | Al menos tan ligero como 200 pesos.                                        |
| 200     | Al menos tan negrita como 100 peso y al menos tan ligera como 300. |
| 300     | Al menos tan negrita como el peso 200 y al menos tan claro como el peso 400. |
| 400     | Normal.                                                                     |
| 500     | Al menos tan negrita como el peso 400 y al menos tan claro como el peso 600. |
| 600     | Al menos tan negrita como el peso 500 y al menos tan claro como el peso 700. |
| 700     | Negrita.                                                                       |
| 800     | Al menos tan negrita como el peso 700 y al menos tan claro como el peso 900. |
| 900     | Al menos tan negrita como el peso 800.                                         |



 

*Atributo estándar de VML*

**Ejemplo**

El grosor de la fuente es negrita.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal bold 36pt Arial"/>
   </v:line>
```



 

 