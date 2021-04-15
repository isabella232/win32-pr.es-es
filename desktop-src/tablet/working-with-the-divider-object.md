---
description: El objeto divisor proporciona acceso a las características de análisis del diseño de Tablet PC.
ms.assetid: 9fa299fe-3713-4fa8-95c6-be15f144103a
title: Trabajar con el objeto divisor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd158f85d368d764bce17e8b481ebe625a4d6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696325"
---
# <a name="working-with-the-divider-object"></a>Trabajar con el objeto divisor

El objeto [divisor](/previous-versions/ms583616(v=vs.100)) proporciona acceso a las características de análisis del diseño de Tablet PC.

En código administrado, se puede crear una instancia del objeto [divisor](/previous-versions/ms583616(v=vs.100)) llamando a uno de los constructores de [división](/previous-versions/ms839465(v=msdn.10)) . En automatización, esto se denomina el objeto [**InkDivider**](inkdivider-class.md) y se puede crear una instancia de él llamando al método [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

Puede obtener una instantánea del resultado del análisis actual llamando al método de [división](/previous-versions/ms839461(v=msdn.10)) del objeto de [divisor](/previous-versions/ms583616(v=vs.100)) . El resultado del análisis se devuelve en un objeto [DivisionResult](/previous-versions/ms839371(v=msdn.10)) . Cada vez que se llama al método de división, el objeto divisor crea un objeto DivisionResult. Para obtener más información sobre el objeto DivisionResult, vea [trabajar con el objeto DivisionResult](working-with-the-divisionresult-object.md).

La colección [Strokes](/previous-versions/ms552701(v=vs.100)) que analiza el objeto [divisor](/previous-versions/ms583616(v=vs.100)) está contenida en la propiedad [Strokes](/previous-versions/ms839422(v=msdn.10)) del objeto divisor. El objeto divisor analiza dinámicamente la colección de trazos a medida que se agrega o se elimina de la colección. Para obtener más información sobre la propiedad Strokes del objeto divisor, vea [trabajar con una colección Strokes](working-with-a-strokes-collection.md).

El objeto [divisor](/previous-versions/ms583616(v=vs.100)) utiliza un contexto de reconocedor para mejorar su análisis de segmentos de reconocimiento y para generar texto de reconocimiento para los elementos de escritura a mano. Puede establecer el contexto del reconocedor mediante la propiedad [RecognizerContext](/previous-versions/ms839415(v=msdn.10)) del objeto divisor. No se puede cambiar la propiedad RecognizerContext una vez que se han asignado trazos al objeto divisor. Para obtener más información sobre la propiedad RecognizerContext del objeto divisor, vea [trabajar con un contexto de reconocedor](working-with-a-recognizer-context.md).

> [!Caution]  
> En código administrado, debe llamar al método [Dispose](/previous-versions/ms839450(v=msdn.10)) en este objeto antes de que salga del ámbito. Este objeto mantiene recursos no administrados. Confiar en la finalización de este objeto puede producir pérdidas de memoria y excepciones dentro de la aplicación.

 

 

 
