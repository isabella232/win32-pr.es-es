---
title: Atributo de metal de VML
description: Atributo de metal de VML
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d318724f0a8f3c5fbce1ee9045ed5d6e0d49686
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420753"
---
# <a name="vml-metal-attribute"></a>Atributo de metal de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si la superficie de la forma extruida se parecerá a metal. Lectura/escritura **VgTriState**.

**Se aplica a**

[Trusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *elemento* metal = " *expresión* " >

**Sintaxis de script**

*Element* . metal = "*expresión*"

*expresión* = de *elemento*. metal

**Comentarios:**

Si se establece en **true**, este atributo hace que la luz reflejada especular sea el color del material en lugar del color de la fuente de luz, lo que hace que el objeto parezca más metálico. Para aproximarse más a un material metálico, es necesario que la especulación sea relativamente alta (aproximadamente 1,2) y que la difusión sea relativamente baja (aproximadamente 0,6). El valor predeterminado es **False**.

*Microsoft Office atributo Extensions*

 

 