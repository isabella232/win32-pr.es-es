---
title: Configuración de la seguridad de Process-Wide
description: Hay varias maneras de establecer la seguridad de todo el proceso.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714269"
---
# <a name="setting-process-wide-security"></a>Configuración de la seguridad de Process-Wide

Hay varias maneras de establecer la seguridad de todo el proceso. La primera forma de usar la herramienta Dcomcnfg.exe es que es más fácil porque no requiere programación. La segunda técnica ofrece al programador más control y requiere una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Otra técnica consiste en establecer la seguridad de todo el proceso en el registro mediante el uso de la clave [AppID](appid-key.md) .

Para obtener más información sobre estas técnicas, vea los temas siguientes:

-   [Establecer la seguridad de Process-Wide mediante DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)
-   [Configuración de la seguridad de Process-Wide con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md)
-   [Establecer la seguridad de Process-Wide a través del registro](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecimiento de la seguridad en el nivel de proxy de interfaz](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[Establecer la seguridad de las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




