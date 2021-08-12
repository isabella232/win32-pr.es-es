---
title: Atributo izquierdo de VML
description: Atributo izquierdo de VML
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c067b15281277a85f707f6152fa855c51ee49aba439b16c009f6ff029139a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599293"
---
# <a name="vml-left-attribute"></a>Atributo izquierdo de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina la posición de la forma con respecto al elemento que queda en el flujo de documento. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="left: *expression* ">

**Sintaxis de script**

*Element* .style.left="*expression*"

*expresión* = *elemento*.style.left

**Comentarios:**

El **atributo Left** es similar al atributo HTML **Left** estándar para los estilos.

Las unidades se pueden asignar al elemento primario o pueden estar en unidades absolutas. Este atributo no se escribirá para las formas delimitadas en línea.

Estos valores incluyen:



| Value      | Descripción                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posición predeterminada de un elemento en el flujo de la página.                                                                                                          |
| units      | Número con un designador de unidades absolutas (cm, mm, in, pt, pc o px) o un designador de unidades relativas (em o ex). Si no se dan unidades, se asumen píxeles (px). |
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



[Ejemplo de atributo izquierdo](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md). (Requiere Microsoft Internet Explorer 5 o superior).

 

 