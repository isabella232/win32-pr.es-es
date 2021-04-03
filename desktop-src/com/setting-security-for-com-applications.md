---
title: Establecer la seguridad de las aplicaciones COM
description: Establecer la seguridad de las aplicaciones COM
ms.assetid: 5b615007-e04b-41be-872c-20e0ea818ff1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8dd705015aaa2ca1965d07c556ff3d55aada00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903911"
---
# <a name="setting-security-for-com-applications"></a>Establecer la seguridad de las aplicaciones COM

Hay varias maneras de ayudar a controlar la seguridad de las aplicaciones. Puede cambiar la configuración de seguridad predeterminada de un equipo, que son utilizadas por todas las aplicaciones del equipo que no proporcionan sus propios valores de seguridad. Puede establecer la seguridad de un proceso determinado, ya sea mediante Dcomcnfg.exe o mediante una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). También puede controlar mediante programación la configuración de seguridad en el nivel de proxy de interfaz.

En los temas siguientes se proporcionan procedimientos que explican cómo establecer la seguridad:

-   [Modificación de los valores predeterminados de seguridad de un equipo](modifying-the-security-defaults-for-a-computer.md)
-   [Configuración de la seguridad de Process-Wide](setting-processwide-security.md)
-   [Establecimiento de la seguridad en el nivel de proxy de interfaz](setting-security-at-the-interface-proxy-level.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




