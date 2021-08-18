---
title: Atributo principal de VML
description: Atributo principal de VML
ms.assetid: faad0c76-3566-4a51-962b-971667df2025
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60176fc9ac60f62c3692fa29b54fde4af8277d1c35fb2204768911d2bd8ae1f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119395825"
---
# <a name="vml-top-attribute"></a>Atributo principal de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la posición de la forma con respecto al elemento situado encima de ella en el flujo de la página. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="top: *expression* ">

**Sintaxis de script**

*element* .style.top="*expression*"

*expresión* = *elemento*.style.top

**Comentarios:**

El **atributo Top** es similar al atributo HTML **Top** estándar para los estilos.

Las unidades se pueden asignar al elemento primario o pueden estar en unidades absolutas. Es posible que este atributo no se escriba para las formas delimitadas en línea.

Estos valores incluyen:



| Value      | Descripción                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posición predeterminada de un elemento en el flujo de la página.                                                                                                          |
| units      | Número con un designador de unidades absolutas (cm, mm, in, pt, pc o px) o un designador de unidades relativas (em o ex). Si no se da ninguna unidad, se suponen píxeles (px). |
| percentage | Valor expresado como porcentaje del alto del objeto primario.                                                                                                   |



 

*Atributo estándar de VML*

**Vea también**

[Unidades](msdn-online-vml-units.md)

**Ejemplo**

El borde superior de la forma está 5 píxeles por debajo del objeto que lo precede en el flujo de la página.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:5;left:1;width:20;height:20">
   </v:rect>
```



[Ejemplo de atributo superior](/previous-versions/bb264098(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 