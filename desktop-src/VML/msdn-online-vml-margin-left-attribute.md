---
title: Atributo de Margin-Left VML
description: Atributo de Margin-Left VML
ms.assetid: 65488c47-06c2-4a8f-8d29-4837865465f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f403c19e617f8131886d3f4a862ff1ac0b878edbd2acf2fd0e27cb17b3406c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680827"
---
# <a name="vml-margin-left-attribute"></a>Atributo de Margin-Left VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica el borde izquierdo del rectángulo que contiene la forma en relación con el delimitador de forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="margin-left: *expression* ">

**Sintaxis de script**

*element* .style.marginleft="*expression*"

*expresión* = *elemento*.style.marginleft

**Comentarios:**

El **atributo Margin-Left** es similar al atributo estándar HTML **Margin-Left** que se usa con las hojas de estilos.

Tenga en cuenta **que se usa marginleft** en lugar **de margin-left** para scripting. Tenga en cuenta también que si **la posición** es **absoluta,** el margen no parecerá cambiar.

Esta propiedad se usa en lugar de **Left** para las formas Microsoft Word y Microsoft Excel que están flotantes en una posición relativa a un punto delimitador.

Estos valores incluyen:



| Value      | Descripción                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posición predeterminada de un elemento en el flujo de la página.                                                                                                                                           |
| units      | Predeterminada. Número con un designador de unidades absolutas (cm, mm, in, pt, pc o px) o un designador de unidades relativas (em o ex). Si no se da ninguna unidad, se suponen píxeles (px). El valor predeterminado es 0. |
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



[Ejemplo de atributo margin-left](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples). (Requiere Microsoft Internet Explorer 5 o superior).

 

 