---
title: Atributo AutoRotationCenter de VML
description: Atributo AutoRotationCenter de VML
ms.assetid: beb6771f-42f4-458a-b525-4eb67bc1eff0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1624ab3f2c37e043a6d478ca8e422a714a83d157
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792388"
---
# <a name="vml-autorotationcenter-attribute"></a>Atributo AutoRotationCenter de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si el centro de rotación será el centro geométrico de la extrusión. Lectura/escritura **VgTriState**.

**Se aplica a**

[Trusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *elemento* autorotationcenter = " *expresión* " >

**Sintaxis de script**

*Element* . autorotationcenter = "*expresión*"

*expresión* = de *elemento*. autorotationcenter

**Comentarios:**

El centro geométrico de una forma extruida es 0, 0,0. Si el valor de este atributo es **false**, el centro de rotación viene determinado por el atributo [RotationCenter](msdn-online-vml-rotationcenter-attribute.md) . El valor predeterminado es **False**.

*Microsoft Office atributo Extensions*

 

 