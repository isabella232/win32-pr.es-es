---
description: La biblioteca de administración de MTS que se incluye con las interfaces de administración de COM+ proporciona compatibilidad con versiones anteriores con la biblioteca de administración de MTS 2.0.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: Biblioteca de administración de MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e449e99ef675f7f8ce893a358806926cd3d1a63ed13e5cc9fff01b97d0742d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306163"
---
# <a name="mts-administration-library"></a>Biblioteca de administración de MTS

La biblioteca de administración de MTS que se incluye con las interfaces de administración de COM+ proporciona compatibilidad con versiones anteriores con la biblioteca de administración de MTS 2.0. La mayoría del código de administración de MTS 2.0 existente seguirá funcionando con la biblioteca MTSAdmin que se proporciona; sin embargo, algunas funcionalidades han cambiado.

Para aprovechar las ventajas de la nueva funcionalidad o si escribe código de administración por primera vez, debe usar la biblioteca COMAdmin.

Los siguientes elementos de la biblioteca de administración de MTS actual se cambian de la biblioteca de administración de MTS 2.0:

-   La **interfaz IRemoteComponentUtil** ya no está disponible.
-   La **colección RemoteComponents** ya no está disponible.
-   La propiedad RoleID ya no está disponible, el nombre de rol ahora se usa como clave para esto.
-   El **método ExportPackage** ya no exporta un client.exe.
-   La propiedad RemoteComponentInstallPath ya no se expone en la [**colección LocalComputer.**](localcomputer.md)
-   La propiedad ApplicationInstallPath ya no se expone en la [**colección LocalComputer.**](localcomputer.md)
-   El paquete del sistema ahora se denomina Aplicación del sistema.
-   El paquete Utilities ahora se denomina UTILIDADES COM+.
-   La propiedad IsSystem existe en la colección [**Components**](components.md) de MTSAdmin, pero devolverá "NotImpl" cuando esté activada y no se guardará si se establece.
-   La colección [**Components**](components.md) ya no admite la propiedad PackageName. Para averiguar el nombre del paquete, ahora deberá obtener packageID y, a continuación, buscar el paquete correspondiente en la colección Packages.
-   Las siguientes propiedades ya no existen en la [**colección InterfacesForComponent:**](interfacesforcomponent.md)
    -   **ProxyCLSID**
    -   **ProxyDLL**
    -   **ProxyThreadingModel**
    -   **TypeLibFile**
    -   **TypeLibID**
    -   **TypeLibLangID**
    -   **TypeLibPlatform**
    -   **TypeLibVersion**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conversión automática desde MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Resultados y problemas de conversión de COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversión manual desde MTS](manual-conversion-from-mts.md)
</dt> </dl>

 

 



