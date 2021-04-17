---
description: El volteo de páginas es importante en el software multimedia, de animación y de juegos. es análogo a la forma en que se puede realizar la animación con un panel de papel.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Intercambio de páginas y almacenamiento en búfer de retroceso (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bffad581c5d4250c7f36980ba1f278a9f770912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714689"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a>Intercambio de páginas y almacenamiento en búfer de retroceso (Direct3D 9)

El volteo de páginas es importante en el software multimedia, de animación y de juegos. es análogo a la forma en que se puede realizar la animación con un panel de papel. En cada página, el artista cambia ligeramente la figura, de modo que cuando se gira rápidamente entre las hojas, el dibujo aparece animado.

El volteo de páginas del software es similar a este proceso. Direct3D implementa la funcionalidad de volteo de páginas a través de una cadena de intercambio, que es una propiedad del dispositivo. Inicialmente, se configura una serie de búferes de Direct3D que se voltean a la pantalla en la forma en que el papel del artista se mueve a la página siguiente. El primer búfer se conoce como el búfer frontal de color. Los búferes subyacentes se denominan búferes de reserva. La aplicación escribe en un búfer de reserva y, a continuación, voltea el búfer frontal de color para que el búfer de reserva aparezca en la pantalla. Mientras el sistema muestra la imagen, el software vuelve a escribir en un búfer de reserva. El proceso continúa mientras se anima, lo que permite animar imágenes de forma eficaz.

Direct3D facilita la configuración de esquemas de volteo de páginas: desde un simple esquema de doble búfer (un búfer frontal de color con un búfer de reserva) a esquemas más sofisticados con búferes de reserva adicionales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> <dt>

[¿Qué es una cadena de intercambio? (Direct3D 9)](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



