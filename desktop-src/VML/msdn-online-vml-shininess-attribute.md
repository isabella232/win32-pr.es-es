---
title: Atributo de brillo de VML
description: Atributo de brillo de VML
ms.assetid: 99c301ff-ed61-48ef-95bb-ceaed1a2553c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a116adeb955c0f3449b374947a3f8121bd848e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359004"
---
# <a name="vml-shininess-attribute"></a>Atributo de brillo de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la concentración de la luz reflejada en una superficie de extrusión. Lectura/escritura **VgNumber**.

**Se aplica a**

[Trusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *elemento* de brillo = " *expresión* " >

**Sintaxis de script**

*Element* . brillo = "*expresión*"

*expresión* = de *elemento*. brillo

**Comentarios:**

Los valores altos (8-10) aproximarían el brillo de un reflejo y los valores bajos (2-3) aproximarían un efecto moteado. Los valores de 4-7 son típicos. Los reflejos no reflejan otros objetos; solo se reflejan las fuentes de luz de Pinpoint. El valor predeterminado es 5.

*Microsoft Office atributo Extensions*

 

 