---
description: El volteo de página es clave en el software multimedia, de animación y de juegos. es análogo a la forma en que se puede realizar la animación con un panel de papel.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Volteo de página y almacenamiento en búfer hacia atrás (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134f1797300a838e453abf6811ae35b8f576e46c89ca0e929d2326b43ffea274
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746935"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a>Volteo de página y almacenamiento en búfer hacia atrás (Direct3D 9)

El volteo de página es clave en el software multimedia, de animación y de juegos. es análogo a la forma en que se puede realizar la animación con un panel de papel. En cada página, el intérprete cambia ligeramente la figura, de modo que cuando se voltea rápidamente entre hojas, el dibujo aparece animado.

El cambio de página en el software es similar a este proceso. Direct3D implementa la funcionalidad de volteo de página a través de una cadena de intercambio, que es una propiedad del dispositivo. Inicialmente, se configura una serie de búferes de Direct3D que se voltea a la pantalla de la manera en que el papel del intérprete se voltea a la página siguiente. El primer búfer se conoce como búfer frontal de color. Los búferes subyacentes se denominan búferes de reserva. La aplicación escribe en un búfer de reserva y, a continuación, invierte el búfer frontal de color para que el búfer de reserva aparezca en la pantalla. Mientras el sistema muestra la imagen, el software vuelve a escribir en un búfer de reserva. El proceso continúa mientras se anima, lo que le permite animar imágenes de forma eficaz.

Direct3D facilita la configuración de esquemas de volteo de página, desde un esquema simple de doble búfer (un búfer frontal de color con un búfer de reserva) a esquemas más sofisticados con búferes de reserva adicionales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> <dt>

[¿Qué es una cadena de intercambio? (Direct3D 9)](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



