---
title: Establecer la seguridad para las aplicaciones COM
description: Establecer la seguridad para las aplicaciones COM
ms.assetid: 5b615007-e04b-41be-872c-20e0ea818ff1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8dd705015aaa2ca1965d07c556ff3d55aada00
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369612"
---
# <a name="setting-security-for-com-applications"></a>Establecer la seguridad para las aplicaciones COM

Hay varias maneras de ayudar a controlar la seguridad de las aplicaciones. Puede cambiar la configuración de seguridad predeterminada de un equipo, que usan todas las aplicaciones del equipo que no proporcionen sus propios valores de seguridad. Puede establecer la seguridad de un proceso determinado, ya sea mediante Dcomcnfg.exe o llamando a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). También puede controlar mediante programación la configuración de seguridad en el nivel de proxy de interfaz.

En los temas siguientes se proporcionan procedimientos que explican cómo establecer la seguridad:

-   [Modificar los valores predeterminados de seguridad para un equipo](modifying-the-security-defaults-for-a-computer.md)
-   [Configuración de Process-Wide seguridad](setting-processwide-security.md)
-   [Establecer la seguridad en el nivel de proxy de interfaz](setting-security-at-the-interface-proxy-level.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




