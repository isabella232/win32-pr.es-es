---
title: Niveles de hardware
description: Los niveles de hardware del nivel 1 al nivel 3 tienen cada vez más recursos disponibles para la canalización.
ms.assetid: 5A640BA9-3914-4481-9A0C-E18B52BD8AFE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38773412d135aa4068f0f843c1a6ef64af06a841
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258516"
---
# <a name="hardware-tiers"></a>Niveles de hardware

Los niveles de hardware del nivel 1 al nivel 3 tienen cada vez más recursos disponibles para la canalización.

-   [Límites dependientes del hardware](#limits-dependant-on-hardware)
-   [Límites invariables](#invariable-limits)
-   [Temas relacionados](#related-topics)

## <a name="limits-dependant-on-hardware"></a>Límites dependientes del hardware



| Recursos disponibles para la canalización                                                                                                              | Nivel 1                                                                   | Nivel 2        | Nivel 3        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|---------------|
| Niveles de características                                                                                                                                   | Versión 11.0 y posteriores                                                                    | Versión 11.0 y posteriores         | 11.1+         |
| Número máximo de descriptores en un montón de vista de búfer constante (CBV), Vista de recursos sombreador (SRV) o unordered Access View (UAV) usado para la representación | 1 000 000                                                                | 1 000 000     | 1,000,000+    |
| Número máximo de vistas de búfer constante en todas las tablas de descriptores por fase de sombreador                                                                | 14                                                                       | 14            | **montón completo** |
| Número máximo de vistas de recursos de sombreador en todas las tablas de descriptores por fase de sombreador                                                                | 128                                                                      | **montón completo** | montón completo     |
| Número máximo de vistas de acceso desordenadas en todas las tablas de descriptores en todas las fases                                                              | 64 para los niveles de características 11.1+<br/> 8 para el nivel de característica 11<br/> | 64            | **montón completo** |
| Número máximo de muestreadores en todas las tablas de descriptores por fase de sombreador                                                                             | 16                                                                       | **2048** | 2048     |



 

**Las** entradas en negrita resaltan mejoras significativas con respecto al nivel anterior.

Hay una restricción adicional para el hardware de nivel 1 que se aplica a todos los montones, y para el hardware de nivel 2 que  se aplica a los montones CBV y UAV, de que todas las entradas del montón de descriptores cubiertas por tablas de descriptores en la firma raíz deben rellenarse con descriptores en el momento en que se ejecuta el sombreador, incluso si el sombreador (quizás debido a la bifurcación) no necesita el descriptor. No hay ninguna restricción de este tipo para el hardware de nivel 3. Una mitigación de esta restricción es el uso diligente de [descriptores NULL](descriptors.md).

## <a name="invariable-limits"></a>Límites invariables

El número máximo de muestreadores en un montón de descriptores visibles del sombreador es 2048.

El número máximo de muestreadores estáticos únicos en las firmas raíz en directo es 2032 (lo que deja 16 para los controladores que necesitan sus propios muestreadores).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> <dt>

[Niveles de características de hardware](hardware-feature-levels.md)
</dt> </dl>

 

 





