---
title: Modificación de los valores predeterminados de seguridad de un equipo
description: Modificación de los valores predeterminados de seguridad de un equipo
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418343"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a>Modificación de los valores predeterminados de seguridad de un equipo

No se recomienda cambiar la configuración de seguridad de todo el sistema, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente. Si va a cambiar la configuración de seguridad de todo el sistema para que afecte a la configuración de seguridad de una aplicación COM determinada, debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM en particular. Para obtener más información acerca de cómo establecer la seguridad de todo el proceso, consulte Configuración de la [seguridad de Process-Wide](setting-processwide-security.md).

Algunos valores del registro determinan la configuración de seguridad de las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Puede modificar esta configuración mediante Dcomcnfg.exe.

Para obtener más información, vea los temas siguientes:

-   [Valores del registro para la seguridad de System-Wide](registry-values-for-machine-wide-security.md)
-   [Establecer la seguridad de System-Wide mediante DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad de todo el proceso](setting-processwide-security.md)
</dt> <dt>

[Establecer la seguridad de las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




