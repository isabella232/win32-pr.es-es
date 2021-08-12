---
title: Atributo de nivel bi de VML
description: Atributo de nivel bi de VML
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6831b84f77777cfa21a5bd5c80cb59e447c5a5ce1da78875cc9bd5ff07548690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602875"
---
# <a name="vml-bilevel-attribute"></a>Atributo de nivel bi de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si una imagen se mostrará en blanco y negro. Lectura/escritura **DvTriState**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *element* bilevel=" *expression* ">

**Sintaxis de script**

*element* .bilevel="*expression*"

*expresión* = *elemento*.bilevel

**Comentarios:**

Si **es True,** la imagen se mostrará con dos colores (blanco y negro). El valor predeterminado es **False**. Esto crea un efecto similar a la pósterización.

*Atributo estándar de VML*

**Ejemplo**

La imagen solo se mostrará en blanco y negro.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 