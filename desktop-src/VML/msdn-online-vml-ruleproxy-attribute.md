---
title: Atributo RuleProxy de VML
description: Atributo RuleProxy de VML
ms.assetid: 040e80f8-65b6-491d-812d-421800801374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fe97afee190d87b5e6f8b74d942a72d3bf11914373931e32cbb9459915b7d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099135"
---
# <a name="vml-ruleproxy-attribute"></a>Atributo RuleProxy de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si se usará un proxy para el motor de reglas. Lectura/escritura **DvTriState**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* ruleproxy=" *expression* ">

**Comentarios:**

El valor predeterminado es **False**. Si **es True,** se usa un proxy.

*Microsoft Office Atributo Extensions*

**Ejemplo**

Un proxy se usa para procesar la forma.


```HTML
   <v:rect id=myrect fillcolor="red" ruleproxy="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 