---
title: Atributo ForceDash de VML
description: Atributo ForceDash de VML
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bcec4a694a6449412aa07ec69aa9a817aa917c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078062"
---
# <a name="vml-forcedash-attribute"></a>Atributo ForceDash de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si un contorno discontinuo se usa para dibujar una forma cuando una forma no tiene línea ni relleno. Lectura/escritura **VgTriState**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* o:forcedash = " *expresión* " >

**Comentarios:**

Lo usan los marcadores de posición de Microsoft PowerPoint para dibujar un contorno discontinuo cuando no hay ninguna línea y ningún relleno para una forma. El valor predeterminado es **false**. Si **es true**, se utilizará un contorno discontinuo para indicar un marcador de posición.

*Microsoft Office atributo Extensions*

**Ejemplo**

Se utilizará una línea discontinua para representar la forma si no hay ninguna línea o relleno.


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 