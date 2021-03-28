---
description: El rectángulo delimitador acumulado es el rectángulo más pequeño que incluye la parte de una ventana o área cliente afectada por las operaciones de dibujo recientes.
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: Rectángulo delimitador acumulado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ae3237304af68a4b8ff447b7ea2d64d3f81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544558"
---
# <a name="accumulated-bounding-rectangle"></a>Rectángulo delimitador acumulado

El *rectángulo delimitador acumulado* es el rectángulo más pequeño que incluye la parte de una ventana o área cliente afectada por las operaciones de dibujo recientes. Una aplicación puede usar este rectángulo para determinar de forma cómoda el alcance de los cambios causados por las operaciones de dibujo. A veces se usa junto con [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) para determinar qué parte del área de cliente se debe volver a dibujar una vez desactivado el bloqueo de actualización.

Una aplicación utiliza la función [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) (ESPECIFICAndo DCB \_ enable) para empezar a acumular el rectángulo delimitador. Posteriormente, el sistema acumula puntos para el rectángulo delimitador a medida que la aplicación utiliza el contexto de dispositivo de pantalla especificado. La aplicación puede recuperar el rectángulo delimitador actual en cualquier momento mediante la función [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) . La aplicación detiene la acumulación al llamar a **SetBoundsRect** de nuevo, especificando el valor de DCB \_ Disable.

 

 



