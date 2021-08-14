---
description: Especifica una clave para seleccionar una fila única en una colección escalar o de tabla.
ms.assetid: 3c4edae0-55be-4804-b5fe-07458b918365
ms.tgt_platform: multiple
title: CLÁUSULA INDEX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca4478164839412238f59d9771aa9c96417c4055390cb4599edbb40b0e6b4a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318747"
---
# <a name="index-clause"></a>CLÁUSULA INDEX

La cláusula INDEX especifica una clave para seleccionar una fila única en una colección escalar o de tabla. El proveedor SNMP se asigna a un tipo diferente de clase CIM en función del tipo de tabla que use el dispositivo SNMP. Dado que una clave puede ser más de un tipo de objeto, el proveedor usa reglas de asignación diferentes en función del tipo de objeto dentro de la clave. Para obtener más información, vea [Tipos de datos de cláusula INDEX](#index-clause-data-types).

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configurar el entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

Una colección escalar se asigna a una clase singleton cim: es decir, una clase que solo puede tener una instancia. Dado que no es necesario identificar de forma única una instancia de otra, una clase singleton no designa una o varias propiedades como clave. Clases generadas a partir de colecciones escalares:

-   No contenga **calificadores de** propiedad Key.
-   Contiene el calificador de clase CIM **estándar Singleton**, que es de tipo **Bool**.

Una colección de tablas se asigna a una clase CIM que puede tener más de una instancia. Como resultado, la definición de clase CIM debe contener al menos una propiedad que defina la clave de objeto; es decir, una propiedad que identifica de forma única una instancia de la clase . La cláusula INDEX de la macro [OBJECT-TYPE](object-type-macro.md) de una colección de tablas especifica el conjunto de propiedades de clave de la colección. Se aplican las siguientes reglas de asignación:

-   El calificador CIM **Key**, tipo **Bool**, define una propiedad de clave.
-   El orden de la información index dentro de la colección de tablas define el orden de las claves dentro de la definición de clase CIM.

    El calificador CIM **Key \_ Order** define el orden de las claves. Este calificador es un valor entero de 32 bits sin signo que, a efectos de la sintaxis del calificador MOF, se debe convertir en un valor entero de 32 bits con signo mediante la operación twos-complement.

Actualmente, la asignación de la cláusula SNMPv2C INDEX no controla el uso del calificador **IMPLIED.** En este caso, no se genera una definición de clase CIM.

## <a name="index-clause-data-types"></a>Tipos de datos de cláusula INDEX

Debido a la flexibilidad de la cláusula INDEX dentro de la macro [OBJECT-TYPE,](object-type-macro.md) la especificación de las propiedades con clave no es sencilla. En su lugar, debe tener en cuenta las posibilidades de que la cláusula INDEX pueda contener uno o varios de los siguientes tipos de datos:

-   Valor **indexobject** accesible internamente

    El **valor indexobject** es un valor con nombre que hace referencia a una definición de objeto MIB que aparece en la fila conceptual de la misma tabla que contiene la cláusula INDEX. La definición de objeto MIB a la que se hace referencia en la cláusula INDEX se asigna a una propiedad clave de la definición de clase CIM.

-   Valor indexobject accesible **externamente**

    En este caso, **indexobject** es un valor con nombre que hace referencia a una definición de objeto MIB que aparece en la fila conceptual de una tabla diferente.

-   Valor **indextype accesible**

    El **valor indextype** es un tipo con nombre que hace referencia a uno de los siguientes tipos de datos: **INTEGER**, **OCTET STRING,** **OBJECT IDENTIFIER,** **NetworkAddress** o **IpAddress.** Si la cláusula INDEX contiene una referencia de tipo MIB, se aplican las siguientes reglas de asignación:

    -   El objeto MIB al que se hace referencia se asigna a una propiedad clave de la definición de clase CIM. Su sintaxis de tipo se basa en el **valor indextype** especificado, que se asigna a calificadores de propiedad CIM mediante los procedimientos de asignación de [cláusulas SYNTAX](syntax-clause.md) estándar.
    -   El proceso de asignación genera un nombre de propiedad único mediante la concatenación del descriptor de objetos de tabla MIB, un carácter de subrayado ( ) y el orden de clasificación del valor indextype de la \_ **cláusula** INDEX. Por ejemplo, el nombre de propiedad del tercer tipo de **índice** de componente de la tabla MIB **enterpriseIfTable** es **enterpriseIfTable \_ 3.**
    -   La propiedad CIM se anota con el **calificador \_ de clave** virtual. Este calificador especifica que el proveedor SNMP debe calcular el valor de la propiedad en función del superconjunto de información de instancia asociado a todas las definiciones de objetos MIB accesibles en la definición de clase.
    -   La definición de clase CIM debe contener al menos una propiedad que no tenga un calificador de clave **virtual \_** asociado; si no se especifica esta propiedad, se invalida la definición de clase.

-   Subtipo de longitud fija

    Cuando la cláusula INDEX de una colección de tablas SNMP contiene un tipo compatible con SNMP que está subtipo como UNA CADENA DE OCTET de longitud fija, se debe usar el calificador de propiedad CIM **Fixed \_ Length** para especificar este valor.

 

 



