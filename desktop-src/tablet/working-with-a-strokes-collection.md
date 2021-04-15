---
description: La colección Strokes que analiza el objeto divisor se mantiene en la propiedad Strokes del objeto divisor.
ms.assetid: c2def964-6f2d-4b79-bfbf-a6719baf3c13
title: Trabajar con una colección de trazos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdeb03ce8168cec489dfed954a091f50f8d846d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696326"
---
# <a name="working-with-a-strokes-collection"></a>Trabajar con una colección de trazos

La colección [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que analiza el objeto [**divisor**](inkdivider-class.md) se mantiene en la propiedad [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) del objeto **divisor** . Dado que una colección de **trazos** es una referencia a los datos de tinta y no es el propio dato real, los cambios en el objeto de [**entrada de lápiz**](inkdisp-class.md) primario de la colección de **trazos** pueden invalidar la colección de **trazos** . Para obtener más información sobre los datos de tinta, vea [Ink Data](ink-data.md). Para obtener más información sobre la recopilación de entradas manuscritas, vea [recopilación de entradas manuscritas](ink-collection.md).

Para mantener la propiedad [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) del objeto [**divisor**](inkdivider-class.md) sincronizada con un objeto [**Ink**](inkdisp-class.md) , utilice los eventos [**InkAdded**](inkdisp-inkadded.md) y [**InkDeleted**](inkdisp-inkdeleted.md) del objeto de **entrada de lápiz** para realizar escuchas de trazos que deben agregarse o quitarse del objeto **divisor** . En este artículo se describen los casos en los que los trazos se agregan, se eliminan, se recortan o se dividen en el objeto de **entrada manuscrita** . Mover, escalar u otras transformaciones en trazos en el objeto de **entrada manuscrita** no generan eventos **InkAdded** ni **InkDeleted** . Para reflejar este tipo de transformación en la propiedad **Strokes** del objeto **divisor** , realice la misma transformación en los trazos del objeto **divisor** .

La propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del objeto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) contiene una copia de los trazos en el objeto [**divisor**](inkdivider-class.md) en el momento en que se creó el objeto **DivisionResult** . Puede comparar las propiedades de **trazos** de dos objetos **DivisionResult** para determinar si los trazos han cambiado entre las dos veces que se llamó al método de [**división**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) .

La propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) del objeto [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) contiene el subconjunto de los trazos del objeto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) que corresponden a este elemento. Puede pasar estos trazos a un [**RecognizerContext**](inkrecognizercontext-class.md) independiente para obtener un resultado de reconocimiento para el elemento. Dado que los elementos de escritura a mano existen en diferentes niveles de detalle, las colecciones de [**trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) para elementos diferentes pueden superponerse. Por ejemplo, la colección **Strokes** para un elemento de segmento de reconocimiento será un subconjunto de la colección **Strokes** del elemento line del que forma parte el segmento de reconocimiento.

 

 
