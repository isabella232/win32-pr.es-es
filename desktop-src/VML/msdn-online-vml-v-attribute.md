---
title: Atributo V de VML
description: Atributo V de VML
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbf2f8654d32714d20e9b0c5a36fb939173698749569692120c04b89e84b6e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768335"
---
# <a name="vml-v-attribute"></a>Atributo V de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define los comandos que son una ruta de acceso. Lectura/escritura **Cadena**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *elemento* v=" *expresión* ">

**Sintaxis de script**

*element* .v="*expression*"

*expresión* = *elemento*.v

**Comentarios:**

Invalida el atributo **Path** de una forma. Las coordenadas pueden ser números fijos, números relativos o referencias a fórmulas (mediante el formato de " " , donde n es un número de fórmula; por ejemplo, " " hace referencia a la segunda fórmula de la matriz de @n @2 fórmulas).

*Atributo estándar de VML*

**Ejemplo**

Se crea un rectángulo mediante el **atributo V.** Tenga en cuenta que se usa una letra minúscula L (comando **lineto)** después del primer conjunto de coordenadas delimitadas por comas.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 