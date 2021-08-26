---
title: Atributo HRef (Forma)(VML)
description: Atributo HRef (Forma)(VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe4b545aa27d311b0e1d0c73f0107aa6fdb357d524d3150ce6ab7dfb1e0f009
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072045"
---
# <a name="href-attribute-shapevml"></a>Atributo HRef (Forma)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define una dirección URL para una forma. Cuando se hace clic en la forma, el explorador cargará la dirección URL. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* href=" *expression* ">

**Sintaxis de script**

*Element* .href="*expression*"

*expresión* = *elemento*.href

**Comentarios:**

El **atributo HRef** es similar al atributo **HRef** HTML estándar de delimitadores.

El **uso de HRef** facilita la creación de botones interesantes en una página web.

*Atributo estándar de VML*

**Ejemplo**

Cuando se hace clic en el rectángulo, el explorador cargará el Microsoft Corporation página principal.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



[Ejemplo de atributo HRef](/previous-versions/bb229672(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 