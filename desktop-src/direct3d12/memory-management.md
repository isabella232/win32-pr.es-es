---
title: Administración de memoria en Direct3D 12
description: Pasar a D3D12 implica realizar la sincronización y administración adecuadas de la residencia de memoria.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037a2d75adcde6ff03adf2ccee8ce30d33d090c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103926"
---
# <a name="memory-management-in-direct3d-12"></a>Administración de memoria en Direct3D 12

Pasar a D3D12 implica realizar la sincronización y administración adecuadas de la residencia de memoria. La administración de la residencia de memoria significa que se debe realizar aún más sincronización. En esta sección se tratan las estrategias de administración de memoria y la subasignación en montones y búferes.

-   [En esta sección](#in-this-section)
-   [Temas relacionados](#related-topics)

## <a name="in-this-section"></a>En esta sección



| Tema                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Estrategias de administración de memoria](memory-management-strategies.md)<br/> | Un administrador de memoria para Direct3D 12 podría resultar muy complicado rápidamente con los distintos niveles de compatibilidad, para los adaptadores de UMA o discretos (no UMA), y con una gran variedad de diferencias de arquitectura entre los adaptadores de GPU.<br/> La estrategia recomendada para la administración de memoria de Direct3D 12, que se describe en esta sección, es "clasificación, presupuesto y flujo".<br/> |
| [Subasignación dentro de búferes](large-buffers.md)<br/>                | Los búferes tienen todas las características necesarias en D3D12 para que las aplicaciones transfieran una gran variedad de datos transitorios de la CPU a la GPU. En esta sección se tratan cuatro escenarios comunes para el uso y la administración de recursos y búferes.<br/>                                                                                                                                     |
| [Subasignación dentro de montones](suballocation-within-heaps.md)<br/>     | Los montones de recursos transfieren datos de la CPU a la GPU (carga) y de la GPU a la CPU (lectura inversa). <br/>                                                                                                                                                                                                                                                                  |
| [Residencia](residency.md)<br/>                                       | Un objeto se considera *residente* cuando es accesible para la GPU.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Enlace de recursos](resource-binding.md)
</dt> </dl>

 

 





