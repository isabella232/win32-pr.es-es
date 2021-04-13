---
description: La biblioteca de administración de MTS incluida con las interfaces de administración de COM+ proporciona compatibilidad con versiones anteriores de la biblioteca de administración de MTS 2,0.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: Biblioteca de administración de MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e4be3cdad6b5b5f4e45c32261a7f94845839ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538806"
---
# <a name="mts-administration-library"></a>Biblioteca de administración de MTS

La biblioteca de administración de MTS incluida con las interfaces de administración de COM+ proporciona compatibilidad con versiones anteriores de la biblioteca de administración de MTS 2,0. La mayoría del código de administración de MTS 2,0 existente seguirá funcionando con la biblioteca MTSAdmin que se proporciona. sin embargo, algunas funciones han cambiado.

Para aprovechar las ventajas de la nueva funcionalidad o si está escribiendo código de administración por primera vez, debe usar la biblioteca COMAdmin.

Los siguientes elementos de la biblioteca de administración de MTS actual se han modificado desde la biblioteca de administración de MTS 2,0:

-   La interfaz **IRemoteComponentUtil** ya no está disponible.
-   La colección **RemoteComponents** ya no está disponible.
-   La propiedad RoleID ya no está disponible, ya que el nombre de rol se usa como clave para este.
-   El método **ExportPackage** ya no exporta un client.exe.
-   La propiedad RemoteComponentInstallPath ya no se expone en la colección [**LocalComputer**](localcomputer.md) .
-   La propiedad ApplicationInstallPath ya no se expondrá en la colección [**LocalComputer**](localcomputer.md) .
-   El paquete del sistema se llama ahora aplicación del sistema.
-   El paquete de utilidades se llama ahora utilidades COM+.
-   La propiedad IsSystem existe en la colección de [**componentes**](components.md) de MTSAdmin, pero devolverá "NotImpl" cuando esté activada y no se guardará si se establece.
-   La colección de [**componentes**](components.md) ya no admite la propiedad packagename. Para averiguar el nombre del paquete, ahora necesitará obtener el PackageID y, a continuación, buscar el paquete coincidente en la colección de paquetes.
-   Las siguientes propiedades ya no existen en la colección [**InterfacesForComponent**](interfacesforcomponent.md) :
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

[Resultados y problemas de la conversión de COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversión manual desde MTS](manual-conversion-from-mts.md)
</dt> </dl>

 

 



