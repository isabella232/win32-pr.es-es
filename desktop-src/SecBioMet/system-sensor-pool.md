---
title: Grupo de sensores del sistema
description: Colección de unidades biométricas que se pueden compartir que proporcionan acceso a Windows servicios de autenticación. Winlogon, UAC y cualquier otro cliente que asocie un SID a una plantilla biométrica específica usan este grupo.
ms.assetid: 308306a9-e12c-4ff6-92c3-a36667a5e548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ae9487b91b57b2e9568817c92e44b4b7197f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071182"
---
# <a name="system-sensor-pool"></a>Grupo de sensores del sistema

El grupo de sensores del sistema es una colección de unidades biométricas compartibles que proporcionan acceso a Windows servicios de autenticación. Winlogon, UAC y cualquier otro cliente que asocie un SID a una plantilla biométrica específica usan este grupo. Unidades biométricas en el grupo del sistema:

-   Varias aplicaciones cliente pueden compartir.
-   Envíe los avisos de eventos generados por la finalización de operaciones biométricas solo a la aplicación que tenga el foco de ventana actual.
-   Use sids de cuenta para representar las identidades de plantilla. Todas las plantillas asociadas a una sola cuenta de usuario se etiquetan con el SID asignado a esa cuenta.
-   Dependa del almacenamiento de plantillas de confianza proporcionado por Windows Biometric Service.

Se puede incluir una unidad biométrica en el grupo del sistema si puede ser:

-   Configurado para funcionar en modo básico y actuar solo como un dispositivo de captura biométrica.
-   Está configurado para funcionar en modo avanzado, pero no tiene almacenamiento de plantillas incorporado. Es decir, debe usar el adaptador de almacenamiento y el almacén de plantillas proporcionados por Microsoft.
-   Configurado para funcionar en modo avanzado, contiene almacenamiento de plantillas incorporado y puede generar los hashes necesarios.

Cuando se conecta un nuevo dispositivo de sensor, Windows Biometric Service crea una unidad biométrica para él e intenta configurar esa unidad para que la use el grupo de sensores del sistema. Si la configuración no se realiza correctamente, la unidad biométrica se coloca en el grupo de sensores sin signo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grupo de sensores privados](private-sensor-pool.md)
</dt> <dt>

[Grupos de sensores](sensor-pools.md)
</dt> <dt>

[Comportamiento del grupo de sistemas](system-pool-behavior.md)
</dt> </dl>

 

 




