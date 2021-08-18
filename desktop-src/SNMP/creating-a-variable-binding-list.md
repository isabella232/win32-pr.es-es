---
title: Crear una lista de enlaces de variables
description: La función SnmpCreateVbl crea una nueva lista de enlaces de variables.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2530b59524375ad6413ff9aa1416db8e25ee3641136284cb4a0f70795e388a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009583"
---
# <a name="creating-a-variable-binding-list"></a>Crear una lista de enlaces de variables

La [**función SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) crea una nueva lista de enlaces de variables. Si la aplicación WinSNMP especifica un nombre de variable y un valor, la función crea la lista y agrega el nombre y el valor como primera entrada de la lista. Si la aplicación especifica **NULL para** el nombre de variable, la función crea una lista vacía.

Para copiar una lista de enlaces de variables, llame a [**la función SnmpDuplicateVbl.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) La función crea una nueva lista de enlaces de variables e inicializa la nueva lista con una copia de los datos de la lista de enlace de variables de origen.

La [**función SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) y la [**función SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) asignan la memoria necesaria para la nueva lista de enlaces de variables. La aplicación WinSNMP debe liberar los recursos asociados a estas listas. Se recomienda que la aplicación haga esto haciendo coincidir cada llamada a [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) y [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) con una llamada correspondiente a la función [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) cuando sea adecuado liberar la memoria asignada.

 

 




