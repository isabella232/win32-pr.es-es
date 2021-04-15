---
title: Atributo de impresión VML
description: Atributo de impresión VML
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676393"
---
# <a name="vml-print-attribute"></a>Atributo de impresión VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si la forma se va a imprimir. Lectura/escritura [VgTriState](msdn-online-vml-vgtristate.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* Print = " *expresión* " >

**Sintaxis de script**

*Element* . Print = "*expresión*"

*expresión* = de *elemento*. Print

**Comentarios:**

Se proporciona como una manera de especificar si se van a imprimir las formas. Tenga en cuenta que todavía se puede mostrar una forma en la pantalla, aunque no se imprima como resultado de que este atributo sea **falso**. El valor predeterminado es **True**.

Este atributo lo usa Microsoft Office pero Microsoft Internet Explorer no lo usa.

*Microsoft Office atributo Extensions*

 

 