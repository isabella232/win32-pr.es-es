---
title: Valores del Registro para System-Wide seguridad
description: Valores del Registro para System-Wide seguridad
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060894"
---
# <a name="registry-values-for-system-wide-security"></a>Valores del Registro para System-Wide seguridad

No se recomienda cambiar la configuración de seguridad de todo el sistema, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podría impedir que funcionen correctamente. Si va a cambiar la configuración de seguridad de todo el sistema para que afecte a la configuración de seguridad de una aplicación COM determinada, en su lugar debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM concreta. Para obtener más información sobre cómo establecer la seguridad de todo el proceso, vea [Setting Process-Wide Security](setting-processwide-security.md).

Ciertos valores del Registro se usan para determinar la configuración de seguridad de las aplicaciones que no llaman [**a CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) Puede usar Dcomcnfg.exe para modificar esta configuración de seguridad predeterminada para un equipo. Para obtener procedimientos paso a paso que describen cómo usar Dcomcnfg.exe para este propósito, vea Establecer la seguridad System-Wide con [DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

Otra manera de cambiar la configuración predeterminada de todo el sistema es manipular los valores del Registro directamente. Sin embargo, solo los administradores y el sistema tienen acceso total a la parte del registro que contiene la configuración de seguridad de llamadas predeterminada para todo el sistema. Todos los demás usuarios solo tienen acceso de lectura.

Los valores con nombre que afectan a los valores predeterminados de seguridad de todo el sistema son los siguientes:

-   [DefaultLaunchPermission](defaultlaunchpermission.md)
-   [DefaultAccessPermission](defaultaccesspermission.md)
-   [LegacyAuthenticationLevel](legacyauthenticationlevel.md)
-   [LegacyImpersonationLevel](legacyimpersonationlevel.md)
-   [LegacySecureReferences](legacysecurereferences.md)
-   [SRPRunningObjectChecks](srprunningobjectchecks.md)
-   [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de Process-Wide seguridad](setting-processwide-security.md)
</dt> </dl>

 

 




