---
title: Atributo ConnectorType de VML
description: Atributo ConnectorType de VML
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a552324582729c74ae87c9fcf1cd512334423bb84c43992f265c0b47fffcd98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601978"
---
# <a name="vml-connectortype-attribute"></a>Atributo ConnectorType de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Indica el tipo de conector utilizado para unir formas. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* o:connectortype=" *expression* ">

**Comentarios:**

Estos valores incluyen:



| Value    | Descripción                    |
|----------|--------------------------------|
| ninguno     | Sin conector.                  |
| Recto | Predeterminada. Conector derecho. |
| Codo    | Conector en forma de anillo.     |
| Curvado   | Conector curvado.            |



 

Un motor de reglas de un editor gráfico también puede usar este atributo.

*Microsoft Office Atributo Extensions*

**Ejemplo**

La forma usa una línea recta como conector.


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 