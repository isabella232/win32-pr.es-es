---
title: Administración de la directiva de retransmisión
description: La aplicación WinSNMP puede solicitar que la implementación de Microsoft WinSNMP ejecute la directiva de retransmisión de la aplicación. Cuando la implementación administra la retransmisión, usa el período de tiempo de espera y los valores de recuento de reintentos en su base de datos.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63737f8cb4a0fcdb8c6e3824d07cbc7c592c1f7e9813e8751197fcd1d64ad786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009433"
---
# <a name="managing-the-retransmission-policy"></a>Administración de la directiva de retransmisión

La aplicación WinSNMP puede solicitar que la implementación de Microsoft WinSNMP ejecute la directiva de retransmisión de la aplicación. Cuando la implementación administra la retransmisión, usa el período de tiempo de espera y los valores de recuento de reintentos en su base de datos.

La implementación identifica el modo de retransmisión predeterminado en un valor devuelto de la [**función SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) durante la inicialización. El modo puede ser uno de los siguientes valores.



| Value        | Significado                                                                      |
|--------------|------------------------------------------------------------------------------|
| SNMPAPI \_ ON  | La implementación está ejecutando la directiva de retransmisión de la aplicación.     |
| SNMPAPI \_ OFF | La implementación no está ejecutando la directiva de retransmisión de la aplicación. |



 

Una aplicación WinSNMP puede recuperar en cualquier momento el modo de retransmisión actual en vigor para la implementación llamando a la [**función SnmpGetRetransmitMode.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) La API de WinSNMP proporciona otras [funciones de base de](winsnmp-functions.md) datos que simplifican la administración de la directiva de retransmisión.

En cualquier momento durante la ejecución del programa, la aplicación WinSNMP puede ajustar la ejecución de la directiva mediante uno de los pasos siguientes:

-   Solicite que la implementación inicie o detenga la ejecución de la directiva de retransmisión llamando a la [**función SnmpSetRetransmitMode.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) Para obtener más información, vea Activar y desactivar la [retransmisión.](turning-retransmission-on-and-off.md)
-   Modifique el período de tiempo de espera y los valores de recuento de reintentos en la base de datos de la implementación. Para obtener más información, [vea Cambiar la directiva de retransmisión.](changing-the-retransmission-policy.md)
-   Llame a [**la función SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) para cancelar el ciclo de retransmisión y liberar las estructuras de datos internas asociadas a una única solicitud de mensaje SNMP. Para obtener más información, [vea Cancelar retransmisión.](canceling-retransmission.md)

La aplicación puede ejecutar su propia directiva de retransmisión. En este caso, la ejecución puede o no basarse en los valores de la base de datos.

 

 




