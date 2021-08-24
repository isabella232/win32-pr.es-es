---
title: Atributo PreferRelative de VML
description: Atributo PreferRelative de VML
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154297a528f18a3ac53f788ebbfe80ff59196f2872dd3dcb3789db16d5c91cb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654985"
---
# <a name="vml-preferrelative-attribute"></a>Atributo PreferRelative de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si el tamaño original de un objeto se guarda después del formatear. Lectura/escritura **DvTriState**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* o:preferrelative=" *expression* ">

**Comentarios:**

El valor predeterminado es **False**. Si **es True**, se almacenará el tamaño original del objeto y todo el cambio de tamaño se basará en un porcentaje de ese tamaño original. De lo contrario, cada cambio de tamaño restablecerá la escala al 100 %.

*Microsoft Office Atributo Extensions*

**Ejemplo**

Si se cambia el tamaño de la forma, no se almacenará el tamaño original.


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 