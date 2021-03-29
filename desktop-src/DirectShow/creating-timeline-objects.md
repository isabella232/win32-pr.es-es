---
description: Crear objetos Timeline
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Crear objetos Timeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929fffb6a953e198b6e7ed9b17250d45e84f7932
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666107"
---
# <a name="creating-timeline-objects"></a>Crear objetos Timeline

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

El código de ejemplo que se presenta en este artículo comienza con una escala de tiempo vacía, pero se aplican los mismos pasos si carga un proyecto existente y desea agregarle objetos.

Para crear cualquier tipo de objeto en la escala de tiempo, llame al método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) . Por ejemplo, el código siguiente crea un nuevo Grupo:


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



El segundo parámetro es un miembro de la enumeración de [**\_ \_ tipo principal**](timeline-major-type.md) de la escala de tiempo. Especifica el tipo de objeto de escala de tiempo que se va a crear, como un grupo o una pista.

El método **CreateEmptyNode** crea el objeto y devuelve un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto. También incrementa el recuento de referencias en la interfaz **IAMTimelineObj** , por lo que debe liberar la interfaz cuando termine de usarla. No llame a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) . En su lugar, use siempre **CreateEmptyNode** para crear un objeto Timeline, ya que inicializa el nuevo objeto para su uso en una escala de tiempo.

La interfaz [**IAMTimelineObj**](iamtimelineobj.md) es una interfaz genérica. Proporciona métodos comunes a todos los tipos de objeto Timeline. Cada tipo de objeto expone también otras interfaces. Por ejemplo, los grupos exponen la interfaz [**IAMTimelineGroup**](iamtimelinegroup.md) , entre otros. Puede obtener punteros a las otras interfaces llamando a **QueryInterface**.

Después de crear un objeto, todavía no es parte de la escala de tiempo. El método para agregar un objeto a la escala de tiempo depende del tipo de objeto. En la sección siguiente se describe cómo agregar grupos, composiciones y pistas a la escala de tiempo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Construir una escala de tiempo](constructing-a-timeline.md)
</dt> </dl>

 

 
