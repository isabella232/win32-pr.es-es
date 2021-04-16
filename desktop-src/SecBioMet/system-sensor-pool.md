---
title: Grupo de sensores del sistema
description: Colección de unidades biométricas que se puede compartir y que proporcionan acceso a los servicios de autenticación de Windows. Winlogon, UAC y cualquier otro cliente que asocia un SID con una plantilla biométrica específica usan este grupo.
ms.assetid: 308306a9-e12c-4ff6-92c3-a36667a5e548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ae9487b91b57b2e9568817c92e44b4b7197f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685546"
---
# <a name="system-sensor-pool"></a>Grupo de sensores del sistema

El grupo de sensores del sistema es una colección de unidades biométricas que se puede compartir y que proporcionan acceso a los servicios de autenticación de Windows. Winlogon, UAC y cualquier otro cliente que asocia un SID con una plantilla biométrica específica usan este grupo. Unidades biométricas en el grupo de sistemas:

-   Se puede compartir entre varias aplicaciones cliente.
-   Envíe avisos de eventos generados por la finalización de las operaciones biométricas únicamente a la aplicación que tenga el foco de ventana actual.
-   Usar SID de cuenta para representar las identidades de plantilla. Todas las plantillas asociadas con una cuenta de usuario individual se etiquetan con el SID asignado a esa cuenta.
-   Dependen del almacenamiento de plantilla de confianza que proporciona el servicio biométrico de Windows.

Se puede incluir una unidad biométrica en el grupo de sistema si puede ser:

-   Está configurado para funcionar en modo básico y actuar solo como un dispositivo de captura biométrica.
-   Está configurado para funcionar en modo avanzado pero no tiene almacenamiento de plantilla incorporado. Es decir, debe utilizar el adaptador de almacenamiento y el almacén de plantillas suministrados por Microsoft.
-   Configurado para funcionar en modo avanzado, contiene el almacenamiento de plantilla incorporado y puede generar los hash necesarios.

Cuando se conecta un nuevo dispositivo de sensor, el servicio biométrico de Windows crea una unidad biométrica para él e intenta configurar esa unidad para que la use el grupo de sensores del sistema. Si la configuración no es correcta, la unidad biométrica se coloca en el grupo de sensores sin asignar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grupo de sensores privados](private-sensor-pool.md)
</dt> <dt>

[Grupos de sensores](sensor-pools.md)
</dt> <dt>

[Comportamiento del grupo de sistemas](system-pool-behavior.md)
</dt> </dl>

 

 




