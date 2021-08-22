---
title: Subasignación en los búferes
description: Los búferes tienen todas las características necesarias en D3D12 para que las aplicaciones transfieran una gran variedad de datos transitorios de la CPU a la GPU. En esta sección se tratan cuatro escenarios comunes para el uso y la administración de recursos y búferes.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63175bdb8b3937a01abe3ffc57032db78ea978768ee19e2c31d0c50db4103573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123818"
---
# <a name="suballocation-within-buffers"></a>Subasignación en los búferes

Los búferes tienen todas las características necesarias en D3D12 para que las aplicaciones transfieran una gran variedad de datos transitorios de la CPU a la GPU. En esta sección se tratan cuatro escenarios comunes para el uso y la administración de recursos y búferes.

De forma similar a D3D11, las aplicaciones de D3D12 todavía necesitan declarar el uso de memoria al asignar búferes en D3D12 en comparación con los recursos dinámicos o de ensayo en D3D11, pero en D3D12, los desarrolladores tienen más flexibilidad y un control más estricto sobre el uso de memoria. Los búferes, a través de la suballocation, tienen todas las características necesarias para la administración de memoria de bajo nivel.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Carga de diferentes tipos de recursos](uploading-resources.md)<br/>                 | Muestra cómo usar un búfer para cargar datos de búfer constante y datos de búfer de vértices en la GPU, y cómo subasigna y coloca correctamente los datos en búferes. El uso de un solo búfer aumenta la flexibilidad de uso de memoria y proporciona a las aplicaciones un control más estricto del uso de memoria. También se muestran las diferencias entre los modelos D3D11 y D3D12 para cargar diferentes tipos de recursos.<br/> |
| [Carga de datos de textura a través de búferes](upload-and-readback-of-texture-data.md)<br/> | La carga de datos de textura 2D o 3D es similar a la carga de datos 1D, salvo que las aplicaciones necesitan prestar más atención a la alineación de datos relacionada con el tono de fila. Los búferes se pueden usar ortogonalmente y simultáneamente desde varias partes de la canalización de gráficos, y son muy flexibles. <br/>                                                                                                                       |
| [Lectura de datos a través de un búfer](readback-data-using-heaps.md)<br/>                    | La lectura de datos de la GPU, como capturar una captura de pantalla, implica el uso del montón de readback. <br/>                                                                                                                                                                                                                                                                                                     |
| [Administración de recursos basada en límites](fence-based-resource-management.md)<br/>            | Muestra cómo administrar el intervalo de vida de los datos de recursos mediante el seguimiento del progreso de la GPU a través de barreras. La memoria se puede volver a usar de forma eficaz con barreras que administran cuidadosamente la disponibilidad del espacio libre en la memoria, como en una implementación de búfer en anillo para un montón Upload anillo. <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de memoria](memory-management.md)
</dt> </dl>

 

 





