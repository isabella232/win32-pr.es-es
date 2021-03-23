---
title: Niveles de hardware
description: Los niveles de hardware del nivel 1 al nivel 3 tienen recursos crecientes disponibles para la canalización.
ms.assetid: 5A640BA9-3914-4481-9A0C-E18B52BD8AFE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38773412d135aa4068f0f843c1a6ef64af06a841
ms.sourcegitcommit: 9d7585cb0b840d0d1a2b7fd02135181e69d0dc9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/15/2020
ms.locfileid: "104549070"
---
# <a name="hardware-tiers"></a>Niveles de hardware

Los niveles de hardware del nivel 1 al nivel 3 tienen recursos crecientes disponibles para la canalización.

-   [Límites dependientes del hardware](#limits-dependant-on-hardware)
-   [Límites invariables](#invariable-limits)
-   [Temas relacionados](#related-topics)

## <a name="limits-dependant-on-hardware"></a>Límites dependientes del hardware



| Recursos disponibles para la canalización                                                                                                              | Nivel 1                                                                   | Nivel 2        | Nivel 3        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|---------------|
| Niveles de características                                                                                                                                   | 11.0 +                                                                    | 11.0 +         | 11.1 +         |
| Número máximo de descriptores en un montón de vista de búfer de constantes (CBV), sombreador Vista de recursos (SRV) o vista de acceso desordenado (UAV) que se usa para la representación | 1 000 000                                                                | 1 000 000     | 1000000 +    |
| Número máximo de vistas de búfer constantes en todas las tablas de descriptores por fase de sombreador                                                                | 14                                                                       | 14            | **montón completo** |
| Número máximo de vistas de recursos de sombreador en todas las tablas de descriptores por fase de sombreador                                                                | 128                                                                      | **montón completo** | montón completo     |
| Número máximo de vistas de acceso desordenado en todas las tablas de descriptores en todas las fases                                                              | 64 para los niveles de características 11.1 +<br/> 8 para el nivel de característica 11<br/> | 64            | **montón completo** |
| Número máximo de muestras en todas las tablas de descriptores por fase de sombreador                                                                             | 16                                                                       | **2048** | 2048     |



 

Las entradas en **negrita** destacan mejoras significativas en el nivel anterior.

Existe una restricción adicional para el hardware de nivel 1 que se aplica a todos los montones, y al hardware de nivel 2 que se aplica a los montones CBV y UAV, que todas las entradas del montón de descriptores que se incluyen en las tablas de descriptor de la firma raíz se *deben* rellenar con descriptores en el momento en que se ejecuta el sombreador No hay ninguna restricción para el hardware de nivel 3. Una mitigación de esta restricción es el uso diligente de [descriptores null](descriptors.md).

## <a name="invariable-limits"></a>Límites invariables

El número máximo de muestras en un montón de descriptor visible del sombreador es 2048.

El número máximo de muestras estáticas únicas en las firmas de raíz dinámica es 2032 (que deja 16 para los controladores que necesitan sus propios muestreadores).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> <dt>

[Niveles de características de hardware](hardware-feature-levels.md)
</dt> </dl>

 

 





