---
title: Seguridad de activación
description: Seguridad de activación
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5b01b918666e911d96ed16528ba5045103f445
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060961"
---
# <a name="activation-security"></a>Seguridad de activación

La seguridad de activación (también denominada seguridad de inicio) ayuda a controlar quién puede iniciar un servidor. El administrador de control de servicios (SCM) de un equipo determinado aplica automáticamente la seguridad de activación. Tras recibir una solicitud de un cliente para activar un objeto (como se describe en Funciones auxiliares de creación de [instancias),](instance-creation-helper-functions.md)el SCM comprueba la solicitud con la información de seguridad de activación almacenada en su registro. (La seguridad de activación también se comprueba para las activaciones en el mismo equipo).

Al determinar la identidad del cliente, la activación examina la marca de ocultación establecida en la llamada del cliente a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Si se establece la marca de protección (para el arroba dinámico o estático), se usa el token de subproceso, si está presente, para determinar la identidad del cliente. Si no se establece ningún ajuste, se usa el token de proceso en lugar del token de subproceso.

Para obtener más información sobre la seguridad de activación, [**vea COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) y [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 