---
description: Crear objetos de escala de tiempo
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Crear objetos de escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c0a2a88b2cd931e6a9d12274f4a2503b4c97d52348b6ed2629c22bf204f302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054785"
---
# <a name="creating-timeline-objects"></a>Crear objetos de escala de tiempo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

El código de ejemplo presentado en este artículo comienza con una escala de tiempo vacía, pero se aplican los mismos pasos si carga un proyecto existente y desea agregarle objetos.

Para crear cualquier tipo de objeto en la escala de tiempo, llame al [**método IAMTimeline::CreateEmptyNode.**](iamtimeline-createemptynode.md) Por ejemplo, el código siguiente crea un nuevo grupo:


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



El segundo parámetro es miembro de la [**enumeración TIMELINE \_ MAJOR \_ TYPE.**](timeline-major-type.md) Especifica el tipo de objeto de escala de tiempo que se va a crear, como un grupo o una pista.

El **método CreateEmptyNode** crea el objeto y devuelve un puntero a la interfaz [**IAMTimelineObj del**](iamtimelineobj.md) objeto. También incrementa el recuento de referencias en la **interfaz IAMTimelineObj,** por lo que debe liberar la interfaz cuando termine de usarlo. No llame a la [**función CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) En su lugar, use **siempre CreateEmptyNode para** crear un objeto de escala de tiempo, ya que inicializa el nuevo objeto para su uso en una escala de tiempo.

La [**interfaz IAMTimelineObj**](iamtimelineobj.md) es una interfaz genérica. Proporciona métodos que son comunes a todos los tipos de objeto de escala de tiempo. Cada tipo de objeto también expone otras interfaces. Por ejemplo, los grupos exponen la [**interfaz IAMTimelineGroup,**](iamtimelinegroup.md) entre otros. Puede obtener punteros a las otras interfaces llamando a **QueryInterface**.

Después de crear un objeto, aún no forma parte de la escala de tiempo. El método para agregar un objeto a la escala de tiempo depende del tipo de objeto. En la sección siguiente se describe cómo agregar grupos, composiciones y pistas a la escala de tiempo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Construir una escala de tiempo](constructing-a-timeline.md)
</dt> </dl>

 

 
