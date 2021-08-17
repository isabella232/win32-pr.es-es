---
title: Atributo V-Text-Align de VML
description: Atributo V-Text-Align de VML
ms.assetid: ca2cbbf6-ddbb-4f2b-942c-3fe0033bd649
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bf8ec2e781b04e7ababc0b30ea3996e569e5cf9066a4bac072806fd7329eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117939134"
---
# <a name="vml-v-text-align-attribute"></a>Atributo V-Text-Align de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la alineación del texto. Lectura/escritura **Cadena**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* style="v-text-align: *expression* ">

**Sintaxis de script**

*element* .style.v-text-align="*expression*"

*expresión* = *elemento*.style.v-text-align

**Comentarios:**

Estos valores incluyen:

-   **left** (valor predeterminado)
-   **Correcto**
-   **Centro**
-   **Justificar**
-   **letter-justify**
-   **stretch-justify**

*Atributo estándar de VML*

**Ejemplo**

El texto se extenderá para ajustarse a la ruta de acceso, pero el espacio adicional se colocará entre cada letra.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-align:letter-justify;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 