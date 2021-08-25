---
title: Atributo ID (VML)
description: Atributo ID (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0ba0addd2d6af8a8b38af4085c79123d3178a3299269468abd73fff1951d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007865"
---
# <a name="id-attribute-vml"></a>Atributo ID (VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Proporciona un identificador único para un elemento. Lectura/escritura **Cadena**.

**Se aplica a**

Todos los elementos VML.

**Sintaxis de etiquetas**

<v: *elementname* id=" *idname* ">

**Sintaxis de script**

*elementname* .id =" *idname* "

*expresión* = *elementname*.id

**Comentarios:**

Use **id.** para hacer referencia a un elemento específico. Una vez que haya creado una forma y le haya dado un identificador, puede usar el nombre del identificador cuando desee manipular el elemento.

**El** identificador es necesario para usar el [elemento ShapeType.](msdn-online-vml-shapetype-element.md)

Cuando vml se genera mediante Microsoft Office, si se asigna un nombre  de modelo de objetos a la forma, el identificador se establece en este nombre. Si no se establece el nombre del modelo de objetos, el nombre se genera mediante *spid* (identificador de forma interno) más un prefijo (S para la forma, M para la forma maestra, T para shapetype).

*Atributo estándar de VML*.

**Ejemplo**

Para cambiar los atributos de una forma, primero debe dar un identificador a la forma. por ejemplo, "myrect".


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



[Ejemplo de atributo id.](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example) (Requiere Microsoft Internet Explorer 5 o superior).

 

 