---
title: Crear una lista de enlaces de variables
description: La función SnmpCreateVbl crea una nueva lista de enlaces de variables.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e9ef7aa208e2e2f887d14c0e124f3bb659ff8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268899"
---
# <a name="creating-a-variable-binding-list"></a>Crear una lista de enlaces de variables

La función [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) crea una nueva lista de enlaces de variables. Si la aplicación WinSNMP especifica un nombre de variable y un valor, la función crea la lista y agrega el nombre y el valor como la primera entrada de la lista. Si la aplicación especifica **null** para el nombre de la variable, la función crea una lista vacía.

Para copiar una lista de enlaces de variables, llame a la función [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) . La función crea una nueva lista de enlaces de variables e inicializa la nueva lista con una copia de los datos en la lista de enlaces de variables de origen.

La función [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) y la función [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) asignan cualquier memoria necesaria para la nueva lista de enlaces de variables. La aplicación WinSNMP debe liberar los recursos asociados a estas listas. Se recomienda que la aplicación haga esto coincidentes con cada llamada a [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) y [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) con la llamada correspondiente a la función [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) cuando sea adecuado liberar la memoria asignada.

 

 




