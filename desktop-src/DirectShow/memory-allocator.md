---
description: Asignador de memoria
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Asignador de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9346cf35e9383ff79e3dc5dafe54c0857a3f6f8818d9d137ae92bd1e6f98977d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584155"
---
# <a name="memory-allocator"></a>Asignador de memoria

El objeto Asignador de memoria asigna búferes para ejemplos multimedia. Los filtros pueden usar este objeto para asignar búferes de memoria compartida; sin embargo, un filtro con requisitos especiales también puede implementar su propio objeto de asignador de memoria. Cree este objeto mediante una llamada **a CoCreateInstance**.



| Etiqueta | Valor |
|------------------|----------------------------------------|
| Identificador de clase | CLSID \_ MemoryAllocator                 |
| Interfaces       | [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Objetos](directshow-objects.md)
</dt> </dl>

 

 



