---
title: Atributo ColorMode de VML
description: Atributo ColorMode de VML
ms.assetid: 92c885ca-7912-42ff-8f07-e6e779e0ef05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7126a3f5a95910eb85007fe9a80d500c5233e5e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420930"
---
# <a name="vml-colormode-attribute"></a>Atributo ColorMode de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina el modo de color de extrusión. Lectura/escritura **VgTriState**.

**Se aplica a**

[Trusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *elemento* ColorMode = " *expresión* " >

**Sintaxis de script**

*Element* . ColorMode = "*expresión*"

*expresión* = de *elemento*. ColorMode

**Comentarios:**

Estos valores incluyen:



| Value  | Descripción                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------|
| auto   | Especifica que el color de la extrusión es el mismo que el color de relleno de la forma. Predeterminada.                |
| custom | Especifica que la extrusión será el color del atributo de [color](color-attribute--extrusion--vml.md) . |



 

*Microsoft Office atributo Extensions*

 

 