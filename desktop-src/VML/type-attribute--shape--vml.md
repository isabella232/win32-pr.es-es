---
title: Atributo type (Shape)(VML)
description: Atributo type (Shape)(VML)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b20f663f8a403acca03ff8ab516a86dc91f7dd8d478eadedaa6be8b919ad48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513155"
---
# <a name="type-attribute-shapevml"></a>Atributo type (Shape)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define una referencia al identificador de un [elemento ShapeType.](msdn-online-vml-shapetype-element.md) Lectura/escritura **Cadena**.

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

Si el **atributo Type** hace referencia al identificador de un elemento **ShapeType,** los rellenos, las rutas de acceso y los trazos de **ShapeType** se usan como plantillas para crear la forma. Los valores derivados de **ShapeType** se pueden reemplazar por valores de forma individuales.

Si se usa en etiquetas, el valor de cadena debe comenzar con un símbolo de signo de número ( \# ).

**Atributo estándar de VML**

**Ejemplo**

Se crea una forma **ShapeType** con "mytype" como identificador.


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



A continuación, si crea una forma con los valores **ShapeType,** la forma tendrá los atributos de "mytype" **ShapeType**; es decir, "shape01" tendrá un relleno rojo con un trazo azul.


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



[Ejemplo de atributo de tipo](/previous-versions/bb264099(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 