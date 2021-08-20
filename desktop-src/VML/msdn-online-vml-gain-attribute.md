---
title: Atributo de ganancia de VML
description: Atributo de ganancia de VML
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7b72f1588608f4988731111583e758b0207080eb3e02768a45b58c39071b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057833"
---
# <a name="vml-gain-attribute"></a>Atributo de ganancia de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la intensidad de todos los colores de una imagen. Lectura/escritura **NumberNumber**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *element* gain=" *expression* ">

**Sintaxis de script**

*element* .gain="*expression*"

*expresión* = *elemento*.gain

**Comentarios:**

Este atributo define lo brillante que es el color blanco, lo que afecta a todos los demás colores. Los valores oscilan entre 0 y infinito. El valor predeterminado es 1,0. Un valor de 0 no muestra ninguna imagen. Los valores mayores que 1 a claro la imagen y los valores menores que 1 hacen que la imagen parezca más gris.

Este atributo se puede usar para crear efectos interesantes.

*Atributo estándar de VML*

**Ejemplo**

La imagen se mostrará con todos los colores que tienden a gris.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 