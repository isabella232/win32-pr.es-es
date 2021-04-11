---
description: Especifica una clave para seleccionar una fila única en una colección escalar o de tabla.
ms.assetid: 3c4edae0-55be-4804-b5fe-07458b918365
ms.tgt_platform: multiple
title: INDEX (cláusula)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 915cbe1c4bf1da5ccd7fbab881770722b70bc53c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156768"
---
# <a name="index-clause"></a>INDEX (cláusula)

La cláusula INDEX especifica una clave para seleccionar una fila única en una colección escalar o de tabla. El proveedor SNMP se asigna a un tipo diferente de clase CIM según el tipo de tabla que usa el dispositivo SNMP. Dado que una clave puede ser más de un tipo de objeto, el proveedor usa reglas de asignación diferentes en función del tipo de objeto dentro de la clave. Para obtener más información, vea tipos de datos de la [cláusula index](#index-clause-data-types).

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Una colección escalar se asigna a una clase singleton CIM: es decir, una clase que solo puede tener una instancia. Dado que no es necesario identificar de forma única una instancia de otra, una clase singleton no designa una o varias propiedades como clave. Clases generadas a partir de colecciones escalares:

-   No contenga calificadores de propiedad de **clave** .
-   Contenga el calificador de clase CIM estándar **Singleton**, que es de tipo **bool**.

Una colección de tablas se asigna a una clase CIM que puede tener más de una instancia. Como resultado, la definición de clase CIM debe contener al menos una propiedad que defina la clave de objeto. es decir, una propiedad que identifica de forma única una instancia de la clase. La cláusula INDEX de la macro [Object-Type](object-type-macro.md) de una colección de tablas especifica el conjunto de propiedades de clave de la colección. Se aplican las siguientes reglas de asignación:

-   La **clave** de calificador de CIM, tipo **bool**, define una propiedad de clave.
-   El orden de la información de índice dentro de la colección de tablas define el orden de las claves dentro de la definición de clase CIM.

    El orden de **claves \_** del calificador de CIM define el orden de las claves. Este calificador es un valor entero de 32 bits sin signo que, para los fines de la sintaxis del calificador MOF, se debe convertir en un valor entero de 32 bits con signo mediante la operación de complemento de dos.

Actualmente, la asignación de la cláusula de índice SNMPv2C no controla el uso del calificador **implícito** . En este caso, no se genera una definición de clase CIM.

## <a name="index-clause-data-types"></a>Tipos de datos de la cláusula INDEX

Debido a la flexibilidad de la cláusula INDEX dentro de la macro [Object-Type](object-type-macro.md) , la especificación de las propiedades con clave no es sencilla. En su lugar, debe tener en cuenta las posibilidades de que la cláusula INDEX contenga uno o varios de los siguientes tipos de datos:

-   Valor de **indexobject** accesible internamente

    El valor **indexobject** es un valor con nombre que hace referencia a una definición de objeto MIB que aparece en la fila conceptual de la misma tabla que contiene la cláusula index. La definición del objeto MIB a la que se hace referencia en la cláusula de índice se asigna a una propiedad de clave de la definición de clase CIM.

-   Valor de **indexobject** accesible externamente

    En este caso, **indexobject** es un valor con nombre que hace referencia a una definición de objeto MIB que aparece en la fila conceptual de una tabla diferente.

-   Valor de **indextype** accesible

    El valor de **indextype** es un tipo con nombre que hace referencia a uno de los siguientes tipos de datos: **entero**, **cadena de octeto**, **identificador de objeto**, **NetworkAddress** o **IpAddress**. Si la cláusula INDEX contiene una referencia de tipo MIB, se aplican las siguientes reglas de asignación:

    -   El objeto MIB al que se hace referencia se asigna a una propiedad de clave de la definición de clase CIM. Su sintaxis de tipo se basa en el valor **indextype** especificado, que se asigna a los calificadores de propiedad CIM mediante los procedimientos de asignación de [cláusulas de sintaxis](syntax-clause.md) estándar.
    -   El proceso de asignación genera un nombre de propiedad único concatenando el descriptor de objeto de tabla MIB, un carácter de subrayado ( \_ ) y el orden de clasificación del valor **indextype** de la cláusula index. Por ejemplo, el nombre de la propiedad del tercer componente **indextype** de la tabla MIB **enterpriseIfTable** es **enterpriseIfTable \_ 3**.
    -   La propiedad CIM se anota con el calificador de **\_ clave virtual** . Este calificador especifica que el proveedor SNMP debe calcular el valor de la propiedad basándose en el supraconjunto de información de instancia asociado a todas las definiciones de objeto MIB accesibles en la definición de clase.
    -   La definición de clase CIM debe contener al menos una propiedad que no tenga un calificador de **\_ clave virtual** asociado; si no se especifica esta propiedad, se invalidará la definición de clase.

-   Subtipo de longitud fija

    Cuando la cláusula INDEX de una colección de tablas SNMP contiene un tipo compatible con SNMP que se subescribe como una cadena de octeto de longitud fija, se debe usar **la \_ longitud fija** del calificador de la propiedad CIM para especificar este valor.

 

 



