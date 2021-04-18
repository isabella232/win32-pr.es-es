---
description: Puede utilizar el proveedor del registro del sistema como una instancia o un proveedor de propiedades.
ms.assetid: 0a8198c0-57c1-4d96-9965-3867c8c0e738
ms.tgt_platform: multiple
title: Usar el proveedor del registro del sistema como proveedor de propiedades
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64fc701843438b4d173b1914ed2ac86214fe685e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706747"
---
# <a name="use-the-system-registry-provider-as-a-property-provider"></a>Usar el proveedor del registro del sistema como proveedor de propiedades

Puede utilizar el [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) como una instancia o un proveedor de propiedades.

Si opta por tener acceso a las interfaces del proveedor de propiedades, debe marcar las clases WMI para indicar su intención.

**Para utilizar el proveedor del registro del sistema como proveedor de propiedades**

-   Defina la clase WMI con los calificadores estándar **DynProps**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)y **PropertyContext** .

    El calificador **DynProps** identifica una clase que tiene las propiedades que mantiene el proveedor de propiedades identificado por el calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) . El calificador **PropertyContext** especifica el nombre del valor del registro que la propiedad va a almacenar. El formato del calificador **PropertyContext** es el mismo que el formato del calificador **ClassContext** con valores de *expresión* y *ValueName* adicionales.

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    *ValueName* y *Expression* son opcionales. El valor de *ValueName* solo se utiliza si el valor del registro tiene un nombre. La *expresión* también es opcional y se usa para los datos del descriptor de recursos. Para obtener más información, vea [Descripción de un recurso para el registro](describing-a-resource-for-the-registry.md).

    En el ejemplo de código siguiente se muestra cómo la clase utiliza el proveedor del registro del sistema como un proveedor de propiedades para mantener sus propiedades sin clave.

    ``` syntax
    [DYNPROPS]
    class PropReg {

        [KEY]  STRING  MyKey;
        STRING Logging;
        STRING Events;
        uint32 Resource1;
    };

    [DYNPROPS]
    instance of PropReg
    {
      MyKey = "a";

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|Logging"), Dynamic, Provider("RegPropProv")]  Logging;

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|EnableEvents"), Dynamic, Provider("RegPropProv")]
       Events;

      [PropertyContext("local|hkey_local_Machine\\hardware\\
       ResourceMap\\Hardware Abstraction Layer\\PC Compatible Eisa/isa 
       hal|.raw(\"Internal\")(0)(0)(\"interrupt.vector\")"), Dynamic, 
       Provider("RegPropProv")]  Resource1;
    };
    ```

 

 
