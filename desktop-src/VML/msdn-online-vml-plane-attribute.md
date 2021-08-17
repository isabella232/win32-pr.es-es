---
title: Atributo de plano VML
description: Atributo de plano VML
ms.assetid: e1de630b-8e25-4052-b316-251046f73e98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85312c8c2987105859b9f773fa102723c64c30c688dedd34fb9578bd370452e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334215"
---
# <a name="vml-plane-attribute"></a>Atributo de plano VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica el plano que está en ángulos derecho para la extrusión. Lectura/escritura **Cadena**.

**Se aplica a**

[Extrusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *element* plane=" *expression* ">

**Sintaxis de script**

*element* .plane="*expression*"

*expresión* = *elemento*.plane

**Comentarios:**

Estos valores incluyen:



| Value | Descripción                                            |
|-------|--------------------------------------------------------|
| xy    | La extrusión está en ángulos derecho hacia el plano xy. Valor predeterminado |
| Zx    | La extrusión está en ángulos derecho hacia el plano zx.         |
| Yz    | La extrusión se encuentra en ángulos a la derecha del plano yz.         |



 

*Microsoft Office Atributo Extensions*

 

 