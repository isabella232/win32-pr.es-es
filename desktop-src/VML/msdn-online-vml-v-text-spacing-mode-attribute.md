---
title: Atributo V-Text-Spacing-Mode de VML
description: Atributo V-Text-Spacing-Mode de VML
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42137e8c8ec401548c4e0b027a50f34813fc7b45b04c4568011617906ac8e1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057663"
---
# <a name="vml-v-text-spacing-mode-attribute"></a>Atributo V-Text-Spacing-Mode de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el modo para elpacing de letras. Lectura/escritura **Cadena**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* style="v-text-spacing-mode: *expression* ">

**Sintaxis de script**

*element* .style.v-text-spacing-mode="*expression*"

*expresión* = *elemento*.style.v-text-spacing-mode

**Comentarios:**

Los valores incluyen

-   **ajuste (valor** predeterminado)
-   **Seguimiento**

Este atributo determina si se quitará espacio entre cada letra (ajuste) o se agregará entre cada letra (seguimiento). El atributo [V-Text-Spacing](msdn-online-vml-v-text-spacing-attribute.md) define la cantidad de cambios de mayúsculas y minúsculas.

*Atributo estándar de VML*

**Ejemplo**

El tamaño de las letras entre cada letra aumenta en 200 unidades.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 