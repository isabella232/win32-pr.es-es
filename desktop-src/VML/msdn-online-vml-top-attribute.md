---
title: Atributo Top de VML
description: Atributo Top de VML
ms.assetid: faad0c76-3566-4a51-962b-971667df2025
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c76a39035bc3dd3f0ae348280561e614d7dab4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792333"
---
# <a name="vml-top-attribute"></a>Atributo Top de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la posición de la forma en relación con el elemento situado encima de él en el flujo de la página. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* style = "Top: *Expression* " >

**Sintaxis de script**

*Element* . Style.Top = "*expresión*"

*expresión* = de *elemento*. Style.Top

**Comentarios:**

El atributo **Top** es similar al atributo **Top** de HTML estándar para los estilos.

Las unidades se pueden asignar al elemento primario o pueden estar en unidades absolutas. Este atributo no se puede escribir para las formas alineadas en línea.

Estos valores incluyen:



| Value      | Descripción                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automático       | Posición predeterminada de un elemento en el flujo de la página.                                                                                                          |
| units      | Número con un designador de unidades absolutas (cm, mm, PDA, PT, PC o PX) o un designador de unidades relativas (EM o ex). Si no se especifica ninguna unidad, se supone que se trata de píxeles (PX). |
| percentage | Valor expresado como porcentaje del alto del objeto primario.                                                                                                   |



 

*Atributo estándar de VML*

**Vea también**

[Unidades](msdn-online-vml-units.md)

**Ejemplo**

El borde superior de la forma es de 5 píxeles por debajo del objeto que lo precede en el flujo de la página.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:5;left:1;width:20;height:20">
   </v:rect>
```



[Ejemplo de atributo Top](/previous-versions/bb264098(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 