---
title: Atributo de Margin-Bottom VML
description: Atributo de Margin-Bottom VML
ms.assetid: c1101430-f4fc-4fa5-8e02-7cee126c2c1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551cf9cba00901e07998f2de38465cba1cb45bb8f563c04d1adf25f75d1852bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057823"
---
# <a name="vml-margin-bottom-attribute"></a>Atributo de Margin-Bottom VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica el borde inferior del rectángulo que contiene la forma en relación con el delimitador de forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* margin-bottom=" *expression* ">

**Sintaxis de script**

*element* .marginbottom="*expression*"

*expresión* = *elemento*.marginbottom

**Comentarios:**

El **atributo Margin-Bottom** es similar al atributo **margin-bottom** HTML estándar que se usa con las hojas de estilos.

Tenga en cuenta **que se usa marginbottom** en lugar **de margin-bottom** para scripting. Tenga en cuenta también que si **la posición** es **absoluta,** el margen no parecerá cambiar.

Estos valores incluyen:



| Valor      | Descripción                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posición predeterminada de un elemento en el flujo de la página.                                                                                                                                           |
| units      | Predeterminada. Número con un designador de unidades absolutas (cm, mm, in, pt, pc o px) o un designador de unidades relativas (em o ex). Si no se da ninguna unidad, se suponen píxeles (px). El valor predeterminado es 0. |
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



[Ejemplo de atributo margin-bottom](/previous-versions/bb229675(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 