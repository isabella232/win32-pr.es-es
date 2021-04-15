---
title: Atributo Render de VML
description: Atributo Render de VML
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70872e823a2d43d6a605fbf07a817473b19a125a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676445"
---
# <a name="vml-render-attribute"></a>Atributo Render de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el modo de representación de la extrusión. Lectura/escritura **Cadena**.

**Se aplica a**

[Trusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *elemento* Render = " *expresión* " >

**Sintaxis de script**

*Element* . Render = "*expresión*"

*expresión* = de *elemento*. Render

**Comentarios:**

Estos valores incluyen:



| Value        | Descripción                                                   |
|--------------|---------------------------------------------------------------|
| barra        | La representación muestra una forma sólida. Predeterminada.                    |
| estructura    | La representación muestra una forma de trama.                         |
| boundingcube | La representación muestra el cubo de límite que contiene la forma. |



 

*Microsoft Office atributo Extensions*

 

 