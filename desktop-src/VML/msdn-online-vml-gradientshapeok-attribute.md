---
title: Atributo GradientShapeOK de VML
description: Atributo GradientShapeOK de VML
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1b7c215fbe0b98c11f7e4d33301e81798bd37f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421318"
---
# <a name="vml-gradientshapeok-attribute"></a>Atributo GradientShapeOK de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si una ruta de acceso de degradado se compone de rutas de acceso concéntrica repetidas. Lectura/escritura **VgTriState**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *Element* gradientshapeok = " *expresión* " >

**Sintaxis de script**

*Element* . gradientshapeok = "*expresión*"

*expresión* = de *elemento*. gradientshapeok

**Comentarios:**

Si **es true**, la ruta de acceso se rellenará con un relleno de degradado concéntrico utilizando la ruta de acceso como forma repetida del degradado. El valor predeterminado es **false**.

*Atributo estándar de VML*

**Ejemplo**

La ruta de acceso se rellenará con un relleno de degradado concéntrico compuesto por rectángulos repetidos.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 