---
title: Tipo de datos IVgAdjustments de VML
description: Tipo de datos IVgAdjustments de VML
ms.assetid: d605632b-3ee2-44fd-8122-f38b1f91e965
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed6512e36e9621d010e8875eec3190fa81524b4947a30f14364199341d18c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599683"
---
# <a name="vml-ivgadjustments-data-type"></a>Tipo de datos IVgAdjustments de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Colección de ajustes en una forma que se puede usar en fórmulas. Los ajustes se pueden usar como marcadores de posición temporales o, por cualquier motivo, usaría variables. Solo hay 8 ajustes en la colección.



| Atributos | Descripción                                                                                                                                                                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Length     | **Entero**. Número de ajustes. No puede ser mayor que 8.                                                                                                                                                                                                                                                                          |
| Elemento       | **Long**. Matriz de ajustes indizados de 0 a 7. Tenga en cuenta que los ajustes se pueden especificar de forma sparcely; Es decir, es posible que los valores intermedios de la matriz no siempre se llenen. Por ejemplo, los elementos 1, 3 y 5 podrían tener valores para una longitud de 3, con item(0), item(2) y item(4) especificados. Para ver si existe un elemento, use el atributo Exists. |
| Exists     | **IVgTriState**. Determina si existe un ajuste especificado. Tenga en cuenta que se debe usar un índice; es decir, exists(item) debe usarse para recuperar la existencia de un elemento.                                                                                                                                                           |
| Value      | **Cadena**. Representación de texto de valores numéricos, con comas entre cada número.                                                                                                                                                                                                                                                    |



 

 

 