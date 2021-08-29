---
title: Atributo MSO-Wrap-Edited de VML
description: Atributo MSO-Wrap-Edited de VML
ms.assetid: cb0e8618-e649-4a3c-9433-2be77c4b65f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb22fa0ebd87f21643abdcf5a76311431d55d8c98a1f0f90cafc1744579d5fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124305"
---
# <a name="vml-mso-wrap-edited-attribute"></a>Atributo MSO-Wrap-Edited de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si el usuario personalizó las coordenadas de encapsulado. Lectura/escritura **DvTriState**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="mso-wrap-edited: *expression* ">

**Comentarios:**

Si un editor genera las coordenadas de encapsulado, este atributo es **True**; De lo contrario, un usuario los personalizó.

*Microsoft Office Atributo Extensions*

**Ejemplo**

Las coordenadas de ajuste de la forma se generaron mediante un editor de formas.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-edited:True"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 