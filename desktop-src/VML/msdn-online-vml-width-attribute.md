---
title: Atributo de ancho de VML
description: Atributo de ancho de VML
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385aee5c45f68d039bc1bcf6bd3b0c52db0871640bc8a2df3a7f25e9e2bdc205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117938962"
---
# <a name="vml-width-attribute"></a>Atributo de ancho de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el ancho de la forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="width: *expression* ">

**Sintaxis de script**

*element* .style.width="*expression*"

*expresión* = *elemento*.style.width

**Comentarios:**

El **atributo Width** es similar al atributo ancho HTML estándar para los estilos. 

Las unidades se pueden asignar al elemento primario o pueden estar en unidades absolutas.

Estos valores incluyen:



| Value      | Descripción                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posición predeterminada de un elemento en el flujo de la página.                                                                                                          |
| units      | Número con un designador de unidades absolutas (cm, mm, in, pt, pc o px) o un designador de unidades relativas (em o ex). Si no se da ninguna unidad, se suponen píxeles (px). |
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



[Ejemplo de atributo de ancho](/previous-versions/bb264101(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 