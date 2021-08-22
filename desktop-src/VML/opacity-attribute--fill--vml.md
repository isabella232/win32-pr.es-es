---
title: Atributo Opacity (Fill)(VML)
description: Atributo Opacity (Fill)(VML)
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ea4f539eb2386dae7b8e863c95556cf70400c320ee515897cf7f96a85fe3ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057603"
---
# <a name="opacity-attribute-fillvml"></a>Atributo Opacity (Fill)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la transparencia de un relleno. Lectura/escritura [Accionario](msdn-online-vml-vgfraction-data-type.md).

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* opacity=" *expression* ">

**Sintaxis de script**

*element* .opacity="*expression*"

*expresión* = *element*.opacity

**Comentarios:**

El valor predeterminado es 1,0.

*Atributo estándar de VML*

**Ejemplo**

El relleno de la forma será 50 % transparente.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 