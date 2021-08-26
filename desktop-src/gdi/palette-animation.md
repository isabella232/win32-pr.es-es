---
description: La animación de paleta es una técnica para simular el movimiento cambiando rápidamente los colores de las entradas seleccionadas en una paleta de colores.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Animación de paleta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ea2d557ddd071a8f8e993f3a797fb42c2f4fef9abc68fc13737cded96a18fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965595"
---
# <a name="palette-animation"></a>Animación de paleta

La animación de paleta es una técnica para simular el movimiento cambiando rápidamente los colores de las entradas seleccionadas en una paleta de colores. Una aplicación puede llevar a cabo la animación de paleta mediante la creación de una paleta lógica que contiene entradas "reservadas" y, a continuación, mediante la [**función AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) para cambiar los colores de esas entradas reservadas.

Una aplicación crea una entrada reservada en una paleta lógica estableciendo el **miembro peFlags** de la estructura [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85)) en la marca \_ RESERVADA de PC. Una vez seleccionada y realizada esta paleta lógica, la aplicación puede llamar a la [**función AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) para cambiar una o varias entradas reservadas. Si la paleta dada está asociada a la ventana activa, el sistema actualiza los colores en la pantalla inmediatamente.

 

 
