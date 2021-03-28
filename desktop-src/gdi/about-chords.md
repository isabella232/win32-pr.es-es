---
description: Una cuerda es una región enlazada por la intersección de una elipse y un segmento de línea denominado secante. En la ilustración siguiente se muestra una cuerda dibujada con la función de cuerda.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: Acerca de las cuerda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d6310c47a503766e61b9c7936816a5891da89a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543630"
---
# <a name="about-chords"></a>Acerca de las cuerda

Una *cuerda* es una región enlazada por la intersección de una elipse y un segmento de línea denominado *secante*. En la ilustración siguiente se muestra una cuerda dibujada con la función de [**cuerda**](/windows/desktop/api/Wingdi/nf-wingdi-chord) .

![Ilustración de un elipse, que muestra dos radiales, una secante y una cuerda](images/csfsh-02.png)

Al llamar a [**cuerda**](/windows/win32/api/wingdi/nf-wingdi-chord), una aplicación proporciona las coordenadas de las esquinas superior izquierda e inferior derecha del rectángulo delimitador de la elipse, así como las coordenadas de dos puntos que definen dos radiales. Un radial es una línea dibujada desde el centro del rectángulo delimitador de una elipse hasta un punto de la elipse.

Cuando el sistema dibuja la parte curvada de la cuerda, lo hace mediante el uso de la dirección de arco actual para el contexto de dispositivo especificado. La dirección de arco predeterminada es en sentido contrario a las agujas del reloj. Puede hacer que la aplicación restablezca la dirección del arco llamando a la función [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .

 

 
