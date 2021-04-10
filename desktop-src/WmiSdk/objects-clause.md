---
description: La cláusula OBJECTs de la macro NOTIFICATION-TYPE enumera el conjunto de objetos asociados al objeto de notificación.
ms.assetid: 0cb4776f-aae2-452d-9472-caf6d28fb870
ms.tgt_platform: multiple
title: OBJECTs (cláusula)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e25848e0fc98ca79ef96e25423ba7872296e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275171"
---
# <a name="objects-clause"></a>OBJECTs (cláusula)

La cláusula OBJECTs de la macro [Notification-Type](notification-type-macro.md) enumera el conjunto de objetos asociados al objeto de notificación.

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Cuando se asignan a clases CIM, se aplican las siguientes reglas:

-   Cada miembro de la cláusula OBJECTs se asigna a una propiedad de la definición de clase CIM. El descriptor de objeto del miembro se asigna literalmente al nombre de la propiedad CIM. Por **ejemplo, el** **siguiente se convierte** en un bajo.
-   Cada propiedad CIM generada por el proceso de asignación contiene el calificador **VarBindIndex** .

    **VarBindIndex** es un calificador de **UInt32** obligatorio que describe la posición del objeto tal y como aparece en la cláusula Objects de la macro [Trap-Type](trap-type-macro.md) o [Notification-Type](notification-type-macro.md) . El entero también especifica la posición de la propiedad tal y como aparece en la lista de enlaces de variables de la PDU de captura de SNMPv1 o SNMPv2C (unidad de datos de protocolo), respectivamente. (Dado que los dos primeros enlaces de variables siempre son TimeStamp e Identification, las variables adicionales se numeran después del valor 2).

    Cuando la clase de eventos CIM se genera a partir de una macro SNMPv1 [Trap-Type](trap-type-macro.md) , el calificador **VarBindIndex** tiene un valor inicial de 1 para la primera variable de la lista de enlaces de variables.

    Cuando la clase de eventos CIM se genera a partir de una macro [de tipo de notificación](notification-type-macro.md) SNMPv2c, el calificador **VarBindIndex** tiene un valor inicial de 3 para la primera variable de la lista de enlaces de variables.

Al asignar una clase CIM encapsulada, cada miembro de la cláusula OBJECTs se asigna a una propiedad CIM que refleja el nombre, el tipo y el valor del objeto MIB correspondiente. Los procedimientos de asignación utilizados se especifican en los temas siguientes:

-   [Cláusula de sintaxis](syntax-clause.md)
-   [Macro de Convención de texto](textual-convention-macro.md)
-   [Cláusulas Access y MAX-ACCESS](access-and-max-access-clauses.md)

Cuando se usa una clase CIM referente, cada miembro de la cláusula OBJECTs se asigna de la siguiente manera:

-   Cada miembro de la cláusula OBJECTs se asigna a una única propiedad de la clase CIM. La propiedad está fuertemente tipada como un objeto incrustado.
-   La clase del objeto incrustado se genera mediante el procedimiento de asignación de objeto estándar. Para obtener más información, vea [macro Object-Type](object-type-macro.md). Por ejemplo, **ifTable** se asigna a una clase incrustada denominada **SNMP \_ RFC1213 \_ MIB \_ ifTable**.
-   Los valores asociados a los enlaces de variables de una PDU de captura se crean como objetos incrustados de un objeto de la clase referente. Cada objeto incrustado contiene valores para cada una de las propiedades con clave del objeto y el valor de la propiedad en el enlace de variable que se está asignando.

 

 



