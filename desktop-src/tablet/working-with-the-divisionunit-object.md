---
description: El objeto DivisionUnit representa un único elemento estructural de un objeto DivisionResult. Un objeto DivisionUnit puede representar un dibujo, un único segmento de reconocimiento de escritura a mano, una línea de escritura a mano o un bloque de escritura a mano.
ms.assetid: 13f6121c-2b83-4788-9d06-460dc03094bf
title: Trabajar con el objeto DivisionUnit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c2ce09bf2b67f5724bba523219d0555063c3f7215810d3b11c48596f979fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966514"
---
# <a name="working-with-the-divisionunit-object"></a>Trabajar con el objeto DivisionUnit

El **objeto DivisionUnit** representa un único elemento estructural de un **objeto DivisionResult.** Un **objeto DivisionUnit** puede representar un dibujo, un segmento de reconocimiento único de escritura a mano, una línea de escritura a mano o un bloque de escritura a mano.

La [**enumeración InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) define los tipos de elementos estructurales que el análisis de diseño reconoce. En Automation, el **objeto DivisionUnit** se denomina [**IInkDivisionUnit.**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit)

La [**propiedad DivisionType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_divisiontype) del **objeto DivisionUnit** devuelve el tipo de elemento estructural que es **el objeto DivisionUnit.** La [**propiedad RecognitionString**](/previous-versions/windows/desktop/legacy/ms703283(v=vs.85)) del objeto **DivisionUnit** devuelve el texto de reconocimiento para los elementos de escritura a mano o **NULL para** los elementos de dibujo.

La [**propiedad Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) del **objeto DivisionUnit** contiene el subconjunto de los trazos del **objeto DivisionResult** que corresponden a este elemento. Dado que existen elementos de escritura a mano para distintos niveles de detalle, las **colecciones De trazos** para distintos elementos pueden superponerse. En concreto, un segmento de reconocimiento comparte trazos con la línea y el bloque del que forma parte, y una línea comparte trazos con el bloque del que forma parte.

La [**propiedad RotationTransform**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_rotationtransform) del **objeto DivisionUnit** devuelve una matriz para girar los trazos del elemento a horizontal. Para los elementos de párrafo y dibujo, **la propiedad RotationTransform** devuelve la matriz de identidad. Un reconocedor de texto funciona mucho mejor en la escritura a mano alineada horizontalmente que en la escritura a mano que no lo es. En Automation, esto se denomina **propiedad RotationTransform** y devuelve un [**objeto InkTransform**](inktransform-class.md) que contiene la matriz de transformación. La **propiedad RotationTransform** devuelve **NULL para** los elementos de párrafo y dibujo.

Para obtener más información sobre **el objeto DivisionResult,** vea [Trabajar con el objeto DivisionResult](working-with-the-divisionresult-object.md).

 

 
