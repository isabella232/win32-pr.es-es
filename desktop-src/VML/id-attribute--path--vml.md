---
title: Atributo ID (Path)(VML)
description: Atributo ID (Path)(VML)
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29fe87845616b0e93e47458cd5c96f25733edd3aea7b09af6088b057d8ce0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118845923"
---
# <a name="id-attribute-pathvml"></a>Atributo ID (Path)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Nombre que proporciona un identificador único para una ruta de acceso. Lectura/escritura **Cadena**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *element* id=" *expression* ">

**Sintaxis de script**

*element* .id="*expression*"

*expresión* = *elemento*.id

**Comentarios:**

Use **id.** para hacer referencia a una ruta de acceso específica. Una vez que haya creado una ruta de acceso y le haya dado un identificador, puede usar el nombre del identificador cuando desee manipular la ruta de acceso.

*Atributo estándar de VML*

**Ejemplo**

La forma tiene un identificador de ruta de acceso denominado "myPath".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 