---
description: La escala de tiempo
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: La escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6ac73b84409629f63ad4be469edf6b943f9e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688739"
---
# <a name="the-timeline"></a>La escala de tiempo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

La escala de tiempo expone la interfaz [**IAMTimeline**](iamtimeline.md) . Esta interfaz contiene métodos para establecer las propiedades de la escala de tiempo; para agregar grupos a la escala de tiempo; y para crear objetos timeline, como grupos, pistas y orígenes. Para crear una nueva escala de tiempo, llame a la función **CoCreateInstance** estándar como se indica a continuación:


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



La nueva escala de tiempo está vacía. En este momento, puede cargar un archivo de proyecto existente (vea [cargar y obtener una vista previa de un proyecto](loading-and-previewing-a-project.md)) o crear la escala de tiempo creando e insertando objetos nuevos (vea [construir una escala de tiempo](constructing-a-timeline.md)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de los componentes de la escala de tiempo](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



