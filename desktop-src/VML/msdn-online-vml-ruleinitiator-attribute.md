---
title: Atributo RuleInitiator de VML
description: Atributo RuleInitiator de VML
ms.assetid: 2c9b1131-b088-4b70-b132-bdb4296433ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b015ba3742eda42fd506d955bbc8d2b9d7285999581897952dede665c9eb3361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654965"
---
# <a name="vml-ruleinitiator-attribute"></a>Atributo RuleInitiator de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si se usará un motor de reglas. Lectura/escritura **DvTriState**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *elemento* o:ruleinitiator=" *expresión* ">

**Comentarios:**

El valor predeterminado es **False**. Si el valor es **True**, se usa un motor de reglas.

*Microsoft Office Atributo Extensions*

**Ejemplo**

La forma la procesará un motor de reglas.


```HTML
   <v:rect id=myrect fillcolor="red" rulesinitiator="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 