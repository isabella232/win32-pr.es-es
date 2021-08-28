---
description: El rectángulo delimitador acumulado es el rectángulo más pequeño que incluye la parte de una ventana o área de cliente afectada por las operaciones de dibujo recientes.
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: Rectángulo delimitador acumulado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d90b2f92b50dbaede477c0a712be970bf0af46b25c5e5edd956fe428d46559
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779355"
---
# <a name="accumulated-bounding-rectangle"></a>Rectángulo delimitador acumulado

El *rectángulo delimitador acumulado es* el rectángulo más pequeño que incluye la parte de una ventana o área de cliente afectada por las operaciones de dibujo recientes. Una aplicación puede usar este rectángulo para determinar cómodamente la extensión de los cambios causados por las operaciones de dibujo. A veces se usa junto con [**LockWindowUpdate para**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) determinar qué parte del área de cliente se debe volver a dibujar después de borrar el bloqueo de actualización.

Una aplicación usa la [**función SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) (especificando DCB ENABLE) para empezar \_ a acumular el rectángulo delimitador. Posteriormente, el sistema acumula puntos para el rectángulo delimitador a medida que la aplicación usa el contexto de dispositivo para mostrar especificado. La aplicación puede recuperar el rectángulo delimitador actual en cualquier momento mediante la [**función GetBoundsRect.**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) La aplicación detiene la acumulación llamando de nuevo **a SetBoundsRect,** especificando el valor DISABLE \_ de DCB.

 

 



