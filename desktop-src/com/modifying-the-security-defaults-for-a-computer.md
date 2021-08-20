---
title: Modificar los valores predeterminados de seguridad para un equipo
description: Modificar los valores predeterminados de seguridad para un equipo
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7936e2d0bc1113b651fd40f94e84037f00f4ffbe12b7e0232f1dc6a6cd8aaeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118105403"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a>Modificar los valores predeterminados de seguridad para un equipo

No se recomienda cambiar la configuración de seguridad de todo el sistema, ya que afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente. Si va a cambiar la configuración de seguridad de todo el sistema para que afecte a la configuración de seguridad de una aplicación COM determinada, en su lugar debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM concreta. Para obtener más información sobre cómo establecer la seguridad de todo el proceso, vea [Setting Process-Wide Security](setting-processwide-security.md).

Determinados valores del Registro determinan la configuración de seguridad de las aplicaciones que no llaman a [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) Puede modificar esta configuración mediante Dcomcnfg.exe.

Para obtener más información, vea los temas siguientes:

-   [Valores del Registro para System-Wide Seguridad](registry-values-for-machine-wide-security.md)
-   [Establecer System-Wide seguridad mediante DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad en todo el proceso](setting-processwide-security.md)
</dt> <dt>

[Establecer la seguridad para las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




