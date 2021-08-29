---
title: Atributo StartAngle de VML
description: Atributo StartAngle de VML
ms.assetid: 334ae52a-cde4-427e-8080-ec789b4d9d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7237c20acb3e2b9a5b2445dc1ffed4e23a93bb55958831f5607410cde092dbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796165"
---
# <a name="vml-startangle-attribute"></a>Atributo StartAngle de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el punto inicial del arco. Lectura y escritura. [DvangleInDegrees.](msdn-online-vml-vgangleindegrees-data-type.md)

**Se aplica a**

[Arc](msdn-online-vml-arc-element.md)

**Sintaxis de etiquetas**

<v: *element* endangle=" *expression* ">

**Sintaxis de script**

*Element* .endAngle="*expression*"

*expresión* = *elemento*.endAngle

**Comentarios:**

El arco se define como un trazo dibujado a lo largo de un óvalo delimitado por los atributos **Style** de una forma. El inicio del trazo se define mediante un ángulo medido desde la derecha hacia arriba (12 en punto) en el sentido de las agujas del reloj. El valor predeterminado es 0 grados.

Atributo estándar de VML

**Ejemplo**

El arco está sonriente. El punto inicial está en el punto de 90 grados de un óvalo inscrito dentro del cuadro de límite de forma. El punto final está en el punto de 270 grados del óvalo.


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 