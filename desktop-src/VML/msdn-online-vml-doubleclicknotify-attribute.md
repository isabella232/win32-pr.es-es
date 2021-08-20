---
title: Atributo DoubleClickNotify de VML
description: Atributo DoubleClickNotify de VML
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9945f4391890f33d3569d1c1aed39a8ec5bbe4b0be29258da1cca4b7caf895da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124835"
---
# <a name="vml-doubleclicknotify-attribute"></a>Atributo DoubleClickNotify de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Envía un mensaje de evento cuando se hace doble clic en una forma. Lectura/escritura **DvTriState**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* o:doubleclicknotify=" *expression* ">

**Comentarios:**

El valor predeterminado es **False**, lo que indica que no se desencadena el evento.

*Microsoft Office Atributo Extensions*

**Ejemplo**

La forma desencadenará un evento de doble clic cuando se haga doble clic.


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 