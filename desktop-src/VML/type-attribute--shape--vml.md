---
title: Atributo de tipo (forma) (VML)
description: Atributo de tipo (forma) (VML)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e53b275d6b6327b3d3783704dbd06156e643f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077910"
---
# <a name="type-attribute-shapevml"></a>Atributo de tipo (forma) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define una referencia al identificador de un elemento [TipoForma](msdn-online-vml-shapetype-element.md) . Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

``` syntax
<v:
          element 
          type=" expression ">
```

**Sintaxis de script**

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

**Comentarios:**

Si el atributo de **tipo** hace referencia al identificador de un elemento **TipoForma** , los rellenos, rutas de acceso y trazos del **TipoForma** se usan como plantillas para crear la forma. Los valores que se derivan de **TipoForma** se pueden reemplazar por valores de forma individuales.

Si se utiliza en etiquetas, el valor de cadena debe comenzar por un símbolo de número ( \# ).

**Atributo estándar de VML**

**Ejemplo**

Una forma **TipoForma** se crea con el "tipo" como identificador.


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



A continuación, si crea una forma con los valores de **TipoForma** , la forma tendrá los atributos de "mi tipo" **TipoForma**; es decir, "shape01" tendrá un relleno rojo con un trazo azul.


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



Puede invalidar los valores heredados, por ejemplo, cambiando el color a verde.


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



[Ejemplo de atributo de tipo](/previous-versions/bb264099(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 