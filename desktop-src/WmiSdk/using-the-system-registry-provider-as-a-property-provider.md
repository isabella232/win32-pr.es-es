---
description: Puede usar el proveedor del Registro del sistema como una instancia o un proveedor de propiedades.
ms.assetid: 0a8198c0-57c1-4d96-9965-3867c8c0e738
ms.tgt_platform: multiple
title: Usar el proveedor del Registro del sistema como proveedor de propiedades
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1b9b23be76845512df76bc0327543d463fd5eec6a816d57871f959b53229aecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107455"
---
# <a name="use-the-system-registry-provider-as-a-property-provider"></a>Usar el proveedor del Registro del sistema como proveedor de propiedades

Puede usar el proveedor [del Registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) como una instancia o un proveedor de propiedades.

Si decide acceder a las interfaces del proveedor de propiedades, debe marcar las clases WMI para indicar su intención.

**Para usar el proveedor del Registro del sistema como proveedor de propiedades**

-   Defina la clase WMI con los calificadores **estándar DynProps**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)y **PropertyContext.**

    El **calificador DynProps** identifica una clase como que tiene propiedades que mantiene el proveedor de propiedades identificado por el [**calificador Provider.**](/windows/desktop/api/Provider/nl-provider-provider) El **calificador PropertyContext** especifica el nombre del valor del Registro que va a almacenar la propiedad . El formato del **calificador PropertyContext** es el mismo que el formato del calificador **ClassContext** con valores de expresión y *valuename* *adicionales.*

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    Tanto *valuename como* *expression* son opcionales. La *configuración valuename* solo se usa si el valor del Registro tiene un nombre. La *expresión* también es opcional y se usa para los datos del descriptor de recursos. Para obtener más información, [vea Describing a Resource for the Registry](describing-a-resource-for-the-registry.md).

    En el ejemplo de código siguiente se muestra cómo la clase utiliza el proveedor del Registro del sistema como proveedor de propiedades para mantener sus propiedades sin clave.

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

 

 
