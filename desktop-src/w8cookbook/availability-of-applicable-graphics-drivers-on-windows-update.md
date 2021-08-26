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
ms.openlocfilehash: 906894f317a86d851501e913e3c9491dc1f83336f7f80eefa660ee43d3510b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935435"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a>Disponibilidad de los controladores de gráficos aplicables en Windows Update

La disponibilidad de estos controladores en Windows Update (WU) determinará si a un usuario se le ofrece automáticamente una actualización de Windows 7, Windows 8 o Windows 8.1 a Windows 10. Si los exámenes de hardware mostraron que no había ningún controlador de gráficos disponible en Windows Update para el adaptador de gráficos en el equipo, no se ofrecía a los usuarios el sistema operativo Windows 10 actualizado. Sin embargo, los usuarios todavía pueden Windows 10 a través de otros orígenes y realizar manualmente la actualización.

Algunos usuarios no estaban seguros de por qué no se les ofrecía la actualización cuando había otras personas, aunque Asesor de actualizaciones explicó que no había ningún controlador gráfico disponible para su hardware.

Además, algunos usuarios forzaron una actualización y, a continuación, encontraron que su funcionalidad de gráficos y rendimiento se han visto obligados debido a la falta de un controlador de hardware.

## <a name="mitigations"></a>Mitigaciones

Para mitigar esto, los usuarios pueden instalar manualmente un controlador anterior, es decir, desde Windows 7, Windows 8 o Windows 8.1, yendo al sitio web de IHV o OEM y descargando un controlador explícitamente. Esto debe hacerse después de la actualización y no se garantiza que funcione. No hay ninguna solución compatible si un controlador de gráficos adecuado no está disponible en WU. El usuario debe decidir si:

-   Permanezca en el sistema operativo anterior;
-   Acepte las limitaciones del controlador de software, adaptador de pantalla básico de Microsoft (MSBDA); O
-   Compre una nueva tarjeta gráfica que tenga un controlador Windows 10 compatible.

## <a name="solutions"></a>Soluciones

Es fundamental que los OEM y los IHV carguen sus controladores de gráficos Windows 10 en WU para cualquier hardware que pretenden admitir.

Tenga en cuenta que es posible que el hardware que ha alcanzado el final de vida (EOL) no tenga controladores en WU. En este caso, no hay ninguna solución: el usuario debe elegir una de las opciones de Mitigaciones anteriores.

 

 




