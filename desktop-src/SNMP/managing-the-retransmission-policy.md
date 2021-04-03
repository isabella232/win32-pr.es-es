---
title: Administrar la Directiva de retransmisión
description: La aplicación WinSNMP puede solicitar que la implementación de Microsoft WinSNMP ejecute la Directiva de retransmisión de la aplicación. Cuando la implementación administra la retransmisión, usa el período de tiempo de espera y los valores de número de reintentos en su base de datos.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2e47d983f8da62ccb8ffbe9c20b35c71bfbb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076052"
---
# <a name="managing-the-retransmission-policy"></a>Administrar la Directiva de retransmisión

La aplicación WinSNMP puede solicitar que la implementación de Microsoft WinSNMP ejecute la Directiva de retransmisión de la aplicación. Cuando la implementación administra la retransmisión, usa el período de tiempo de espera y los valores de número de reintentos en su base de datos.

La implementación de identifica el modo de retransmisión predeterminado en un valor devuelto de la función [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) durante la inicialización. El modo puede ser uno de los valores siguientes.



| Value        | Significado                                                                      |
|--------------|------------------------------------------------------------------------------|
| SNMPAPI \_  | La implementación está ejecutando la Directiva de retransmisión de la aplicación.     |
| SNMPAPI \_ desactivado | La implementación no está ejecutando la Directiva de retransmisión de la aplicación. |



 

Una aplicación WinSNMP puede recuperar en cualquier momento el modo de retransmisión actual en vigor para la implementación mediante una llamada a la función [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) . La API WinSNMP proporciona otras [funciones de base de datos](winsnmp-functions.md) que simplifican la administración de la Directiva de retransmisión.

En cualquier momento durante la ejecución del programa, la aplicación WinSNMP puede ajustar la ejecución de la Directiva llevando a cabo uno de los siguientes pasos:

-   Solicite que la implementación inicie o detenga la ejecución de la Directiva de retransmisión mediante una llamada a la función [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) . Para obtener más información, consulte [activación y desactivación de la retransmisión](turning-retransmission-on-and-off.md).
-   Modifique el período de tiempo de espera y los valores de número de reintentos en la base de datos de implementación. Para obtener más información, consulte [cambiar la Directiva de retransmisión](changing-the-retransmission-policy.md).
-   Llame a la función [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) para cancelar el ciclo de retransmisión y liberar las estructuras de datos internas asociadas a una única solicitud de mensaje SNMP. Para obtener más información, consulte cancelación de la [retransmisión](canceling-retransmission.md).

La aplicación puede ejecutar su propia Directiva de retransmisión. En este caso, la ejecución puede o no basarse en los valores de la base de datos.

 

 




