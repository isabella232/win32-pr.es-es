---
description: Asignador de memoria
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Asignador de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be12e25886eda968a00b10386a6eac3fd36e7279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537804"
---
# <a name="memory-allocator"></a>Asignador de memoria

El objeto de asignador de memoria asigna búferes para los ejemplos de medios. Los filtros pueden utilizar este objeto para asignar búferes de memoria compartida; sin embargo, un filtro con requisitos especiales también puede implementar su propio objeto de asignador de memoria. Cree este objeto llamando a **CoCreateInstance**.



|                  |                                        |
|------------------|----------------------------------------|
| Identificador de clase | CLSID \_ MemoryAllocator                 |
| Interfaces       | [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de DirectShow](directshow-objects.md)
</dt> </dl>

 

 



