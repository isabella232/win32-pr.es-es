---
description: El objeto DivisionUnit representa un único elemento estructural de un objeto DivisionResult. Un objeto DivisionUnit puede representar un dibujo, un solo segmento de reconocimiento de escritura a mano, una línea de escritura a mano o un bloque de escritura a mano.
ms.assetid: 13f6121c-2b83-4788-9d06-460dc03094bf
title: Trabajar con el objeto DivisionUnit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade8b617ae8e64c2641ef53a628a44e72e4fc35f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907907"
---
# <a name="working-with-the-divisionunit-object"></a>Trabajar con el objeto DivisionUnit

El objeto **DivisionUnit** representa un único elemento estructural de un objeto **DivisionResult** . Un objeto **DivisionUnit** puede representar un dibujo, un solo segmento de reconocimiento de escritura a mano, una línea de escritura a mano o un bloque de escritura a mano.

La enumeración [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) define los tipos de elemento estructurales que reconoce el análisis de diseño. En Automation, el objeto **DivisionUnit** se llama [**IInkDivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit).

La propiedad [**DivisionType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_divisiontype) del objeto **DivisionUnit** devuelve el tipo de elemento estructural que es el objeto **DivisionUnit** . La propiedad [**RecognitionString**](/previous-versions/windows/desktop/legacy/ms703283(v=vs.85)) del objeto **DivisionUnit** devuelve el texto de reconocimiento para los elementos de escritura a mano o **null** para los elementos de dibujo.

La propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) del objeto **DivisionUnit** contiene el subconjunto de los trazos del objeto **DivisionResult** que corresponden a este elemento. Dado que los elementos de escritura a mano existen para diferentes niveles de detalle, las colecciones de **trazos** para elementos diferentes pueden superponerse. En concreto, un segmento de reconocimiento comparte trazos con la línea y el bloque forma parte de, y una línea comparte trazos con el bloque del que forma parte.

La propiedad [**RotationTransform**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_rotationtransform) del objeto **DivisionUnit** devuelve una matriz para girar los trazos del elemento a horizontal. En el caso de los elementos de párrafo y de dibujo, la propiedad **RotationTransform** devuelve la matriz de identidad. Un reconocedor de texto funciona mucho mejor en la escritura a mano que está alineada horizontalmente con la escritura a mano que no es. En automatización, esto se denomina la propiedad **RotationTransform** y devuelve un objeto [**InkTransform**](inktransform-class.md) que contiene la matriz de transformación. La propiedad **RotationTransform** devuelve **null** para los elementos de párrafo y de dibujo.

Para obtener más información sobre el objeto **DivisionResult** , vea [trabajar con el objeto DivisionResult](working-with-the-divisionresult-object.md).

 

 
