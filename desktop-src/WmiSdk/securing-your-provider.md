---
description: Para escribir un proveedor seguro es necesario tener en cuenta cómo se hospeda el proveedor, cómo el proveedor controla la suplantación y cómo asegurarse de que los usuarios tienen los derechos de acceso a los datos.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Protección del proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6b8fef1e90f09bc09488c058240b7fd1a88ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706082"
---
# <a name="securing-your-provider"></a>Protección del proveedor

Para escribir un proveedor seguro es necesario tener en cuenta cómo se hospeda el proveedor, cómo el proveedor controla la suplantación y cómo asegurarse de que los usuarios tienen los derechos de acceso a los datos. Puede proteger los datos en el espacio de nombres del proveedor requiriendo que los datos se cifren antes de enviarlos a través de una red. Para obtener más información, vea [requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).

Si un usuario tiene acceso de **\_ escritura completo** en cualquier espacio de nombres, el usuario puede crear suscripciones entre espacios de nombres para los datos de un espacio de nombres en el que el usuario está restringido. Dado que un proveedor se puede cargar en cualquier espacio de nombres y ejecutarse en cualquier contexto de seguridad, el proveedor debe realizar sus propias comprobaciones de acceso para asegurarse de que solo los usuarios autorizados tienen permiso de acceso a los datos o para ejecutar métodos. Para obtener más información, vea [realizar comprobaciones de acceso](performing-access-checks.md).

En los temas siguientes se describe la seguridad del proveedor:

-   [Hospedaje y seguridad de proveedores](provider-hosting-and-security.md)
-   [Realización de comprobaciones de acceso](performing-access-checks.md)
-   [Claves del registro para controlar la seguridad del proveedor](registry-keys-for-controlling-provider-security-.md)
-   [Acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md)
-   [Suplantar a un cliente](impersonating-a-client.md)

En los temas siguientes se describe cómo interactúan los clientes y scripts con la seguridad del proveedor:

-   [Configuración de la autenticación en WMI](setting-authentication-in-wmi.md)
-   [Conexión entre distintos sistemas operativos](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [Establecer el nivel de seguridad de proceso predeterminado mediante VBScript](setting-the-default-process-security-level-using-vbscript.md)
-   [Establecer la seguridad del proceso de la aplicación cliente](setting-client-application-process-security.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mantenimiento de la seguridad de WMI](maintaining-wmi-security.md)
</dt> <dt>

[Usar WMI](using-wmi.md)
</dt> </dl>

 

 
