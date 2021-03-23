---
title: Subasignación dentro de búferes
description: Los búferes tienen todas las características necesarias en D3D12 para que las aplicaciones transfieran una gran variedad de datos transitorios de la CPU a la GPU. En esta sección se tratan cuatro escenarios comunes para el uso y la administración de recursos y búferes.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64944cb11507b8dc437d075938fad419f333433
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103841"
---
# <a name="suballocation-within-buffers"></a>Subasignación dentro de búferes

Los búferes tienen todas las características necesarias en D3D12 para que las aplicaciones transfieran una gran variedad de datos transitorios de la CPU a la GPU. En esta sección se tratan cuatro escenarios comunes para el uso y la administración de recursos y búferes.

De forma similar a D3D11, las aplicaciones de D3D12 todavía tienen que declarar el uso de memoria cuando se asignan búferes en D3D12 en comparación con recursos dinámicos o de ensayo en D3D11, pero en D3D12, los desarrolladores tienen más flexibilidad y mayor control sobre el uso de memoria. Los búferes, a través de la subasignación, tienen todas las características necesarias para la administración de memoria de bajo nivel.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cargar diferentes tipos de recursos](uploading-resources.md)<br/>                 | Muestra cómo utilizar un búfer para cargar datos de búfer de constantes y datos de búfer de vértices en la GPU, y cómo subasignar y colocar datos correctamente en los búferes. El uso de un único búfer aumenta la flexibilidad del uso de memoria y proporciona a las aplicaciones un control más estricto del uso de memoria. También se muestran las diferencias entre los modelos D3D11 y D3D12 para cargar diferentes tipos de recursos.<br/> |
| [Cargar datos de textura a través de búferes](upload-and-readback-of-texture-data.md)<br/> | La carga de datos de textura 2D o 3D es similar a la carga de datos 1D, salvo que las aplicaciones necesitan prestar atención a la alineación de datos relacionada con el paso de las filas. Los búferes se pueden usar de forma ortogonal y simultánea desde varias partes de la canalización de gráficos y son muy flexibles. <br/>                                                                                                                       |
| [Lectura de datos a través de un búfer](readback-data-using-heaps.md)<br/>                    | La lectura de datos de la GPU, como la captura de una captura de pantalla, implica el uso del montón Readback. <br/>                                                                                                                                                                                                                                                                                                     |
| [Administración de recursos basada en valla](fence-based-resource-management.md)<br/>            | Muestra cómo administrar la duración de los datos de recursos mediante el seguimiento del progreso de la GPU a través de vallas. La memoria se puede reutilizar eficazmente con barreras administrando cuidadosamente la disponibilidad de espacio libre en memoria, como en una implementación de búfer de anillo para un montón de carga. <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de memoria](memory-management.md)
</dt> </dl>

 

 





