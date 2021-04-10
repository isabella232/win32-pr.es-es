---
title: Valores del registro para la seguridad de System-Wide
description: Valores del registro para la seguridad de System-Wide
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994089"
---
# <a name="registry-values-for-system-wide-security"></a>Valores del registro para la seguridad de System-Wide

No se recomienda cambiar la configuración de seguridad de todo el sistema, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente. Si va a cambiar la configuración de seguridad de todo el sistema para que afecte a la configuración de seguridad de una aplicación COM determinada, debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM en particular. Para obtener más información acerca de cómo establecer la seguridad de todo el proceso, consulte Configuración de la [seguridad de Process-Wide](setting-processwide-security.md).

Ciertos valores del registro se usan para determinar la configuración de seguridad de las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Puede usar Dcomcnfg.exe para modificar estos valores de seguridad predeterminados para un equipo. Para conocer los procedimientos paso a paso que describen cómo usar Dcomcnfg.exe con este fin, vea [establecer la seguridad de System-Wide mediante DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

Otra manera de cambiar la configuración predeterminada para todo el sistema es manipular los valores del registro directamente. Sin embargo, solo los administradores y el sistema tienen acceso total a la parte del registro que contiene la configuración predeterminada de seguridad de llamadas en todo el sistema. Todos los demás usuarios tienen solo acceso de lectura.

Los valores con nombre que afectan a los valores predeterminados de seguridad del sistema son los siguientes:

-   [DefaultLaunchPermission](defaultlaunchpermission.md)
-   [DefaultAccessPermission](defaultaccesspermission.md)
-   [LegacyAuthenticationLevel](legacyauthenticationlevel.md)
-   [LegacyImpersonationLevel](legacyimpersonationlevel.md)
-   [LegacySecureReferences](legacysecurereferences.md)
-   [SRPRunningObjectChecks](srprunningobjectchecks.md)
-   [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la seguridad de Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 




