---
title: Atributo del método VML
description: Atributo del método VML
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d6b5ae67f94a2fc6e27451fb1a947c8341d1f77c08a721ca7946250cee3b7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124768"
---
# <a name="vml-method-attribute"></a>Atributo del método VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el método utilizado para generar un relleno de degradado. Lectura/escritura **DvsigmaType**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* method=" *expression* ">

**Sintaxis de script**

*element* .method="*expression*"

*expresión* = *element*.method

**Comentarios:**

Estos valores incluyen:



| Value  | Descripción          |
|--------|----------------------|
| Ninguno   | Sin relleno sigma.       |
| Lineal | Relleno sigma lineal.   |
| Sigma  | Relleno sigma. Predeterminada. |
| Any    | Cualquier relleno sigma.      |



 

*Atributo estándar de VML*

**Ejemplo**

La forma tendrá un relleno de degradado lineal rojo.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 