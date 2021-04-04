---
title: Atributo de Margin-Bottom VML
description: Atributo de Margin-Bottom VML
ms.assetid: c1101430-f4fc-4fa5-8e02-7cee126c2c1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35712733179a3c03dc291c4d5efcf4fee68c2865
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792766"
---
# <a name="vml-margin-bottom-attribute"></a>Atributo de Margin-Bottom VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica el borde inferior del rectángulo que contiene la forma en relación con el delimitador de la forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *elemento* margin-bottom = " *expresión* " >

**Sintaxis de script**

*Element* . marginbottom = "*expresión*"

*expresión* = de *elemento*. marginbottom

**Comentarios:**

El atributo **margin-bottom** es similar al atributo **margin-bottom de** HTML estándar que se usa con las hojas de estilos.

Tenga en cuenta que se utiliza **marginbottom** en lugar de **margin-bottom para el** scripting. Tenga en cuenta también que si la **posición** es **absoluta**, el margen no aparecerá para cambiar.

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

El margen inferior se establece en 25 píxeles.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-bottom:25px">
   </v:rect>
```



[Ejemplo de atributo margin-bottom](/previous-versions/bb229675(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 