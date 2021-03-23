---
title: Subasignación dentro de montones
description: Los montones de recursos transfieren datos de la CPU a la GPU (carga) y de la GPU a la CPU (lectura inversa).
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701e68e31e698bbf2c955a252bd46876f45d6b7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105027"
---
# <a name="suballocation-within-heaps"></a>Subasignación dentro de montones

Los montones de recursos transfieren datos de la CPU a la GPU (carga) y de la GPU a la CPU (lectura inversa).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Alias de memoria y herencia de datos](memory-aliasing-and-data-inheritance.md)<br/> | Los recursos colocados y reservados pueden asignar un alias a la memoria física dentro de un montón. Los recursos colocados permiten más escenarios de herencia de datos que los recursos reservados cuando el montón tiene establecida la marca compartida o cuando los recursos con alias tienen diseños de memoria totalmente definidos. <br/> |
| [Montones compartidos](shared-heaps.md)<br/>                                                 | Compartir es útil para arquitecturas multiproceso y multiadaptador.<br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID3D12Device::CreateHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Administración de memoria](memory-management.md)
</dt> </dl>

 

 





