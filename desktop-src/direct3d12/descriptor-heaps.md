---
title: Montones de descriptores
description: Un montón de descriptores es una colección de asignaciones contiguas de descriptores, una asignación para cada descriptor.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f19821cff5e8730c376e5c80fef07e67974d31d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104865"
---
# <a name="descriptor-heaps"></a>Montones de descriptores

Un montón de descriptores es una colección de asignaciones contiguas de descriptores, una asignación para cada descriptor.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Información general sobre montones de descriptores](descriptor-heaps-overview.md)<br/>                             | Los montones descriptores contienen muchos tipos de objetos que no forman parte de un objeto de estado de canalización (PSO), como las vistas de recursos del sombreador (SRVs), las vistas de acceso desordenado (UAVs), las vistas de búfer de constantes (CBVs) y los muestreadores. <br/>                |
| [Niveles de hardware](hardware-support.md)<br/>                                                 | Los niveles de hardware del nivel 1 al nivel 3 tienen recursos crecientes disponibles para la canalización. <br/>                                                                                                                              |
| [Montones de descriptor visibles del sombreador](shader-visible-descriptor-heaps.md)<br/>                 | Los montones de descriptor visibles del sombreador, son montones de descriptor a los que pueden hacer referencia los sombreadores a través de tablas de descriptores.<br/>                                                                                                              |
| [Montones de descriptor visibles sin sombreador](non-shader-visible-descriptor-heaps.md)<br/>         | Los sombreadores no pueden hacer referencia a algunos montones de descriptor a través de tablas de descriptores, pero existen para ayudar a la aplicación a ensayar los descriptores antes de grabar una lista de comandos o porque no se requiere ningún montón visible del sombreador.<br/> |
| [Crear montones de descriptor](creating-descriptor-heaps.md)<br/>                             | Para crear y configurar un montón de descriptores, debe seleccionar un tipo de montón de descriptores, determinar el número de descriptores que contiene y establecer marcas que indiquen si es visible para la CPU o el sombreador. <br/>                    |
| [Establecer y rellenar montones de descriptores](setting-descriptor-heaps.md)<br/>                | Los tipos de montón descriptor que se pueden establecer en una lista de comandos son aquellos que contienen descriptores para los que se pueden usar tablas de descriptor (como máximo una de cada cada vez). <br/>                                                        |
| [Resumen de la capacidad de configurar el montón de descriptores](descriptor-heap-configurability-summary.md)<br/> | En la tabla siguiente se resume la información sobre el sombreador y la compatibilidad con el montón visible de no sombreador.<br/>                                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descriptores de](descriptors.md)
</dt> <dt>

[Tablas de descriptores](descriptor-tables.md)
</dt> <dt>

[**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[Enlace de recursos](resource-binding.md)
</dt> <dt>

[Firmas raíz](root-signatures.md)
</dt> </dl>

 

 





