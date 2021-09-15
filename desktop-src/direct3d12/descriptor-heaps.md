---
title: Montones de descriptores
description: Un montón de descriptores es una colección de asignaciones contiguas de descriptores, una asignación para cada descriptor.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f19821cff5e8730c376e5c80fef07e67974d31d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570877"
---
# <a name="descriptor-heaps"></a>Montones de descriptores

Un montón de descriptores es una colección de asignaciones contiguas de descriptores, una asignación para cada descriptor.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Información general sobre los montones de descriptores](descriptor-heaps-overview.md)<br/>                             | Los montones de descriptores contienen muchos tipos de objeto que no forman parte de un objeto de estado de canalización (PSO), como vistas de recursos de sombreador (SRV), vistas de acceso desordenado (UAV), vistas de búfer constante (CBV) y muestreadores. <br/>                |
| [Niveles de hardware](hardware-support.md)<br/>                                                 | Los niveles de hardware del nivel 1 al nivel 3 tienen cada vez más recursos disponibles para la canalización. <br/>                                                                                                                              |
| [Montones de descriptores visibles por el sombreador](shader-visible-descriptor-heaps.md)<br/>                 | Los montones de descriptores visibles del sombreador son montones de descriptores a los que pueden hacer referencia los sombreadores a través de tablas de descriptores.<br/>                                                                                                              |
| [Montones de descriptores no visibles por el sombreador](non-shader-visible-descriptor-heaps.md)<br/>         | Los sombreadores no pueden hacer referencia a algunos montones de descriptores a través de tablas de descriptores, pero existen para ayudar a la aplicación a almacenamiento provisional de los descriptores antes de registrar una lista de comandos o porque no se requiere ningún montón visible para el sombreador.<br/> |
| [Creación de montones de descriptores](creating-descriptor-heaps.md)<br/>                             | Para crear y configurar un montón de descriptores, debe seleccionar un tipo de montón de descriptores, determinar cuántos descriptores contiene y establecer marcas que indiquen si está visible en la CPU o en el sombreador. <br/>                    |
| [Configuración y relleno de los montones de descriptores](setting-descriptor-heaps.md)<br/>                | Los tipos de montón de descriptores que se pueden establecer en una lista de comandos son aquellos que contienen descriptores para los que se pueden usar tablas de descriptores (como máximo una de cada una a la vez). <br/>                                                        |
| [Resumen de la capacidad de configuración del montón de descriptores](descriptor-heap-configurability-summary.md)<br/> | En la tabla siguiente se resume información sobre la compatibilidad del montón visible de sombreador y no sombreador.<br/>                                                                                                                                    |



 

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

 

 





