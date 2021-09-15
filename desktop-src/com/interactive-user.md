---
title: Usuario interactivo
description: El usuario interactivo es el usuario que ha iniciado sesión actualmente en el equipo donde se ejecuta el servidor COM.
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7fc8aeb5fd9674c09b40f6c46e4e173f5965a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566325"
---
# <a name="interactive-user"></a>Usuario interactivo

El *usuario interactivo* es el usuario que ha iniciado sesión actualmente en el equipo donde se ejecuta el servidor COM. Si la identidad se establece para ser el usuario interactivo, todos los clientes usan la misma instancia del servidor si el servidor registra su generador de clases como multiuso. Si ningún usuario ha iniciado sesión, el servidor no se ejecutará. Si el servidor tiene una interfaz gráfica de usuario (GUI) que el cliente necesita ver, debe usar un usuario interactivo para la identidad del servidor. Sin embargo, elegir esta identidad conlleva algunos riesgos de seguridad porque el servidor se ejecuta bajo la identidad del usuario que ha iniciado sesión sin el conocimiento o consentimiento del usuario que ha iniciado sesión. Además, una aplicación de servicio no puede mostrar una interfaz de usuario. Para obtener más información, vea [Interactive Services](/windows/desktop/Services/interactive-services).

Si un servidor COM está configurado para ejecutarse como usuario interactivo, en un entorno de terminal Services, el servidor se inicia en la sesión interactiva que coincide con la identidad del usuario del cliente. Sin embargo, la aplicación cliente puede usar el moniker de sesión para hacer referencia a un objeto proporcionado por el servidor en una sesión que no coincide con la identidad del cliente. Cuando se usa, la aplicación cliente puede especificar cualquier sesión, en cuyo caso el servidor se ejecutará como el usuario propietario de la sesión, no como el usuario de inicio. Los permisos de acceso predeterminados en este escenario no permitirían al usuario de inicio llamar a métodos en el servidor. Sin embargo, los siguientes riesgos de seguridad permanecen:

-   Si el servidor COM expone interfaces que no están controladas por COM, como puertos TCP, canalizaciones con nombre, puertos LPC, secciones de memoria compartida, y así sucesivamente, el usuario de inicio podría usar estas interfaces para influir en el servidor. Los objetos COM configurados para ejecutarse como el usuario interactivo deben reducir esta superficie de ataque tanto como sea posible.
-   Los objetos COM pueden establecer sus propios permisos de acceso. Si el objeto establece permisos de acceso, ya sea en su registro de AppID o mediante una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), para permitir el acceso de usuario de inicio, el usuario podría iniciar el servidor para ejecutarse como otro usuario y, a continuación, acceder al objeto .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Identidad de aplicación](application-identity.md)
</dt> <dt>

[Iniciar usuario](launching-user.md)
</dt> <dt>

[Identidad de servicio](service-identity.md)
</dt> <dt>

[Usuario especificado](specified-user.md)
</dt> </dl>

 

 