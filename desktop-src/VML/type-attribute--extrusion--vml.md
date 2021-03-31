---
title: Atributo de tipo (extrusión) (VML)
description: Atributo de tipo (extrusión) (VML)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14bc91f9348603bc89189debb2255f8fff39e135
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904709"
---
# <a name="type-attribute-extrusionvml"></a>Atributo de tipo (extrusión) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la manera en que se extrude la forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Trusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: tipo de *elemento* = " *expresión* " >

**Sintaxis de script**

*Element* . Type = "*expresión*"

*expresión* = de *elemento*. Type

**Comentarios:**

Estos valores incluyen:



| Value       | Descripción                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parallel    | La extrusión se representa para que el centro de proyección esté indefinidamente lejos; es decir, las líneas de extrusión no convergen (a diferencia de las proyecciones de perspectiva). Predeterminada. |
| perspectiva | La extrusión se representa en un centro de proyección, que es igual que el punto de desvanecimiento para los objetos no girados.                                                       |



 

**Microsoft Office atributo Extensions**

 

 