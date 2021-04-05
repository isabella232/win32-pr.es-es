---
description: Las clases que se usan para almacenar los datos del registro se definen con varios calificadores estándar.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Definir una clase del registro con calificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45fdff611814eadbf57eabedf7444d098666918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908679"
---
# <a name="defining-a-registry-class-with-qualifiers"></a>Definir una clase del registro con calificadores

Las clases que se usan para almacenar los datos del registro se definen con varios calificadores estándar.

A continuación se muestra una lista de los calificadores estándar:

-   [Dynamic](standard-wmi-qualifiers.md) y [ **Provider**](/windows/desktop/api/Provider/nl-provider-provider)

    Puede asociar el calificador **dinámico** a una clase o una instancia. El calificador **dinámico** marca la clase o instancia como administrada dinámicamente por un proveedor. Cuando se muestra **Dynamic** en una clase o instancia, también debe aparecer el calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) . El calificador de **proveedor** identifica el proveedor determinado que debe administrar la clase dinámica o la instancia.

-   [ClassContext](standard-wmi-qualifiers.md)

    El calificador **ClassContext** se adjunta a una clase. Especifica la ruta de acceso a la clave del registro que contiene la información que la clase representa.

    El calificador **ClassContext** tiene el formato siguiente.

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    El valor de la ruta de clave puede ser largo si incluye claves con subclaves.

    En el ejemplo siguiente se muestra el calificador **ClassContext** que contiene la ruta de acceso a un dispositivo de transporte de equipo determinado.

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

La plantilla siguiente para una definición de clase muestra el uso de los calificadores **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)y **ClassContext** . El proveedor denominado por el calificador de **proveedor** es el proveedor del registro del sistema de la instancia. Tenga en cuenta que las rutas de acceso del registro no distinguen mayúsculas de minúsculas, como son los nombres de los calificadores.

``` syntax
[dynamic, provider("RegProv"), 
    ClassContext("local|hkey_local_machine\\software\\microsoft
    \\WBEM\\transports\\Network Transport Modules")]

class RegTrans
{
  [key] string  TransportsGUID;
  [PropertyContext("Name")] string Name;
  [PropertyContext("Independent")] uint32 Enabled;
};
```

Las aplicaciones de administración también pueden utilizar el proveedor del registro del sistema para recuperar y modificar los datos del registro de una clave determinada.

 

 



