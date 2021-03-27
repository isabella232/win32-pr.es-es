---
description: La animación de paleta es una técnica para simular el movimiento mediante el cambio rápido de los colores de las entradas seleccionadas en una paleta de colores.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Animación de paleta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9761e99033e7a01fa875fce7c41e5a35cf40ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811905"
---
# <a name="palette-animation"></a>Animación de paleta

La animación de paleta es una técnica para simular el movimiento mediante el cambio rápido de los colores de las entradas seleccionadas en una paleta de colores. Una aplicación puede llevar a cabo la animación de la paleta mediante la creación de una paleta lógica que contiene entradas "reservadas" y, a continuación, el uso de la función [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) para cambiar los colores de esas entradas reservadas.

Una aplicación crea una entrada reservada en una paleta lógica estableciendo el miembro **peFlags** de la estructura [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85)) en la \_ marca reservada de PC. Una vez seleccionada y realizada esta paleta lógica, la aplicación puede llamar a la función [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) para cambiar una o varias entradas reservadas. Si la paleta determinada está asociada a la ventana activa, el sistema actualiza los colores de la pantalla inmediatamente.

 

 
