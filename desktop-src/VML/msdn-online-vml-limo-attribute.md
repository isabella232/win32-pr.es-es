---
title: Atributo VmL Limo
description: Atributo VmL Limo
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa99325f396a3e4709fcd7ca1ee6ee82df1b653dff50df56df2df06ef2d513ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598315"
---
# <a name="vml-limo-attribute"></a>Atributo VmL Limo

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define un punto de extensión en la ruta de acceso. Lectura/escritura **Vector2D**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *element* limo=" *expression* ">

**Sintaxis de script**

*element* .limo="*expression*"

*expresión* = *elemento*.limo

**Comentarios:**

El valor predeterminado es "0 0". Los stretchs de limusina son puntos en el borde de una forma que definen dónde y cómo un usuario puede extender una forma en un editor gráfico.

*Atributo estándar de VML*

**Ejemplo**

Un punto de stretch de limusina se define a medio camino a lo largo de la línea horizontal.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 