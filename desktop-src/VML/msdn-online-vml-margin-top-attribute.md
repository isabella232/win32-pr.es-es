---
title: Atributo de Margin-Top VML
description: Atributo de Margin-Top VML
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e42d86ba6e0fe05c2b0dff1f6d8bdabba0100fffee97d489fd59360cb8e13bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346401"
---
# <a name="vml-margin-top-attribute"></a>Atributo de Margin-Top VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica el borde superior del rectángulo que contiene la forma en relación con el delimitador de forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* margin-top=" *expression* ">

**Sintaxis de script**

*Element* .margin-top="*expression*"

*expresión* = *elemento*.margin-top

**Comentarios:**

El **atributo Margin-Top** es similar al atributo estándar **margin-top** html que se usa con las hojas de estilos.

Tenga en cuenta **que se usa margintop** en lugar **de margin-top** para el scripting. Tenga en cuenta también que **si la posición** es **absoluta,** el margen no parecerá cambiar.

Esta propiedad se usa en lugar de **Top** para las formas de Microsoft Word y Microsoft Excel que están flotantes en una posición relativa a un punto delimitador.

Estos valores incluyen:



| Valor      | Descripción                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posición predeterminada de un elemento en el flujo de la página.                                                                                                                                           |
| units      | Predeterminada. Número con un designador de unidades absolutas (cm, mm, in, pt, pc o px) o un designador de unidades relativas (em o ex). Si no se dan unidades, se asumen píxeles (px). El valor predeterminado es 0. |
| percentage | Valor expresado como un porcentaje del alto del objeto primario.                                                                                                                                    |



 

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



[Ejemplo de atributo margin-top](/previous-versions/bb264087(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 