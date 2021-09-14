---
title: Administración de la memoria en Direct3D 12
description: El traslado a D3D12 implica realizar la sincronización y administración adecuadas de la residencia de memoria.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b8091c2893f8906fe2ab5baadbf1288a1474cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072942"
---
# <a name="memory-management-in-direct3d-12"></a>Administración de la memoria en Direct3D 12

El traslado a D3D12 implica realizar la sincronización y administración adecuadas de la residencia de memoria. La administración de la residencia de memoria significa que se debe realizar aún más sincronización. En esta sección se tratan las estrategias de administración de memoria y la suballocation dentro de montones y búferes.

-   [En esta sección](#in-this-section)
-   [Temas relacionados](#related-topics)

## <a name="in-this-section"></a>En esta sección



| Tema                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Estrategias de administración de la memoria](memory-management-strategies.md)<br/> | Un administrador de memoria para Direct3D 12 podría complicarse rápidamente con todos los distintos niveles de compatibilidad, para adaptadores UMA o discretos (no UMA) y con una gran variedad de diferencias de arquitectura entre los adaptadores de GPU.<br/> La estrategia recomendada para la administración de memoria de Direct3D 12, descrita en esta sección, es "clasificar, presupuesto y flujo".<br/> |
| [Subasignación en los búferes](large-buffers.md)<br/>                | Los búferes tienen todas las características necesarias en D3D12 para que las aplicaciones transfieran una gran variedad de datos transitorios de la CPU a la GPU. En esta sección se tratan cuatro escenarios comunes para el uso y la administración de recursos y búferes.<br/>                                                                                                                                     |
| [Subasignación en los búferes](suballocation-within-heaps.md)<br/>     | Los montones de recursos transfieren datos de la CPU a la GPU (carga) y de la GPU a la CPU (read back). <br/>                                                                                                                                                                                                                                                                  |
| [Residencia](residency.md)<br/>                                       | Se considera que un objeto es *residentes cuando* la GPU puede acceder a él.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Enlace de recursos](resource-binding.md)
</dt> </dl>

 

 





