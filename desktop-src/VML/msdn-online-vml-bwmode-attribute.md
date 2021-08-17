---
title: Atributo BWMode de VML
description: Atributo BWMode de VML
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5640680af40f4649f7ab34b2ec8cfd4e5cf94ee4c7c6ce3c3f2185e68bdac360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754970"
---
# <a name="vml-bwmode-attribute"></a>Atributo BWMode de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina cómo se representará una forma para los dispositivos de salida en blanco y negro. Lectura/escritura [DvBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* o:bwmode=" *expression* ">

**Comentarios:**

Cuando una forma se imprime en una impresora en blanco y negro o se muestra en una vista en blanco y negro en una aplicación, son posibles varias opciones. Para obtener más información sobre los valores de este atributo, vea el tema [DeCkBlackWhiteMode.](msdn-online-vml-vgblackwhitemode.md) El valor predeterminado es **auto.**

Si se especifica **auto,** [BWNormal](msdn-online-vml-bwnormal-attribute.md) se usa para determinar el comportamiento de la salida normal en blanco y negro, y [BWPure](msdn-online-vml-bwpure-attribute.md) se usa para determinar el comportamiento de la salida pura en blanco y negro.

*Microsoft Office Atributo Extensions*

**Ejemplo**

El modo en blanco y negro de la forma es **automático.**


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 