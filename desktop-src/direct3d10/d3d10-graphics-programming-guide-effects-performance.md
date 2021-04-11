---
description: Consideraciones de rendimiento (Direct3D 10)
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: Consideraciones de rendimiento (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba2dbe00475efebdb6ff5d772b3eccd6cd4263a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080143"
---
# <a name="performance-considerations-direct3d-10"></a>Consideraciones de rendimiento (Direct3D 10)

## <a name="using-effect-pools"></a>Uso de grupos de efectos

Es habitual que las canalizaciones de representación utilicen muchos sombreadores para representar diferentes tipos de objeto y efectos especiales. El sombreador es una mezcla de Estados que es común entre todos los sombreadores, como una matriz mundial o una posición ligera, y otro estado específico de cada sombreador, como el color difuso de un objeto o el cálculo del resaltado especular. Un grupo de efectos es un lugar en la memoria para almacenar el estado que se usa en muchos sombreadores, así como objetos de dispositivo comunes como, por ejemplo, sombreadores, objetos de estado de representación y búferes de constantes. Los resultados de la mejora del rendimiento de la actualización del Estado común una vez para todos los sombreadores que necesitan ese estado.

Un grupo de efectos es una ubicación de memoria compartida para el estado de efecto. Un grupo se crea de forma similar a un efecto; se puede crear a partir de la memoria (o un archivo o un recurso). Esto conduce a dos tipos diferentes de efectos: un efecto global que no depende del estado en otro efecto frente a un efecto secundario que depende del estado de otro efecto.

Especifique si un efecto es un efecto global (el caso predeterminado) o un efecto secundario (proporcionando la marca de efecto de [ \_ \_ compilar efecto \_ secundario \_ de D3D10](d3d10-effect.md) ) cuando se crea el efecto. Un efecto global puede servir como grupo de efectos; un efecto secundario no puede ser un grupo de efectos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar un efecto](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[Efectos (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



