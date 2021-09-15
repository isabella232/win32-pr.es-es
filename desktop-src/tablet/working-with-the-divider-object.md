---
description: El objeto Divider proporciona acceso a las características de análisis de diseño de Tablet PC.
ms.assetid: 9fa299fe-3713-4fa8-95c6-be15f144103a
title: Trabajar con el objeto divisor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd158f85d368d764bce17e8b481ebe625a4d6d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247683"
---
# <a name="working-with-the-divider-object"></a>Trabajar con el objeto divisor

El [objeto Divider proporciona](/previous-versions/ms583616(v=vs.100)) acceso a las características de análisis de diseño de Tablet PC.

En el código administrado, se puede crear una instancia del objeto [Divider](/previous-versions/ms583616(v=vs.100)) llamando a uno de los [constructores](/previous-versions/ms839465(v=msdn.10)) divisores. En Automation, esto se denomina el objeto [**InkDivider**](inkdivider-class.md) y se pueden crear instancias mediante una llamada al [**método CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

Puede obtener una instantánea del resultado del análisis actual llamando al [método Divide](/previous-versions/ms839461(v=msdn.10)) del [objeto Divider.](/previous-versions/ms583616(v=vs.100)) El resultado del análisis se devuelve en un [objeto DivisionResult.](/previous-versions/ms839371(v=msdn.10)) Cada vez que se llama al método Divide, el objeto Divider crea un objeto DivisionResult. Para obtener más información sobre el objeto DivisionResult, vea [Trabajar con el objeto DivisionResult](working-with-the-divisionresult-object.md).

La [colección Strokes](/previous-versions/ms552701(v=vs.100)) que analiza el [objeto Divider](/previous-versions/ms583616(v=vs.100)) se encuentra en la [propiedad Strokes](/previous-versions/ms839422(v=msdn.10)) del objeto Divider. El objeto Divider analiza dinámicamente la colección Strokes a medida que agrega o elimina de la colección. Para obtener más información sobre la propiedad Strokes del objeto Divider, vea [Trabajar con una colección de trazos](working-with-a-strokes-collection.md).

El [objeto Divider](/previous-versions/ms583616(v=vs.100)) usa un contexto de reconocedor para mejorar su análisis de segmentos de reconocimiento y para generar texto de reconocimiento para los elementos de escritura a mano. Puede establecer el contexto del reconocedor mediante la [propiedad RecognizerContext](/previous-versions/ms839415(v=msdn.10)) del objeto Divider. No se puede cambiar la propiedad RecognizerContext después de asignar trazos al objeto Divider. Para obtener más información sobre la propiedad RecognizerContext del objeto Divider, vea [Trabajar con un contexto de reconocedor.](working-with-a-recognizer-context.md)

> [!Caution]  
> En el código administrado, debe llamar al [método Dispose](/previous-versions/ms839450(v=msdn.10)) en este objeto antes de que salga del ámbito. Este objeto mantiene los recursos no administrados. Confiar en la finalización de este objeto puede provocar pérdidas de memoria y excepciones en la aplicación.

 

 

 
