---
title: Atributo ID (Stroke)(VML)
description: Atributo ID (Stroke)(VML)
ms.assetid: 584b0e90-9d66-471b-a1d2-33a236c2ed8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02fa8ad958315af58e2abfa6d374a6545cc1e3e171080ec29ac6a30600160184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125308"
---
# <a name="id-attribute-strokevml"></a>Atributo ID (Stroke)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Nombre que proporciona un identificador único para un trazo. Lectura/escritura **Cadena**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* id=" *expression* ">

**Sintaxis de script**

*element* .id="*expression*"

*expresión* = *elemento*.id

**Comentarios:**

Use **id.** para hacer referencia a un trazo específico. Una vez que haya creado un trazo y le haya dado un identificador, puede usar el nombre del identificador cuando desee manipular el trazo.

*Atributo estándar de VML*

**Ejemplo**

La forma tiene un identificador de trazo llamado "mystroke".


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke id="mystroke"/>
   </v:shape>
```



 

 