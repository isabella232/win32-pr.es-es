---
title: Administración de una lista de enlaces de variables
description: La función SnmpGetVb recupera información de enlace de variables de una lista de enlaces de variables. La función recupera el nombre de la variable y el valor asociado de la variable de la entrada de enlace de variable especificada por la aplicación WinSNMP.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c382e2780ae49a1f029aab2cfef2bcd4357fcfbf7b37ce9a1fcad9aed5bc0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009453"
---
# <a name="managing-a-variable-binding-list"></a>Administración de una lista de enlaces de variables

La [**función SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) recupera información de enlace de variables de una lista de enlaces de variables. La función recupera el nombre de la variable y el valor asociado de la variable de la entrada de enlace de variable especificada por la aplicación WinSNMP.

Para actualizar las entradas de enlace de variables en una lista de enlaces de variables, llame a la [**función SnmpSetVb.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) La **función SnmpSetVb** también anexa nuevas entradas de enlace de variables a una lista de enlaces de variables existente.

La aplicación WinSNMP debe llamar a [**la función SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) para quitar entradas de una lista de enlaces de variables.

Para recuperar, modificar o eliminar una entrada de enlace de variables, la aplicación WinSNMP debe especificar la posición de la entrada en la lista de enlaces de variables.

Una llamada a la [**función SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) asocia una lista de enlaces de variables a una PDU. Una llamada a la [**función SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) recupera una lista de enlaces de variables de una PDU. Un enlace de variable individual no está asociado directamente a una PDU, pero se asocia indirectamente a través de su inclusión en una lista de enlaces de variables.

 

 




