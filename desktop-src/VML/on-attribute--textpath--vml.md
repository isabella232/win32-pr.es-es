---
title: Atributo On (TextPath)(VML)
description: Atributo On (TextPath)(VML)
ms.assetid: b4a88473-6d5f-42b3-afd6-86f602c83724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7b1361bc0600ecca64e252ac25254d26b340cfd34a481de9424017de3381ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345818"
---
# <a name="on-attribute-textpathvml"></a>Atributo On (TextPath)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define si se muestra el texto. Lectura/escritura **DvTriState**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* on=" *expression* ">

**Sintaxis de script**

*Element* .on="*expression*"

*expresión* = *elemento*.on

**Comentarios:**

El valor predeterminado es **false**. Este valor debe establecerse en **True para** mostrar texto en una ruta de texto.

*Atributo estándar de VML*

**Ejemplo**

Se mostrará el texto de la ruta de acceso de texto.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 