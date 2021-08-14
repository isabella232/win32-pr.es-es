---
title: Atributo de visibilidad de VML
description: Atributo de visibilidad de VML
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2087a8c5915b400f32f6007d58c5c20344f9abab1e2c5bc5d4c93da74ddf1182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346187"
---
# <a name="vml-visibility-attribute"></a>Atributo de visibilidad de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si se muestra una forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="visibility: *expression* ">

**Sintaxis de script**

*element* .style.visibility="*expression*"

*expresión* = *elemento*.style.visibility

**Comentarios:**

El **atributo Visibility** es similar al atributo de visibilidad HTML estándar para los estilos. 

Estos valores incluyen:



| Valor    | Descripción                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| visible  | La forma es visible.                                                                                                                                                                   |
| hidden   | La forma no es visible, pero sigue formando parte del flujo de los objetos en el explorador. Los eventos del mouse no se procesan.                                                                  |
| inherit  | Predeterminada. El estado de visibilidad se hereda del elemento primario de la forma. Microsoft Office aplicaciones solo usan **inherit** y **hidden**; cualquier otro valor se asigna para **heredar**. |
| contraer | Se usa para aplicaciones de edición gráfica que pueden contraer grupos de formas; por ejemplo, los esquemas.                                                                                     |



 

*Atributo estándar de VML*

**Ejemplo**

El código siguiente crea una forma, pero la oculta. Otros objetos del documento fluirán a su alrededor, dejando un espacio del mismo tamaño que la forma.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



[Ejemplo de atributo de visibilidad](/previous-versions/bb264100(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 