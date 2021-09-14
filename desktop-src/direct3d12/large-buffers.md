---
title: Subasignación en los búferes
description: Los búferes tienen todas las características necesarias en D3D12 para que las aplicaciones transfieran una gran variedad de datos transitorios de la CPU a la GPU. En esta sección se tratan cuatro escenarios comunes para el uso y la administración de recursos y búferes.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64944cb11507b8dc437d075938fad419f333433
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072955"
---
# <a name="suballocation-within-buffers"></a>Subasignación en los búferes

Los búferes tienen todas las características necesarias en D3D12 para que las aplicaciones transfieran una gran variedad de datos transitorios de la CPU a la GPU. En esta sección se tratan cuatro escenarios comunes para el uso y la administración de recursos y búferes.

De forma similar a D3D11, las aplicaciones de D3D12 todavía necesitan declarar el uso de memoria al asignar búferes en D3D12 en comparación con los recursos dinámicos y de ensayo en D3D11, pero en D3D12, los desarrolladores tienen más flexibilidad y un control más estricto sobre el uso de memoria. Los búferes, mediante suballocation, tienen todas las características necesarias para la administración de memoria de bajo nivel.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Carga de diferentes tipos de recursos](uploading-resources.md)<br/>                 | Muestra cómo usar un búfer para cargar datos de búfer constante y datos de búfer de vértices en la GPU, y cómo subasigna y coloca correctamente los datos en búferes. El uso de un solo búfer aumenta la flexibilidad de uso de memoria y proporciona a las aplicaciones un control más estricto del uso de memoria. También se muestran las diferencias entre los modelos D3D11 y D3D12 para cargar diferentes tipos de recursos.<br/> |
| [Carga de datos de textura a través de búferes](upload-and-readback-of-texture-data.md)<br/> | La carga de datos de textura 2D o 3D es similar a la carga de datos 1D, salvo que las aplicaciones deben prestar más atención a la alineación de datos relacionada con el tono de fila. Los búferes se pueden usar ortogonal y simultáneamente desde varias partes de la canalización de gráficos, y son muy flexibles. <br/>                                                                                                                       |
| [Lectura de datos a través de un búfer](readback-data-using-heaps.md)<br/>                    | La lectura de datos de la GPU, como la captura de pantalla, implica el uso del montón readback. <br/>                                                                                                                                                                                                                                                                                                     |
| [Administración de recursos basada en límites](fence-based-resource-management.md)<br/>            | Muestra cómo administrar la duración de los datos de recursos mediante el seguimiento del progreso de la GPU a través de barreras. La memoria se puede volver a usar de forma eficaz con barreras que administran cuidadosamente la disponibilidad de espacio disponible en la memoria, como en una implementación de búfer en anillo para un montón Upload de almacenamiento. <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de memoria](memory-management.md)
</dt> </dl>

 

 





