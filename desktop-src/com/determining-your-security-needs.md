---
title: Determinación de las necesidades de seguridad
description: La forma de configurar la seguridad COM para la aplicación depende del tipo de seguridad que necesite la aplicación. Hay varias situaciones comunes que determinan lo que debe hacer.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cacef6d4e3aab59cb3b603125c36dd17d07846
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779969"
---
# <a name="determining-your-security-needs"></a>Determinación de las necesidades de seguridad

La forma de configurar la seguridad COM para la aplicación depende del tipo de seguridad que necesite la aplicación. Hay varias situaciones comunes que determinan lo que debe hacer.

Si decide usar los valores predeterminados de seguridad COM, no tiene que hacer anythingâ "COM lo controla todo. Para obtener información sobre cuál es la configuración predeterminada, vea [valores predeterminados de seguridad com](com-security-defaults.md).

También puede evitar las llamadas remotas en el equipo deshabilitando DCOM por completo (COM entre equipos remotos). Para obtener más información, vea [establecer la seguridad de System-Wide mediante DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

En el caso de las aplicaciones heredadas o nuevas, puede establecer la seguridad de todo el proceso en el registro. Para obtener más información, consulte [configuración de la seguridad de Processwide a través del registro](setting-processwide-security-through-the-registry.md).

También puede invalidar la configuración de seguridad predeterminada para las llamadas a determinadas interfaces en el proceso mientras establece la seguridad predeterminada para el resto del proceso (para permitir que COM controle los casos generales). Para obtener más información, consulte [configuración de la seguridad en el nivel de proxy de interfaz](setting-security-at-the-interface-proxy-level.md).

En cuanto a los requisitos de seguridad complejos, puede administrar toda la seguridad mediante programación en lugar de permitir que COM lo controle. Para ello, llame a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para deshabilitar la autenticación automática y, a continuación, controle toda la configuración de seguridad mediante el establecimiento de la seguridad en una base de proxy por interfaz. Para obtener más información, consulte Configuración de la [seguridad de Processwide con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) y [configuración de la seguridad en el nivel de proxy de interfaz](setting-security-at-the-interface-proxy-level.md).

En algunos escenarios, puede que desee desactivar la seguridad por completo. Podría decidir que la aplicación no necesita ninguna seguridad o que desee deshabilitar la seguridad durante el tiempo de desarrollo para que pueda habilitar las características de seguridad de forma individual. Para obtener información sobre cómo deshabilitar la seguridad de COM, consulte desactivación de la [seguridad](turning-off-security.md).

La seguridad en COM se basa en los servicios de autenticación administrados por paquetes de seguridad. NTLMSSP funciona bien con muchas aplicaciones, pero no proporciona la seguridad más sólida que ofrecen otros paquetes. Por lo tanto, COM admite el paquete de seguridad Schannel y el protocolo de seguridad Kerberos V5. Para obtener más información sobre el uso de estos paquetes de seguridad, consulte [com y paquetes de seguridad](com-and-security-packages.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




