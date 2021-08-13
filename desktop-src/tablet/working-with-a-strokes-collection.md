---
description: La colección Strokes que analiza el objeto Divider se mantiene en la propiedad Strokes del objeto Divider.
ms.assetid: c2def964-6f2d-4b79-bfbf-a6719baf3c13
title: Trabajar con una colección de trazos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35673ef17882f246969e7c74869f47b09b604195c74bb1456c3624713a42045d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119221875"
---
# <a name="working-with-a-strokes-collection"></a>Trabajar con una colección de trazos

La [**colección Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que analiza [**el objeto Divider**](inkdivider-class.md) se mantiene en la propiedad [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) del **objeto Divider.** Dado que una **colección Strokes** es una referencia a los datos de entrada de lápiz y no son los propios datos reales, los cambios en el objeto [**Ink**](inkdisp-class.md) primario de la colección **Strokes** pueden invalidar la **colección Strokes.** Para obtener más información sobre los datos de entrada de lápiz, vea [Datos de entrada de lápiz](ink-data.md). Para obtener más información sobre la colección de entrada de lápiz, vea [Ink Collection](ink-collection.md).

Para mantener la propiedad [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) del objeto [**Divider**](inkdivider-class.md) sincronizada con un objeto [**Ink,**](inkdisp-class.md) use los eventos [**InkAdded**](inkdisp-inkadded.md) y [**InkDeleted**](inkdisp-inkdeleted.md) del objeto **Ink** para escuchar los trazos que se deben agregar o quitar del objeto **Divider.** Esto cubre los casos en los que se agregan, eliminan, recortan o dividen trazos dentro del **objeto Ink.** El movimiento, el escalado u otras transformaciones en trazos del objeto **Ink** no generan eventos **InkAdded** o **InkDeleted.** Para reflejar esta transformación en la propiedad **Strokes** del objeto **Divider,** realice la misma transformación en los trazos del **objeto Divider.**

La [**propiedad Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del [**objeto DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) contiene una copia de los trazos del objeto [**Divider**](inkdivider-class.md) en el momento en que se creó el objeto **DivisionResult.** Puede comparar las propiedades **Strokes** de dos **objetos DivisionResult** para determinar si los trazos han cambiado entre las dos veces que se llamó al método [**Divide.**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide)

La [**propiedad Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) del [**objeto DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) contiene el subconjunto de los trazos del [**objeto DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) que corresponden a este elemento. Puede pasar estos trazos a un [**RecognizerContext independiente**](inkrecognizercontext-class.md) para obtener un resultado de reconocimiento para el elemento. Puesto que los elementos de escritura a mano existen en distintos niveles de detalle, las [**colecciones de trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) para distintos elementos pueden superponerse. Por ejemplo, la colección **Strokes** de un elemento de segmento de reconocimiento será un subconjunto de la colección **Strokes** para el elemento de línea del que forma parte el segmento de reconocimiento.

 

 
