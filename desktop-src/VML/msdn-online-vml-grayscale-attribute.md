---
title: Atributo GrayScale de VML
description: Atributo GrayScale de VML
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683371e2441ffa93f96dc8f727e4eed293954b1897267db8848aa39ffa497af8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099215"
---
# <a name="vml-grayscale-attribute"></a>Atributo GrayScale de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si una imagen se mostrará en modo de escala de grises. Lectura/escritura **DvTriState**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *element* grayscale=" *expression* ">

**Sintaxis de script**

*element* .grayscale="*expression*"

*expresión* = *elemento*.grayscale

**Comentarios:**

Si **es True,** la imagen se mostrará en escala de grises en lugar de en color. El valor predeterminado es **False**.

El valor se basa según la recomendación 709 de CCIR, que favorece más peso verde y genera resultados más satisfactorios para el color natural.

*Atributo estándar de VML*

**Ejemplo**

La imagen se mostrará en escala de grises en lugar de en color.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 