---
description: Asignador de memoria
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Asignador de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072167"
---
# <a name="memory-allocator"></a>Asignador de memoria

El objeto Asignador de memoria asigna búferes para los ejemplos de medios. Los filtros pueden usar este objeto para asignar búferes de memoria compartida; sin embargo, un filtro con requisitos especiales también puede implementar su propio objeto de asignador de memoria. Cree este objeto mediante una llamada **a CoCreateInstance**.



| Etiqueta | Value |
|------------------|----------------------------------------|
| Identificador de clase | CLSID \_ MemoryAllocator                 |
| Interfaces       | [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Objetos](directshow-objects.md)
</dt> </dl>

 

 



