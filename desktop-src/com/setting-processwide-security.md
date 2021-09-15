---
title: Configuración de Process-Wide seguridad
description: Hay varias maneras de establecer la seguridad en todo el proceso.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466107"
---
# <a name="setting-process-wide-security"></a>Configuración de Process-Wide seguridad

Hay varias maneras de establecer la seguridad en todo el proceso. La primera, mediante la herramienta Dcomcnfg.exe, es más fácil porque no requiere programación. La segunda técnica ofrece al programador más control y requiere una llamada a [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) Otra técnica consiste en establecer la seguridad de todo el proceso en el Registro mediante la [clave AppID.](appid-key.md)

Para obtener más información sobre estas técnicas, vea los temas siguientes:

-   [Establecer Process-Wide seguridad mediante DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)
-   [Establecer Process-Wide seguridad con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md)
-   [Establecer Process-Wide seguridad mediante el Registro](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad en el nivel de proxy de interfaz](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[Establecer la seguridad para las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




