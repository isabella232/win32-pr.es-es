---
title: Atributo XScale de VML
description: Atributo XScale de VML
ms.assetid: b876201d-87d1-4795-8f7f-33712a8bf493
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9fa96e26fefe6036ec9108456ca0d034bee2ec0ab41bb91e0796e1ced1743a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754180"
---
# <a name="vml-xscale-attribute"></a>Atributo XScale de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si se usará una ruta de texto recta en lugar de la ruta de acceso de forma. Lectura/escritura **DvTriState**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* style="xscale: *expression* ">

**Sintaxis de script**

*element* .style.xscale="*expression*"

*expresión* = *elemento*.style.xscale

**Comentarios:**

Si **es True,** el texto se ejecuta a lo largo de una ruta de izquierda a derecha a lo largo del valor x del límite inferior de la forma. El valor predeterminado es **False**.

*Atributo estándar de VML*

**Ejemplo**

El texto aparecerá como si se hubiera dibujado en una línea horizontal, aunque el trazado de forma sea una diagonal.


```HTML
   <v:line from="100 100" to="400 400">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="xscale:true;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 