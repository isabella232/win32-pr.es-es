---
description: Escala de tiempo
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: Escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f298c2649a280bf5fd622d5fb5a2aef820d1f340d45f7e2beb83fe9edd6a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050005"
---
# <a name="the-timeline"></a>Escala de tiempo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

La escala de tiempo expone la [**interfaz IAMTimeline.**](iamtimeline.md) Esta interfaz contiene métodos para establecer propiedades en la escala de tiempo; para agregar grupos a la escala de tiempo; y para crear objetos de escala de tiempo, como grupos, pistas y orígenes. Para crear una nueva escala de tiempo, llame a la **función CoCreateInstance** estándar como se muestra a continuación:


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



La nueva escala de tiempo está vacía. En este punto, puede cargar un archivo de proyecto existente (consulte Carga y vista previa de un [Project)](loading-and-previewing-a-project.md)o compilar la escala de tiempo mediante la creación e inserción de nuevos objetos (vea Construcción de una escala de [tiempo).](constructing-a-timeline.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de los componentes de escala de tiempo](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



