---
title: Seguridad de activación
description: Seguridad de activación
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5b01b918666e911d96ed16528ba5045103f445
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488366"
---
# <a name="activation-security"></a>Seguridad de activación

La seguridad de activación (también denominada seguridad de inicio) ayuda a controlar quién puede iniciar un servidor. El administrador de control de servicios (SCM) de un equipo determinado aplica automáticamente la seguridad de activación. Tras recibir una solicitud de un cliente para activar un objeto (tal y como se describe en [funciones auxiliares de creación de instancias](instance-creation-helper-functions.md)), el SCM comprueba la solicitud con la información de seguridad de activación almacenada en el registro. (La seguridad de activación también se comprueba para las activaciones del mismo equipo).

Al determinar la identidad del cliente, la activación examina la marca de Cloaking establecida en la llamada del cliente a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Si se establece la marca de Cloaking (para Cloaking dinámico o estático), se utiliza el token de subproceso, si está presente, para determinar la identidad del cliente. Si no se establece ningún Cloaking, se utiliza el token de proceso en lugar del token de subproceso.

Para obtener más información sobre la seguridad de activación, consulte [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) y [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 