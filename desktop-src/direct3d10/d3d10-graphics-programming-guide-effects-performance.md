---
description: Consideraciones de rendimiento (Direct3D 10)
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: Consideraciones de rendimiento (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81247041ff5e4619445ab5a2455af708a9a545be38b8f321dc2d77696e9a83c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096685"
---
# <a name="performance-considerations-direct3d-10"></a>Consideraciones de rendimiento (Direct3D 10)

## <a name="using-effect-pools"></a>Uso de grupos de efectos

Es habitual que las canalizaciones de representación usen muchos sombreadores para representar diferentes tipos de objetos y efectos especiales. El sombreador es una combinación de estados que son comunes entre todos los sombreadores, como una matriz del mundo o una posición ligera, y otro estado específico de cada sombreador, como el color difuso de un objeto o el cálculo de resaltado especular. Un grupo de efectos es un lugar en la memoria para almacenar el estado que se usa en muchos sombreadores, así como objetos de dispositivo comunes, como sombreadores, objetos de estado de representación y búferes constantes. La mejora del rendimiento se debe a la actualización del estado común una vez para todos los sombreadores que necesitan ese estado.

Un grupo de efectos es una ubicación de memoria compartida para el estado del efecto. Un grupo se crea de forma similar a un efecto; se puede crear a partir de la memoria (o un archivo o un recurso). Esto conduce a dos tipos diferentes de efectos: un efecto global que no depende del estado de otro efecto frente a un efecto secundario que depende del estado de otro efecto.

Especifique si un efecto es un efecto global (el caso predeterminado) o un efecto secundario (al proporcionar la marca [D3D10 \_ EFFECT COMPILE CHILD \_ \_ \_ EFFECT)](d3d10-effect.md) cuando se crea el efecto. Un efecto global puede actuar como un grupo de efectos; un efecto secundario no puede ser un grupo de efectos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de un efecto](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[Efectos (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



