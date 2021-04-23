---
description: Asignador de memoria
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Asignador de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909432"
---
# <a name="memory-allocator"></a>Asignador de memoria

El objeto Asignador de memoria asigna búferes para ejemplos multimedia. Los filtros pueden usar este objeto para asignar búferes de memoria compartida. sin embargo, un filtro con requisitos especiales también puede implementar su propio objeto de asignador de memoria. Cree este objeto mediante una llamada **a CoCreateInstance**.



| Etiqueta | Value |
|------------------|----------------------------------------|
| Identificador de clase | CLSID \_ MemoryAllocator                 |
| Interfaces       | [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos DirectShow](directshow-objects.md)
</dt> </dl>

 

 



