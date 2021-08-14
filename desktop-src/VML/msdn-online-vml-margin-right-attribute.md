---
title: Atributo de Margin-Right VML
description: Atributo de Margin-Right VML
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5569f4f89cbe5320cfc348f2e2929b986736412f4cb864a62dd4584bde43a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346463"
---
# <a name="vml-margin-right-attribute"></a>Atributo de Margin-Right VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica el borde derecho del rectángulo que contiene la forma en relación con el delimitador de forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="margin-right: *expression* ">

**Sintaxis de script**

*element* .style.marginright="*expression*"

*expresión* = *elemento*.style.marginright

**Comentarios:**

El **atributo Margin-Right** es similar al atributo estándar **margin-right** HTML que se usa con las hojas de estilos.

Tenga en cuenta **que se usa marginright** en lugar **de margin-right** para el scripting. Tenga en cuenta también que si **la posición** es **absoluta,** el margen no parecerá cambiar.

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

El margen derecho se establece en 25 píxeles.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



[Ejemplo de atributo margin-right](/previous-versions/bb229677(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 