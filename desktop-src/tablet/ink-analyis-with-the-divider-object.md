---
description: El objeto Divider proporciona características de análisis de diseño que clasifican y agrupan trazos en diferentes elementos estructurales.
ms.assetid: 9e4ed24f-4451-431c-9f0f-2f1c4f5e5084
title: Análisis de entrada de lápiz con el objeto divisor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d036428bbe32c42e6419c2218e6196a0b89a892137e55d141d5553d360c0a652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939565"
---
# <a name="ink-analysis-with-the-divider-object"></a>Análisis de entrada de lápiz con el objeto divisor

El [objeto Divider proporciona](/previous-versions/ms583616(v=vs.100)) características de análisis de diseño que clasifican y agrupan trazos en diferentes elementos estructurales.

## <a name="divider-object"></a>Objeto divisor

El [objeto Divisor](/previous-versions/ms583616(v=vs.100)) analiza los trazos a medida que los agrega o quita. Puede recuperar la clasificación y agrupación actuales de los trazos analizados en un [objeto DivisionResult](/previous-versions/ms583620(v=vs.100)) llamando al método [Divide](/previous-versions/ms568936(v=vs.100)) del objeto Divider.

Los trazos que [analiza el objeto Divisor](/previous-versions/ms583616(v=vs.100)) se mantienen en la propiedad [Strokes](/previous-versions/ms582090(v=vs.100)) del objeto Divider. Dado que una [colección Strokes](/previous-versions/ms552701(v=vs.100)) es una referencia a los datos de entrada de lápiz y no son los propios datos reales, los cambios en el objeto [Ink](/previous-versions/ms583670(v=vs.100)) primario de la colección Strokes pueden invalidar la colección Strokes. Para obtener más información sobre los datos de entrada de lápiz, vea [Datos de entrada de lápiz](ink-data.md).

El [objeto Divider](/previous-versions/ms583616(v=vs.100)) usa un contexto de reconocedor para mejorar su análisis de segmentos de reconocimiento y generar texto de reconocimiento para elementos de escritura a mano. Si no se asigna un contexto de reconocedor a la propiedad [RecognizerContext](/previous-versions/ms582089(v=vs.100)) del objeto Divider o los reconocedores no están instalados, la característica de análisis de diseño realiza la división del segmento de reconocimiento y no hay texto asociado al objeto [DivisionResult.](/previous-versions/ms583620(v=vs.100)) Para obtener más información sobre el reconocimiento de entrada de lápiz, vea [Ink Recognition](ink-recognition.md).

## <a name="divisionresult-object"></a>Objeto DivisionResult

Cada [objeto DivisionResult](/previous-versions/ms583620(v=vs.100)) registra el análisis de diseño de los trazos contenidos por el objeto [Divider](/previous-versions/ms583616(v=vs.100)) en el momento en que se llama al método [Divide.](/previous-versions/ms568936(v=vs.100)) El objeto DivisionResult también almacena una copia de los trazos que se usaron en el análisis.

El [objeto DivisionResult](/previous-versions/ms583620(v=vs.100)) agrupa los resultados del análisis por tipo de elemento estructural. El [**método ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) del objeto DivisionResult devuelve en una colección [DivisionUnits](/previous-versions/ms583625(v=vs.100)) la colección de todos los elementos estructurales de un tipo determinado. La [enumeración InkDivisionType](/previous-versions/ms552251(v=vs.100)) define los tipos de elemento que el análisis de diseño reconoce.

En la tabla siguiente se describen los tipos de elemento de la [enumeración InkDivisionType.](/previous-versions/ms552251(v=vs.100))



| Nombre                 | Descripción                                                                      |
|----------------------|----------------------------------------------------------------------------------|
| Segment<br/>   | Segmento de reconocimiento.<br/>                                                |
| Línea<br/>      | Línea de escritura a mano que contiene uno o varios segmentos de reconocimiento.<br/> |
| Paragraph<br/> | Bloque de trazos que contiene una o varias líneas de escritura a mano.<br/>    |
| Dibujo<br/>   | Entrada manuscrita que no es texto.<br/>                                                 |



 

En la imagen siguiente se muestra un ejemplo de los distintos tipos de elementos que reconoce el objeto [DivisionResult.](/previous-versions/ms583620(v=vs.100))

![ilustración de los distintos tipos de elementos que el objeto divisionresult reconoce](images/5f2ab955-1f74-4b71-b3ba-8d1ca23e0578.gif)

## <a name="divisionunits-collection-and-divisionunit-objects"></a>Objetos DivisionUnits Collection y DivisionUnit

Cada [colección DivisionUnits](/previous-versions/ms583625(v=vs.100)) es una copia del resultado del análisis de diseño para un único tipo de elemento estructural. El [objeto DivisionUnit](/previous-versions/ms583624(v=vs.100)) representa un elemento individual de la colección DivisionUnits. Cada elemento estructural tiene una referencia a los trazos que lo hacen. Si hay reconocedores instalados, los elementos de escritura a mano tienen texto de reconocimiento disponible. Los elementos de segmento de línea y reconocimiento también incluyen una matriz de rotación que puede girar los trazos de un elemento de vertical a horizontal.

En [el tema Ink Divider Sample (Ejemplo](ink-divider-sample.md) de divisor de lápiz) se muestra cómo usar un objeto [Divider](/previous-versions/ms583616(v=vs.100)) con objetos [Ink](/previous-versions/ms583670(v=vs.100)) para realizar análisis de diseño de lápiz.

Para obtener más información sobre el uso del análisis de entrada de lápiz, vea [The Divider Object](the-divider-object.md).

 

