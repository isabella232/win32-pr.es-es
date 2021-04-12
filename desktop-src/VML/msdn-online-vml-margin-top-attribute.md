---
title: Atributo de Margin-Top VML
description: Atributo de Margin-Top VML
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14b6f4743f04740fe3fdbac4cc1d03f7bbe0282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359397"
---
# <a name="vml-margin-top-attribute"></a>Atributo de Margin-Top VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica el borde superior del rectángulo que contiene la forma en relación con el delimitador de la forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *elemento* margin-top = " *expresión* " >

**Sintaxis de script**

*Element* . margin-top = "*expresión*"

*expresión* = de *elemento*. margin-top

**Comentarios:**

El atributo **margin-top** es similar al atributo **margin-top** de HTML estándar que se usa con las hojas de estilos.

Tenga en cuenta que se utiliza **marginTop** en lugar de **margin-top** para el scripting. Tenga en cuenta también que si la **posición** es **absoluta**, el margen no aparecerá para cambiar.

Esta propiedad se utiliza en lugar de la **parte superior** para las formas de Microsoft Word y Microsoft Excel que están flotando en una posición relativa a un punto de anclaje.

Estos valores incluyen:



| Value      | Descripción                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automático       | Posición predeterminada de un elemento en el flujo de la página.                                                                                                                                           |
| units      | Predeterminada. Número con un designador de unidades absolutas (cm, mm, PDA, PT, PC o PX) o un designador de unidades relativas (EM o ex). Si no se especifica ninguna unidad, se supone que se trata de píxeles (PX). El valor predeterminado es 0. |
| percentage | Valor expresado como porcentaje del alto del objeto primario.                                                                                                                                    |



 

*Atributo estándar de VML*

**Vea también**

[Unidades](msdn-online-vml-units.md)

**Ejemplo**

El margen superior se establece en 25 píxeles.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



[Ejemplo de atributo margin-top](/previous-versions/bb264087(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 