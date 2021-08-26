---
title: Atributo ID (TextBox)(VML)
description: Atributo ID (TextBox)(VML)
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a3a7e88c847cf63a1362d43cb6acaf21a548b141b71ffd2724c779f8eebac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099295"
---
# <a name="id-attribute-textboxvml"></a>Atributo ID (TextBox)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Nombre que proporciona un identificador único para un cuadro de texto. Lectura/escritura **Cadena**.

**Se aplica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxis de etiquetas**

<v: *element* id=" *expression* ">

**Sintaxis de script**

*element* .id="*expression*"

*expresión* = *elemento*.id

**Comentarios:**

Use **id.** para hacer referencia a un cuadro de texto específico. Una vez que haya creado un cuadro de texto y le haya dado un identificador, puede usar el nombre del identificador cuando desee manipular el cuadro de texto.

*Atributo estándar de VML*

**Ejemplo**

La forma tiene un identificador de cuadro de texto denominado "mytextbox".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 