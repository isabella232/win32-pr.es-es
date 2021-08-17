---
title: Atributo de altura de VML
description: Atributo de altura de VML
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49218b83834d0d276d458656376d1806089be00a2158f271e38a4ee8da8099c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136998"
---
# <a name="vml-height-attribute"></a>Atributo de altura de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica el alto de la forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="height: *expression* ">

**Sintaxis de script**

*element* .style.height="*expression*"

*expresión* = *elemento*.style.height

**Comentarios:**

El **atributo Height** es similar al atributo alto HTML estándar para los estilos. 

Las unidades se pueden asignar al elemento primario o pueden estar en unidades absolutas.

Estos valores incluyen:



| Value      | Descripción                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posición predeterminada de un elemento en el flujo de la página.                                                                                                          |
| units      | Número con un designador de unidades absolutas (cm, mm, in, pt, pc o px) o un designador de unidades relativas (em o ex). Si no se dan unidades, se asumen píxeles (px). |
| percentage | Valor expresado como un porcentaje del alto del objeto primario.                                                                                                   |



 

*Atributo estándar de VML*

**Vea también**

[Unidades](msdn-online-vml-units.md)

**Ejemplo**

El alto de la forma se establece en 30.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



[Ejemplo de atributo height](/previous-versions/bb229671(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 