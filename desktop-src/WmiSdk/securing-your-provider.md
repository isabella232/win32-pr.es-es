---
description: La escritura de un proveedor seguro requiere tener en cuenta cómo se hospeda el proveedor, cómo controla la suplantación y asegurarse de que se comprueban los derechos de acceso de los usuarios a los datos.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Protección del proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6b8fef1e90f09bc09488c058240b7fd1a88ebd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063909"
---
# <a name="securing-your-provider"></a>Protección del proveedor

La escritura de un proveedor seguro requiere tener en cuenta cómo se hospeda el proveedor, cómo controla la suplantación y asegurarse de que se comprueban los derechos de acceso de los usuarios a los datos. Puede proteger los datos en el espacio de nombres del proveedor exigiendo que se cifran los datos antes de enviarlos a través de una red. Para obtener más información, vea [Requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).

Si un usuario tiene acceso **DE \_** ESCRITURA COMPLETA en cualquier espacio de nombres, el usuario puede crear suscripciones entre espacios de nombres para los datos de un espacio de nombres en el que el usuario está restringido. Dado que un proveedor se puede cargar en cualquier espacio de nombres y ejecutarse en cualquier contexto de seguridad, el proveedor debe realizar sus propias comprobaciones de acceso para asegurarse de que solo los usuarios autorizados puedan acceder a los datos o ejecutar métodos. Para obtener más información, vea [Realizar comprobaciones de acceso.](performing-access-checks.md)

En los temas siguientes se describe la seguridad del proveedor:

-   [Hospedaje y seguridad del proveedor](provider-hosting-and-security.md)
-   [Realizar comprobaciones de acceso](performing-access-checks.md)
-   [Claves del Registro para controlar la seguridad del proveedor](registry-keys-for-controlling-provider-security-.md)
-   [Acceso a espacios de nombres WMI](access-to-wmi-namespaces.md)
-   [Suplantación de un cliente](impersonating-a-client.md)

En los temas siguientes se describe cómo interactúan los clientes y los scripts con la seguridad del proveedor:

-   [Establecer la autenticación en WMI](setting-authentication-in-wmi.md)
-   [Conexión entre diferentes sistemas operativos](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [Establecer el nivel de seguridad de proceso predeterminado mediante VBScript](setting-the-default-process-security-level-using-vbscript.md)
-   [Establecer la seguridad del proceso de la aplicación cliente](setting-client-application-process-security.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mantener la seguridad de WMI](maintaining-wmi-security.md)
</dt> <dt>

[Uso de WMI](using-wmi.md)
</dt> </dl>

 

 
