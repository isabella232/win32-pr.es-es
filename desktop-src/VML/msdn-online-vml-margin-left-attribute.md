---
title: Atributo de Margin-Left VML
description: Atributo de Margin-Left VML
ms.assetid: 65488c47-06c2-4a8f-8d29-4837865465f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f98900e862f22f31ad444bc6fb6f372627eca1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359196"
---
# <a name="vml-margin-left-attribute"></a>Atributo de Margin-Left VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica el borde izquierdo del rectángulo que contiene la forma en relación con el delimitador de la forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* style = "margin-left: *Expression* " >

**Sintaxis de script**

*Element* . Style. MarginLeft = "*expresión*"

*expresión* = de *Element*. Style. MarginLeft

**Comentarios:**

El atributo **margin-left** es similar al atributo **margin-left de** HTML estándar que se usa con las hojas de estilos.

Tenga en cuenta que se usa **MarginLeft** en lugar de **margin-left** para scripting. Tenga en cuenta también que si la **posición** es **absoluta**, el margen no aparecerá para cambiar.

Esta propiedad se utiliza en lugar de la **izquierda** para las formas de Microsoft Word y Microsoft Excel que están flotando en una posición relativa a un punto de anclaje.

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

El margen izquierdo se establece en 25 píxeles.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-left:25px">
   </v:rect>
```



[Ejemplo de atributo margin-left](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 