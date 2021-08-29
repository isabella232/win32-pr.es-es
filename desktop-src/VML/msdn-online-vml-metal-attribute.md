---
title: Atributo DE METAL DE VML
description: Atributo DE METAL DE VML
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58b137dd2f874333bb618d1b892632abb5a679d5b533b924a73416ff38732e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867195"
---
# <a name="vml-metal-attribute"></a>Atributo DE METAL DE VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si la superficie de la forma extruida se parecerá al metal. Lectura/escritura **DvTriState**.

**Se aplica a**

[Extrusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *element* metal=" *expression* ">

**Sintaxis de script**

*element* .metal="*expression*"

*expresión* = *elemento*.metal

**Comentarios:**

Si se establece en **True**, este atributo hace que la luz reflejada especularmente sea el color del material en lugar del color de la fuente de luz, lo que hace que el objeto parezca más resistente. Para aproximarse aún más a un material resistente, es necesario que la especularidad sea relativamente alta (aproximadamente 1,2) y que la diferencia sea relativamente baja (aproximadamente 0,6). El valor predeterminado es **False**.

*Microsoft Office Atributo Extensions*

 

 