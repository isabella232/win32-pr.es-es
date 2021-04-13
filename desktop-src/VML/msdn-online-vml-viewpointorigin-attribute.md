---
title: Atributo ViewpointOrigin de VML
description: Atributo ViewpointOrigin de VML
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad256f0f5d38c6fbbfb5722e803985506efca217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487855"
---
# <a name="vml-viewpointorigin-attribute"></a>Atributo ViewpointOrigin de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el origen del punto de vista en el cuadro de límite de la forma. Lectura/escritura **VgVector2D**.

**Se aplica a**

[Trusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *elemento* viewpointorigin = " *expresión* " >

**Sintaxis de script**

*Element* . viewpointorigin = "*expresión*"

*expresión* = de *elemento*. viewpointorigin

**Comentarios:**

Define el Viewpoint en términos de los valores x e y de la forma original. Los valores x e y van de 0,5 a-0,5 (50% a-50% del origen de coordenadas de la forma). El valor predeterminado es 0, 0.

*Microsoft Office atributo Extensions*

 

 