---
title: Administrar una lista de enlaces de variables
description: La función SnmpGetVb recupera información de enlace de variables de una lista de enlaces de variables. La función recupera el nombre de la variable y el valor asociado de la variable de la entrada de enlace de variables especificada por la aplicación WinSNMP.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc8c1cbfa4eb0ec3acdc13e9c9cc480b88ddae8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075475"
---
# <a name="managing-a-variable-binding-list"></a>Administrar una lista de enlaces de variables

La función [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) recupera información de enlace de variables de una lista de enlaces de variables. La función recupera el nombre de la variable y el valor asociado de la variable de la entrada de enlace de variables especificada por la aplicación WinSNMP.

Para actualizar las entradas de enlace de variables en una lista de enlaces de variables, llame a la función [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) . La función **SnmpSetVb** también anexa nuevas entradas de enlace de variables a una lista de enlaces de variables existente.

La aplicación WinSNMP debe llamar a la función [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) para quitar las entradas de una lista de enlaces de variables.

Para recuperar, modificar o eliminar una entrada de enlace de variables, la aplicación WinSNMP debe especificar la posición de la entrada en la lista de enlaces de variables.

Una llamada a la función [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) asocia una lista de enlaces de variables a una PDU. Una llamada a la función [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) recupera una lista de enlaces de variables de una PDU. Un enlace de variable individual no está asociado directamente a una PDU, pero se asocia indirectamente a través de su inclusión en una lista de enlaces de variables.

 

 




