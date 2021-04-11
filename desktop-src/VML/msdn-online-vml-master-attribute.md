---
title: Atributo maestro VML
description: Atributo maestro VML
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d6c34fe49c107ed7ee1b4c1fb90d31bb07f17a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149611"
---
# <a name="vml-master-attribute"></a>Atributo maestro VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si un elemento **TipoForma** es un elemento principal. Lectura/escritura **VgTriState**.

**Se aplica a**

[TipoForma](msdn-online-vml-shapetype-element.md)

**Sintaxis de etiquetas**

<v: *Element* o:Master = " *expresión* " >

**Comentarios:**

Si es **true**, la forma **TipoForma** la representa el motor de representación. El valor predeterminado es **False**.

*Microsoft Office atributo Extensions*

**Ejemplo**

El elemento **TipoForma** es una forma maestra.


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 