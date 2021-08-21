---
title: Subasignación en los búferes
description: Los montones de recursos transfieren datos de la CPU a la GPU (carga) y de la GPU a la CPU (read back).
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bdda33f1db1b0f798e9c3d18d8b3f33f7fbc30638ae6d62d38c0d5e2767463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912141"
---
# <a name="suballocation-within-heaps"></a>Subasignación en los búferes

Los montones de recursos transfieren datos de la CPU a la GPU (carga) y de la GPU a la CPU (read back).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Alias de memoria y herencia de datos](memory-aliasing-and-data-inheritance.md)<br/> | Los recursos colocados y reservados pueden crear un alias de memoria física dentro de un montón. Los recursos colocados permiten más escenarios de herencia de datos que recursos reservados cuando el montón tiene establecida la marca compartida o cuando los recursos con alias tienen diseños de memoria totalmente definidos. <br/> |
| [Montones compartidos](shared-heaps.md)<br/>                                                 | El uso compartido es útil para arquitecturas de varios procesos y adaptadores.<br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID3D12Device::CreateHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Administración de memoria](memory-management.md)
</dt> </dl>

 

 





