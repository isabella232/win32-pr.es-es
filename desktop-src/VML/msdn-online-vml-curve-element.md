---
title: Elemento Curve de VML
description: Elemento Curve de VML
ms.assetid: 37197ef0-7597-465a-bc37-7ffcde2e736b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fd06480b0d4bcf062f1f64eb9fa0b22862cf2b338b2c2f5ea0bf1c3cd2a1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655535"
---
# <a name="vml-curve-element"></a>Elemento Curve de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Forma de curva predefinida.

**Curve** usa los [atributos a](to-attribute--curve--vml.md), [de](from-attribute--curve--vml.md), [control1](msdn-online-vml-control1-attribute.md)y [control2.](msdn-online-vml-control2-attribute.md)

A continuación se muestra el código mínimo necesario para generar una imagen.


```HTML
   <v:curve
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```





 

 