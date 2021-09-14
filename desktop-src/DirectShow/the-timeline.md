---
description: Escala de tiempo
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: Escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6ac73b84409629f63ad4be469edf6b943f9e64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069993"
---
# <a name="the-timeline"></a>Escala de tiempo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

La escala de tiempo expone la [**interfaz IAMTimeline.**](iamtimeline.md) Esta interfaz contiene métodos para establecer propiedades en la escala de tiempo; para agregar grupos a la escala de tiempo; y para crear objetos de escala de tiempo, como grupos, pistas y orígenes. Para crear una nueva escala de tiempo, llame a la **función CoCreateInstance** estándar como se muestra a continuación:


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



La nueva escala de tiempo está vacía. En este punto, puede cargar un archivo de proyecto existente (consulte Carga y vista previa de un [Project)](loading-and-previewing-a-project.md)o compilar la escala de tiempo mediante la creación e inserción de nuevos objetos (vea [Construir](constructing-a-timeline.md)una escala de tiempo).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de los componentes de escala de tiempo](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



