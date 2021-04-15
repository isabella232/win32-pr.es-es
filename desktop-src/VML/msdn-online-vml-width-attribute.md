---
title: Atributo de ancho VML
description: Atributo de ancho VML
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b3d4917d76b3c8820186b04b2e77537e6a6ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695651"
---
# <a name="vml-width-attribute"></a>Atributo de ancho VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el ancho de la forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* style = "width: *Expression* " >

**Sintaxis de script**

*Element* . Style. width = "*expresión*"

*expresión* = de *elemento*. Style. width

**Comentarios:**

El atributo **ancho** es similar al atributo **ancho** HTML estándar para los estilos.

Las unidades se pueden asignar al elemento primario o pueden estar en unidades absolutas.

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

El ancho de la forma es 25.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:25;height:20">
   </v:rect>
```



[Ejemplo de atributo de ancho](/previous-versions/bb264101(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 