---
title: Atributo izquierdo de VML
description: Atributo izquierdo de VML
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17810d7635d4b8194f2bd2df258a900cb534581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488175"
---
# <a name="vml-left-attribute"></a>Atributo izquierdo de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina la posición de la forma en relación con el elemento que queda en el flujo del documento. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* style = "Left: *Expression* " >

**Sintaxis de script**

*Element* . Style. Left = "*expresión*"

*expresión* = de *Element*. Style. Left

**Comentarios:**

El atributo **izquierdo** es similar al atributo **izquierdo** HTML estándar para los estilos.

Las unidades se pueden asignar al elemento primario o pueden estar en unidades absolutas. Este atributo no se escribirá para las formas insertadas en línea.

Estos valores incluyen:



| Value      | Descripción                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automático       | Posición predeterminada de un elemento en el flujo de la página.                                                                                                          |
| units      | Número con un designador de unidades absolutas (cm, mm, PDA, PT, PC o PX) o un designador de unidades relativas (EM o ex). Si no se especifica ninguna unidad, se supone que se trata de píxeles (PX). |
| percentage | Valor expresado como porcentaje del ancho del objeto primario.                                                                                                    |



 

*Atributo estándar de VML*

**Vea también**

[Unidades](msdn-online-vml-units.md)

**Ejemplo**

El valor izquierdo de la forma se establece en 1 en el ejemplo siguiente.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Ejemplo de atributo](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md)de la izquierda. (Requiere Microsoft Internet Explorer 5 o posterior).

 

 