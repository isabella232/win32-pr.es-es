---
title: Tipo de datos IVgAdjustments de VML
description: Tipo de datos IVgAdjustments de VML
ms.assetid: d605632b-3ee2-44fd-8122-f38b1f91e965
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29f85f93218db098ca247fa66b1f493e9c622a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487879"
---
# <a name="vml-ivgadjustments-data-type"></a>Tipo de datos IVgAdjustments de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Colección de ajustes de una forma que se puede usar en las fórmulas. Los ajustes se pueden usar como marcadores de posición temporales o, por cualquier motivo, se usarían variables. Solo hay 8 ajustes en la colección.



| Atributos | Descripción                                                                                                                                                                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Length     | **Entero**. Número de ajustes. No puede ser mayor que 8.                                                                                                                                                                                                                                                                          |
| Elemento       | **Largo**. Matriz de ajustes indizada de 0 a 7. Tenga en cuenta que los ajustes pueden especificarse de SPARC. es decir, es posible que no siempre se rellenen los valores de matriz intermedios. Por ejemplo, los elementos 1, 3 y 5 podrían tener valores para una longitud de 3, con el elemento (0), el elemento (2) y el elemento (4) especificado. Para ver si existe un elemento, utilice el atributo EXISTS. |
| Exists     | **IVgTriState**. Determina si existe un ajuste especificado. Tenga en cuenta que se debe usar un índice; es decir, exists (Item) se debe usar para recuperar la existencia de un elemento.                                                                                                                                                           |
| Value      | **Cadena**. Representación de texto de valores numéricos, con comas entre cada número.                                                                                                                                                                                                                                                    |



 

 

 