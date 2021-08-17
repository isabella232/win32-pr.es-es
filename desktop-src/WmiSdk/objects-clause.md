---
description: La cláusula OBJECTS de la macro NOTIFICATION-TYPE enumera el conjunto de objetos asociados al objeto de notificación.
ms.assetid: 0cb4776f-aae2-452d-9472-caf6d28fb870
ms.tgt_platform: multiple
title: OBJECTS (Cláusula)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9289be0a3fa228e74a720ec385a5b13354f849710a88287a9911f470e40758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131047"
---
# <a name="objects-clause"></a>OBJECTS (Cláusula)

La cláusula OBJECTS de la macro [NOTIFICATION-TYPE](notification-type-macro.md) enumera el conjunto de objetos asociados al objeto de notificación.

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configuración del entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

Las reglas siguientes se aplican al asignar a clases CIM:

-   Cada miembro de la cláusula OBJECTS se asigna a una propiedad de la definición de clase CIM. El descriptor de objeto del miembro asigna textualmente al nombre de la propiedad CIM. Por ejemplo, **ifIndex se** traduce a **ifIndex**.
-   Cada propiedad CIM generada por el proceso de asignación contiene el **calificador VarBindIndex.**

    **VarBindIndex** es un calificador **obligatorio uint32** que describe la posición del objeto tal como aparece en la cláusula OBJECTS de [la macro TRAP-TYPE](trap-type-macro.md) o [NOTIFICATION-TYPE.](notification-type-macro.md) El entero también especifica la posición de la propiedad tal como aparece en la lista de enlaces de variables de SNMPv1 o SNMPv2C TRAP PDU (unidad de datos de protocolo), respectivamente. (Dado que los dos primeros enlaces de variables son siempre TimeStamp e Identification, las variables adicionales se numeran después del valor 2).

    Cuando la clase de eventos CIM se genera a partir de una macro [TRAP-TYPE](trap-type-macro.md) de SNMPv1, el calificador **VarBindIndex** tiene un valor inicial de 1 para la primera variable de la lista de enlaces de variables.

    Cuando la clase de eventos CIM se genera a partir de una macro [NOTIFICATION-TYPE](notification-type-macro.md) de SNMPv2C, el calificador **VarBindIndex** tiene un valor inicial de 3 para la primera variable de la lista de enlaces de variables.

Al asignar una clase CIM encapsulada, cada miembro de la cláusula OBJECTS se asigna a una propiedad CIM que refleja el nombre, el tipo y el valor del objeto MIB correspondiente. Los procedimientos de asignación utilizados se especifican en los temas siguientes:

-   [CLÁUSULA SYNTAX](syntax-clause.md)
-   [TEXTUAL-CONVENTION (Macro)](textual-convention-macro.md)
-   [Cláusulas ACCESS y MAX-ACCESS](access-and-max-access-clauses.md)

Cuando se usa una clase CIM de referencia, cada miembro de la cláusula OBJECTS se asigna de la siguiente manera:

-   Cada miembro de la cláusula OBJECTS se asigna a una sola propiedad de la clase CIM. La propiedad está fuertemente typed como un objeto incrustado.
-   La clase del objeto incrustado se genera a través del procedimiento de asignación de objetos estándar. Para obtener más información, vea [OBJECT-TYPE Macro](object-type-macro.md). Por ejemplo, **ifTable se** asigna a una clase insertada denominada **SNMP \_ RFC1213 \_ MIB \_ ifTable**.
-   Se crea una instancia de los valores asociados a los enlaces de variables de una PDU TRAP como objetos incrustados de un objeto de la clase de referencia. Cada objeto incrustado contiene valores para cada una de las propiedades con clave del objeto y el valor de la propiedad en el enlace de variables que se está asignando.

 

 



