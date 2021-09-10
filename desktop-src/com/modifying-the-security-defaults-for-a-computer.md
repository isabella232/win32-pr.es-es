---
title: Modificar los valores predeterminados de seguridad para un equipo
description: Modificar los valores predeterminados de seguridad para un equipo
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369616"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a>Modificar los valores predeterminados de seguridad para un equipo

No se recomienda cambiar la configuración de seguridad de todo el sistema, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podría impedir que funcionen correctamente. Si va a cambiar la configuración de seguridad de todo el sistema para que afecte a la configuración de seguridad de una aplicación COM determinada, en su lugar debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM concreta. Para obtener más información sobre cómo establecer la seguridad de todo el proceso, vea [Setting Process-Wide Security](setting-processwide-security.md).

Determinados valores del Registro determinan la configuración de seguridad de las aplicaciones que no llaman [**a CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) Puede modificar esta configuración mediante Dcomcnfg.exe.

Para obtener más información, vea los temas siguientes:

-   [Valores del Registro para System-Wide seguridad](registry-values-for-machine-wide-security.md)
-   [Configuración System-Wide seguridad mediante DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad de todo el proceso](setting-processwide-security.md)
</dt> <dt>

[Configuración de la seguridad para aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




