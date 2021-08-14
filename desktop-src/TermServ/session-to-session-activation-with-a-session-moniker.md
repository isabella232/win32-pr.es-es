---
title: Activación de sesión a sesión con un moniker de sesión
description: La activación de sesión a sesión (también denominada activación entre sesiones) permite que un proceso de cliente inicie (active) un proceso de servidor local en una sesión especificada.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213627facdd2dee9e4ba7cc698d2be5455424b4394d295448a07aeb52788dd42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988135"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a>Activación de sesión a sesión con un moniker de sesión

La activación de sesión a sesión (también denominada activación entre sesiones) permite que un proceso de cliente inicie (active) un proceso de servidor local en una sesión especificada. Esta característica está disponible para las aplicaciones configuradas para ejecutarse en el contexto de seguridad del usuario interactivo, también conocido como modo de activación de objetos "RunAs Interactive User". Para obtener más información sobre los contextos de seguridad, vea [Contexto de seguridad del cliente.](/windows/desktop/SecAuthZ/the-client-security-context)

COM distribuido (DCOM) habilita la activación de objetos por sesión mediante un [Moniker](session-monikers.md)de sesión proporcionado por el sistema . Otros monikers proporcionados por el sistema incluyen [monikers](../com/file-monikers.md)de archivo, monikers de elementos, [monikers](../com/composite-monikers.md)compuestos genéricos, [anti monikers,](../com/anti-monikers.md) [puntero monikers](../com/pointer-monikers.md)y [monikers](../com/item-monikers.md)de [url.](../com/url-monikers.md)

Para poder usar el moniker de sesión, la aplicación DCOM debe establecerse para ejecutarse como el usuario interactivo. Esto se puede establecer mediante la herramienta Administración de servicios de componentes,  viendo las propiedades de la aplicación DCOM y seleccionando El usuario interactivo en la **pestaña Identidad.** Para obtener más información sobre los posibles riesgos de seguridad asociados con la configuración de una aplicación DCOM para que se ejecute como usuario interactivo en un entorno de Servicios de Escritorio remoto, consulte la sección "Identidad de aplicación (COM)" de la documentación de COM en Platform Software Development Kit (SDK).

Si se selecciona cualquier otro tipo de usuario para ejecutar la aplicación, la aplicación omitirá el moniker de sesión. Las aplicaciones de servidor COM+ también omiten el moniker de sesión. Para obtener más información sobre otros métodos para seleccionar el tipo de usuario para ejecutar la aplicación, consulte la documentación de COM en platform SDK.

Para crear un moniker de sesión, debe crear el identificador de sesión de la sesión Servicios de Escritorio remoto con un moniker de clase que especifique el identificador de clase del servidor de procesos.

**Para crear un moniker de sesión**

1.  Antefique el nombre para mostrar del moniker de clase con el nombre para mostrar del moniker de sesión mediante la sintaxis siguiente:

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    donde *digits* representa el identificador de sesión de la sesión en la que se va a iniciar el proceso de servidor y donde *el* identificador de clase representa el identificador de clase del servidor. Tenga en cuenta que el identificador de sesión es un número de base 10.

    En el caso de los equipos que ejecutan Windows XP o posterior, el uso de la sintaxis siguiente hará que COM envíe la activación a la sesión de consola física actualmente activa, sea cual sea su identificador de sesión:

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  Después de crear el moniker de sesión, puede pasar el resultado a la función [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) o a la [función MkParseDisplayNameEx.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85))

Puede usar un moniker de sesión de la misma manera que usaría cualquier otro moniker.

Para obtener un ejemplo de código que muestra cómo activar un proceso de servidor local en una sesión especificada, vea [Usar un Moniker de sesión](using-a-session-moniker.md).

Para más información sobre la activación de objetos, monikers proporcionados por el sistema y monikers de clase, consulte la documentación de COM en Platform SDK.

> [!Note]  
> Los procesos que se crean entre sesiones tienen un límite superior en el tamaño del bloque de entorno. Este límite es de aproximadamente 4 KB, pero puede ser mayor o menor en función de la información que se necesite para crear el proceso (por ejemplo, nombres de archivo, directorios y parámetros para el nuevo proceso).

 

 

 