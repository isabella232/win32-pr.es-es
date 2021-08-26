---
title: Determinar las necesidades de seguridad
description: La configuración de la seguridad COM para la aplicación depende del tipo de seguridad que necesite la aplicación. Hay varias situaciones comunes que determinan lo que debe hacer.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57ccbbc8fc96b7c94e90fd3925dfb2ffff07225c34ebe1da34353f42b08b3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993235"
---
# <a name="determining-your-security-needs"></a>Determinar las necesidades de seguridad

La configuración de la seguridad COM para la aplicación depende del tipo de seguridad que necesite la aplicación. Hay varias situaciones comunes que determinan lo que debe hacer.

Si decide usar los valores predeterminados de seguridad COM, no tiene que hacer nada: COM lo controla todo. Para obtener información sobre cuáles son estas configuraciones [predeterminadas,](com-security-defaults.md)vea Valores predeterminados de seguridad COM.

También puede evitar las llamadas remotas a la máquina si deshabilita DCOM por completo (COM entre equipos remotos). Para obtener más información, vea [Establecer System-Wide seguridad mediante DCOMCNFG.](setting-machine-wide-security-using-dcomcnfg.md)

En el caso de las aplicaciones heredadas o nuevas, puede establecer la seguridad de todo el proceso en el Registro. Para obtener más información, vea [Establecer la seguridad de todo el proceso a través del Registro](setting-processwide-security-through-the-registry.md).

También puede invalidar la configuración de seguridad predeterminada para las llamadas a determinadas interfaces del proceso al establecer la seguridad predeterminada para el resto del proceso (para permitir que COM controle los casos generales). Para obtener más información, vea [Establecer la seguridad en el nivel de proxy de interfaz](setting-security-at-the-interface-proxy-level.md).

Para requisitos de seguridad complejos, puede controlar toda la seguridad mediante programación en lugar de permitir que COM la controle por usted. Para ello, llame a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para deshabilitar la autenticación automática y, a continuación, controle toda la configuración de seguridad estableciendo la seguridad en función del proxy por interfaz. Para obtener más información, vea [Establecer la seguridad de todo el proceso con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) y Establecer la seguridad en el nivel de proxy de [interfaz](setting-security-at-the-interface-proxy-level.md).

En algunos escenarios, es posible que quiera desactivar completamente la seguridad. Puede decidir que la aplicación no necesita ninguna seguridad o puede deshabilitar la seguridad durante el tiempo de desarrollo para que pueda habilitar las características de seguridad individualmente. Para obtener información sobre cómo deshabilitar la seguridad COM, vea [Desactivar la seguridad](turning-off-security.md).

La seguridad en COM se basa en los servicios de autenticación administrados por paquetes de seguridad. NTLMSSP funciona bien para muchas aplicaciones, pero no proporciona la seguridad más sólida que ofrecen otros paquetes. Por lo tanto, COM admite el paquete de seguridad de Schannel y el protocolo de seguridad Kerberos v5. Para obtener más información sobre el uso de estos paquetes de seguridad, [vea COM y Paquetes de seguridad.](com-and-security-packages.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




