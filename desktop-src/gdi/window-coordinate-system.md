---
description: El sistema de coordenadas de una ventana se basa en el sistema de coordenadas del dispositivo de visualización.
ms.assetid: 8590fc59-d7ad-4149-9a77-242037a11188
title: Sistema de coordenadas de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c5492aaa02e1b2b2ace7e0cb02a65caa1faad320eca11414707145066308e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717875"
---
# <a name="window-coordinate-system"></a>Sistema de coordenadas de ventana

El sistema de coordenadas de una ventana se basa en el sistema de coordenadas del dispositivo de visualización. La unidad básica de medida es la unidad de dispositivo (normalmente, el píxel). Los puntos de la pantalla se describen mediante pares de coordenadas x e y. Las coordenadas x aumentan a la derecha; Las coordenadas y aumentan de arriba a abajo. El origen (0,0) del sistema depende del tipo de coordenadas que se usen.

El sistema y las aplicaciones especifican la posición de una ventana en la pantalla en coordenadas *de pantalla.* Para las coordenadas de pantalla, el origen es la esquina superior izquierda de la pantalla. La posición completa de una ventana a menudo se describe mediante una estructura [**RECT**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas de pantalla de dos puntos que definen las esquinas superior izquierda e inferior derecha de la ventana.

El sistema y las aplicaciones especifican la posición de los puntos en una ventana mediante coordenadas *de cliente*. En este caso, el origen es la esquina superior izquierda de la ventana o el área de cliente. Las coordenadas de cliente garantizan que una aplicación puede usar valores de coordenadas coherentes al dibujar en la ventana, independientemente de la posición de la ventana en la pantalla.

Las dimensiones del área de cliente también se describen mediante una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que contiene coordenadas de cliente para el área. En todos los casos, la coordenada superior izquierda del rectángulo se incluye en el área de ventana o cliente, mientras que la coordenada inferior derecha se excluye. Las operaciones de gráficos en una ventana o área cliente se excluyen de los bordes derecho e inferior del rectángulo que lo incluye.

En ocasiones, es posible que las aplicaciones deba asignar coordenadas de una ventana a las de otra ventana. Una aplicación puede asignar coordenadas mediante la [**función MapWindowPoints.**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints) Si una de las ventanas es la ventana de escritorio, la función convierte eficazmente las coordenadas de pantalla en coordenadas de cliente y viceversa. la ventana de escritorio siempre se especifica en coordenadas de pantalla.

 

 
