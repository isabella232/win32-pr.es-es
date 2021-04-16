---
description: El objeto divisor proporciona características de análisis de diseño que clasifican y agrupan los trazos en diferentes elementos estructurales.
ms.assetid: 9e4ed24f-4451-431c-9f0f-2f1c4f5e5084
title: Análisis de tinta con el objeto divisor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f1df175f8746e56cf6ebd1b222b3901fbef36e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540446"
---
# <a name="ink-analysis-with-the-divider-object"></a>Análisis de tinta con el objeto divisor

El objeto [divisor](/previous-versions/ms583616(v=vs.100)) proporciona características de análisis de diseño que clasifican y agrupan los trazos en diferentes elementos estructurales.

## <a name="divider-object"></a>Objeto divisor

El objeto [divisor](/previous-versions/ms583616(v=vs.100)) analiza los trazos a medida que se agregan o se quitan. Puede recuperar la clasificación y agrupación actuales de los trazos analizados en un objeto [DivisionResult](/previous-versions/ms583620(v=vs.100)) llamando al método de [división](/previous-versions/ms568936(v=vs.100)) del objeto de divisor.

Los trazos que analiza el objeto [divisor](/previous-versions/ms583616(v=vs.100)) se mantienen en la propiedad [Strokes](/previous-versions/ms582090(v=vs.100)) del objeto divisor. Dado que una colección de [trazos](/previous-versions/ms552701(v=vs.100)) es una referencia a los datos de tinta y no es el propio dato real, los cambios en el objeto de [entrada de lápiz](/previous-versions/ms583670(v=vs.100)) primario de la colección de trazos pueden invalidar la colección de trazos. Para obtener más información sobre los datos de tinta, vea [Ink Data](ink-data.md).

El objeto [divisor](/previous-versions/ms583616(v=vs.100)) utiliza un contexto de reconocedor para mejorar su análisis de segmentos de reconocimiento y para generar texto de reconocimiento para los elementos de escritura a mano. Si no se asigna un contexto de reconocedor a la propiedad [RecognizerContext](/previous-versions/ms582089(v=vs.100)) del objeto divisor o no se instalan los reconocedores, la característica de análisis de diseño realiza la división del segmento de reconocimiento y no hay texto asociado al objeto [DivisionResult](/previous-versions/ms583620(v=vs.100)) . Para obtener más información sobre el reconocimiento de tinta, vea [reconocimiento de tinta](ink-recognition.md).

## <a name="divisionresult-object"></a>Objeto DivisionResult

Cada objeto [DivisionResult](/previous-versions/ms583620(v=vs.100)) registra el análisis del diseño de los trazos que contiene el objeto [divisor](/previous-versions/ms583616(v=vs.100)) en el momento en que se llama al método de [división](/previous-versions/ms568936(v=vs.100)) . El objeto DivisionResult también almacena una copia de los trazos que se usaron en el análisis.

El objeto [DivisionResult](/previous-versions/ms583620(v=vs.100)) agrupa los resultados del análisis por tipo de elemento estructural. El método [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) del objeto DivisionResult devuelve en una colección [DivisionUnits](/previous-versions/ms583625(v=vs.100)) la colección de todos los elementos estructurales de un tipo determinado. La enumeración [InkDivisionType](/previous-versions/ms552251(v=vs.100)) define los tipos de elementos que reconoce el análisis de diseño.

En la tabla siguiente se describen los tipos de elemento de la enumeración [InkDivisionType](/previous-versions/ms552251(v=vs.100)) .



| Nombre                 | Descripción                                                                      |
|----------------------|----------------------------------------------------------------------------------|
| Segment<br/>   | Un segmento de reconocimiento.<br/>                                                |
| Línea<br/>      | Línea de escritura a mano que contiene uno o más segmentos de reconocimiento.<br/> |
| Paragraph<br/> | Bloque de trazos que contiene una o más líneas de escritura a mano.<br/>    |
| Dibujo<br/>   | Tinta que no es texto.<br/>                                                 |



 

La imagen siguiente muestra un ejemplo de los distintos tipos de elementos que reconoce el objeto [DivisionResult](/previous-versions/ms583620(v=vs.100)) .

![Ilustración de los distintos tipos de elementos que reconoce el objeto divisionresult](images/5f2ab955-1f74-4b71-b3ba-8d1ca23e0578.gif)

## <a name="divisionunits-collection-and-divisionunit-objects"></a>Colección DivisionUnits y objetos DivisionUnit

Cada colección [DivisionUnits](/previous-versions/ms583625(v=vs.100)) es una copia del resultado del análisis de diseño para un único tipo de elemento estructural. El objeto [DivisionUnit](/previous-versions/ms583624(v=vs.100)) representa un elemento individual de la colección DivisionUnits. Cada elemento estructural tiene una referencia a los trazos que componen el elemento. Si los reconocedores están instalados, los elementos de escritura a mano tienen texto de reconocimiento disponible. Los elementos de segmento de línea y reconocimiento también incluyen una matriz de rotación que puede girar los trazos de un elemento de vertical a horizontal.

El tema de [ejemplo de divisor de tinta](ink-divider-sample.md) muestra cómo utilizar un objeto [divisor](/previous-versions/ms583616(v=vs.100)) con objetos de [entrada manuscrita](/previous-versions/ms583670(v=vs.100)) para realizar análisis de diseño de la tinta.

Para obtener más información sobre el uso del análisis de tinta, vea [el objeto divisor](the-divider-object.md).

 

