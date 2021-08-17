---
title: Atributo de tipo (extrusión)(VML)
description: Atributo de tipo (extrusión)(VML)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a14c3b69aa4156cbd94bb8598caa80ccd92721574daafe074486eb293059cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057593"
---
# <a name="type-attribute-extrusionvml"></a>Atributo de tipo (extrusión)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la forma en que se extruye la forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Extrusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *element* type=" *expression* ">

**Sintaxis de script**

*element* .type="*expression*"

*expresión* = *element*.type

**Comentarios:**

Estos valores incluyen:



| Value       | Descripción                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parallel    | La extrusión se representa para que el centro de proyección esté infinitamente lejos; es decir, las líneas de extrusión no convergen (a diferencia de las proyecciones de perspectiva). Predeterminada. |
| perspectiva | La extrusión se representa en un centro de proyección, que es el mismo que el punto de desvaneciendo para los objetos sin procesar.                                                       |



 

**Microsoft Office Atributo Extensions**

 

 