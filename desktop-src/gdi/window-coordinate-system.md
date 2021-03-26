---
description: El sistema de coordenadas de una ventana se basa en el sistema de coordenadas del dispositivo de pantalla.
ms.assetid: 8590fc59-d7ad-4149-9a77-242037a11188
title: Sistema de coordenadas de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69c5faa7359700af8a3bb04413fa9b25648b0cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813022"
---
# <a name="window-coordinate-system"></a>Sistema de coordenadas de ventana

El sistema de coordenadas de una ventana se basa en el sistema de coordenadas del dispositivo de pantalla. La unidad de medida básica es la unidad del dispositivo (normalmente, el píxel). Los puntos de la pantalla se describen mediante los pares de coordenadas x e y. Las coordenadas x aumentan a la derecha; las coordenadas y aumentan de arriba a abajo. El origen (0,0) del sistema depende del tipo de coordenadas que se estén usando.

El sistema y las aplicaciones especifican la posición de una ventana en la pantalla en coordenadas de la *pantalla*. En el caso de las coordenadas de pantalla, el origen es la esquina superior izquierda de la pantalla. La posición completa de una ventana suele describirse mediante una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas de pantalla de dos puntos que definen las esquinas superior izquierda e inferior derecha de la ventana.

El sistema y las aplicaciones especifican la posición de los puntos en una ventana mediante las *coordenadas de cliente*. El origen en este caso es la esquina superior izquierda del área de la ventana o cliente. Las coordenadas de cliente garantizan que una aplicación puede usar valores de coordenadas coherentes mientras se dibuja en la ventana, independientemente de la posición de la ventana en la pantalla.

Las dimensiones del área cliente también se describen mediante una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene coordenadas de cliente para el área. En todos los casos, la coordenada superior izquierda del rectángulo se incluye en el área de ventana o cliente, mientras que la coordenada inferior derecha se excluye. Las operaciones de gráficos en una ventana o área cliente se excluyen de los bordes derecho e inferior del rectángulo envolvente.

En ocasiones, es posible que las aplicaciones necesiten asignar coordenadas en una ventana a las de otra ventana. Una aplicación puede asignar coordenadas mediante la función [**MapWindowPoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints) . Si una de las ventanas es la ventana del escritorio, la función convierte eficazmente las coordenadas de la pantalla en coordenadas de cliente y viceversa. la ventana de escritorio siempre se especifica en coordenadas de pantalla.

 

 
