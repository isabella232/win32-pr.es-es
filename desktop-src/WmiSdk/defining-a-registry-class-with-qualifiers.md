---
description: Las clases usadas para contener datos del Registro se definen con varios calificadores estándar.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Definir una clase del Registro con calificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45fdff611814eadbf57eabedf7444d098666918
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270367"
---
# <a name="defining-a-registry-class-with-qualifiers"></a>Definir una clase del Registro con calificadores

Las clases usadas para contener datos del Registro se definen con varios calificadores estándar.

A continuación se muestra una lista de los calificadores estándar:

-   [Dynamic](standard-wmi-qualifiers.md) y [ **Provider**](/windows/desktop/api/Provider/nl-provider-provider)

    Puede asociar el **calificador Dinámico** a una clase o a una instancia de . El **calificador Dinámico** marca la clase o instancia como administrada dinámicamente por un proveedor. Cuando **dynamic** aparece en una clase o instancia, también debe aparecer [**el calificador**](/windows/desktop/api/Provider/nl-provider-provider) Provider. El **calificador** Provider identifica el proveedor determinado que debe administrar la clase o instancia dinámica.

-   [ClassContext](standard-wmi-qualifiers.md)

    El **calificador ClassContext** está asociado a una clase. Especifica la ruta de acceso a la clave del Registro que contiene la información que representa la clase .

    El **calificador ClassContext** tiene el formato siguiente.

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    El valor de KeyPath puede ser largo si incluye claves con subclaves.

    En el ejemplo siguiente se muestra el **calificador ClassContext** que contiene la ruta de acceso a un dispositivo de transporte de equipo determinado.

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

La plantilla siguiente para una definición de clase muestra el uso de los calificadores **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)y **ClassContext.** El proveedor denominado por el **calificador Provider** es el proveedor del Registro del sistema de instancia. Tenga en cuenta que las rutas de acceso del Registro no tienen en cuenta mayúsculas de minúsculas, al igual que los nombres de calificador.

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

Las aplicaciones de administración también pueden usar el proveedor del Registro del sistema para recuperar y modificar los datos del Registro de una clave determinada.

 

 



