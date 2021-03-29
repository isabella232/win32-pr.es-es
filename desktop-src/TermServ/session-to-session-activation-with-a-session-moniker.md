---
title: Activación de sesión a sesión con un moniker de sesión
description: La activación de sesión a sesión (también denominada activación entre sesiones) permite que un proceso de cliente inicie (Active) un proceso de servidor local en una sesión especificada.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2714f3dbe7b23c8b7f04d4271018891960b87f76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793365"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a>Activación de sesión a sesión con un moniker de sesión

La activación de sesión a sesión (también denominada activación entre sesiones) permite que un proceso de cliente inicie (Active) un proceso de servidor local en una sesión especificada. Esta característica está disponible para las aplicaciones que están configuradas para ejecutarse en el contexto de seguridad del usuario interactivo, también conocido como el modo de activación de objetos de "usuario interactivo de runas". Para obtener más información sobre los contextos de seguridad, vea [el contexto de seguridad del cliente](/windows/desktop/SecAuthZ/the-client-security-context).

COM distribuido (DCOM) permite la activación de objetos por sesión mediante el uso de un [moniker de sesión](session-monikers.md)proporcionado por el sistema. Otros monikers proporcionados por el sistema son monikers de [archivo](../com/file-monikers.md), monikers de [elemento](../com/item-monikers.md), monikers [compuestos](../com/composite-monikers.md)genéricos, [anti-monikers](../com/anti-monikers.md), monikers de [puntero](../com/pointer-monikers.md)y [monikers de dirección URL](../com/url-monikers.md).

Para poder utilizar el moniker de sesión, la aplicación DCOM debe estar configurada para ejecutarse como usuario interactivo. Esto se puede establecer mediante la herramienta administrativa Servicios de componentes, viendo las propiedades de la aplicación DCOM y seleccionando **el usuario interactivo** en la pestaña **identidad** . Para obtener más información sobre los posibles riesgos de seguridad asociados con la configuración de una aplicación DCOM para que se ejecute como usuario interactivo en un entorno de Servicios de Escritorio remoto, vea la sección "identidad de la aplicación (COM)" de la documentación de COM en el kit de desarrollo de software (SDK) de la plataforma.

Si se selecciona cualquier otro tipo de usuario para ejecutar la aplicación, la aplicación omitirá el moniker de la sesión. Las aplicaciones de servidor COM+ también omiten el moniker de la sesión. Para obtener más información acerca de otros métodos para seleccionar el tipo de usuario para ejecutar la aplicación, consulte la documentación de COM en el SDK de la plataforma.

Para crear un moniker de sesión, debe componer el ID. de sesión de la sesión de Servicios de Escritorio remoto con un moniker de clase que especifique el identificador de clase del servidor de procesos.

**Para crear un moniker de sesión**

1.  Prefije el nombre para mostrar del moniker de clase con el nombre para mostrar del moniker de la sesión mediante la sintaxis siguiente:

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    donde *digits* representa el ID. de sesión de la sesión en la que se iniciará el proceso de servidor y donde ID. de *clase* representa el ID. de clase del servidor. Tenga en cuenta que el identificador de sesión es un número de base 10.

    En el caso de los equipos que ejecutan Windows XP o versiones posteriores, el uso de la siguiente sintaxis dará como resultado que COM envíe la activación a la sesión de consola física activa actualmente, sea cual sea su identificador de sesión:

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  Después de haber creado el moniker de la sesión, puede pasar el resultado a la función [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) o a la función [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) .

Puede utilizar un moniker de la sesión de la misma manera que usaría cualquier otro moniker.

Para obtener un ejemplo de código que muestra cómo activar un proceso de servidor local en una sesión especificada, vea [usar un moniker de sesión](using-a-session-moniker.md).

Para obtener más información sobre la activación de objetos, monikers y monikers proporcionados por el sistema, vea la documentación de COM en Platform SDK.

> [!Note]  
> Los procesos que se crean en las sesiones tienen un límite superior en el tamaño del bloque de entorno. Este límite es de aproximadamente 4 KB, pero puede ser mayor o menor en función de la información que se necesite para crear el proceso (por ejemplo, nombres de archivo, directorios y parámetros para el nuevo proceso).

 

 

 