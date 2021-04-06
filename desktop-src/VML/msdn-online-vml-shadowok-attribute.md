---
title: Atributo ShadowOK de VML
description: Atributo ShadowOK de VML
ms.assetid: 88400bf5-f41c-4495-a5d0-9b35c1cae9f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e6b4ca6b98ce66208e906c45fd560324121e8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077785"
---
# <a name="vml-shadowok-attribute"></a>Atributo ShadowOK de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si se mostrará una sombra. Lectura/escritura **VgTriState**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *Element* shadowok = " *expresión* " >

**Sintaxis de script**

*Element* . shadowok = "*expresión*"

*expresión* = de *elemento*. shadowok

**Comentarios:**

Si **es false**, la ruta de acceso no puede tener una sombra. El valor predeterminado es **True**. Este atributo invalida todos los demás atributos de sombra del elemento primario o de **sombra** .

*Atributo estándar de VML*

**Ejemplo**

La forma no tendrá una sombra.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True" offset="5pt,5pt" color="blue"/>
   <v:path id= "myPath" shadowok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 