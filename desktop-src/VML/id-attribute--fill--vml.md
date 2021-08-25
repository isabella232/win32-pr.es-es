---
title: Atributo ID (Fill)(VML)
description: Atributo ID (Fill)(VML)
ms.assetid: 56865772-51bd-4729-8e56-6b00e3c6bed0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f317cef4d588444f5c01770dafd5b56af0d2bca48ee228ff789a11b46348bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007875"
---
# <a name="id-attribute-fillvml"></a>Atributo ID (Fill)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Nombre que proporciona un identificador único para un relleno. Lectura/escritura **Cadena**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* id=" *expression* ">

**Sintaxis de script**

*element* .id="*expression*"

*expresión* = *elemento*.id

**Comentarios:**

Use **id.** para hacer referencia a un relleno específico. Una vez que haya creado un relleno y le haya dado un identificador, puede usar el nombre del identificador cuando desee manipular el relleno.

*Atributo estándar de VML*

**Ejemplo**

La forma tiene un identificador de relleno denominado "myfill".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill id="myfill"/>
   </v:shape>
```



 

 