---
title: Disponibilidad de los controladores de gráficos aplicables en Windows Update
description: La disponibilidad de estos controladores en Windows Update (WU) determinará si a un usuario se le ofrece automáticamente una actualización de Windows 7, Windows 8 o Windows 8.1 a Windows 10.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 208e984199c8de63dfa49133a255865035c84bdd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695292"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a>Disponibilidad de los controladores de gráficos aplicables en Windows Update

La disponibilidad de estos controladores en Windows Update (WU) determinará si a un usuario se le ofrece automáticamente una actualización de Windows 7, Windows 8 o Windows 8.1 a Windows 10. Si los análisis de hardware mostraron que no había ningún controlador de gráficos disponible en Windows Update para el adaptador de gráficos del equipo, no se ofrecía al usuario el sistema operativo Windows 10 actualizado. Sin embargo, los usuarios todavía pueden obtener Windows 10 a través de otros orígenes y realizar la actualización manualmente.

Algunos usuarios no estaban seguros de por qué no se les ofrecía la actualización cuando otras personas, aunque el asesor de actualizaciones explicó que no había ningún controlador de gráficos disponible para su hardware.

Además, algunos usuarios forzaban una actualización y, a continuación, detectaban que la funcionalidad de gráficos y el rendimiento sufrieron debido a la falta de un controlador de hardware.

## <a name="mitigations"></a>Mitigaciones

Para mitigar esto, los usuarios pueden instalar manualmente un controlador anterior, es decir, desde Windows 7, Windows 8 o Windows 8.1, yendo al sitio web de IHV o OEM y descargando un controlador explícitamente. Esto debe hacerse después de la actualización y no se garantiza que funcione. No hay ninguna solución compatible Si un controlador de gráficos adecuado no está disponible en WU. El usuario debe decidir si:

-   Permanecer en el sistema operativo anterior;
-   Acepte las limitaciones del controlador de software, el adaptador de pantalla básico de Microsoft (MSBDA). de
-   Compre una nueva tarjeta gráfica que tenga un controlador compatible con Windows 10.

## <a name="solutions"></a>Soluciones

Es fundamental que los fabricantes de equipos originales (IHV) carguen sus controladores de gráficos de Windows 10 en WU para cualquier hardware que pretendan admitir.

Tenga en cuenta que el hardware que ha alcanzado el final de la vida (EOL) podría no tener controladores en WU. En este caso, no hay ninguna solución: el usuario debe elegir una de las opciones de mitigaciones anteriores.

 

 




