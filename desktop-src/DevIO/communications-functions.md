---
description: Las siguientes funciones se usan con recursos de comunicaciones.
ms.assetid: ba7d1a9e-6906-4923-a8eb-db58050ba699
title: Funciones de comunicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64853bf2b0c42d4e7ca607fbbe624995cfe1a249
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164521"
---
# <a name="communications-functions"></a>Funciones de comunicaciones

Las siguientes funciones se usan con recursos de comunicaciones.



| Función                                                   | Descripción                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**BuildCommDCB**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba)                       | Rellena una estructura [**DCB especificada**](/windows/desktop/api/Winbase/ns-winbase-dcb) con los valores especificados en una cadena de control de dispositivo.                           |
| [**BuildCommDCBAndTimeouts**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcbandtimeoutsa) | Convierte una cadena de definición de dispositivo en códigos de bloque de control de dispositivo adecuados y los coloca en un bloque de control de dispositivo. |
| [**ClearCommBreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak)                   | Restaura la transmisión de caracteres para un dispositivo de comunicaciones especificado y coloca la línea de transmisión en un estado nobreak.    |
| [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror)                   | Recupera información sobre un error de comunicaciones e informa del estado actual de un dispositivo de comunicaciones.                  |
| [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga)               | Muestra un cuadro de diálogo de configuración proporcionado por el controlador.                                                                           |
| [**EscapeCommFunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction)           | Indica a un dispositivo de comunicaciones especificado que realice una función extendida.                                                     |
| [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig)                     | Recupera la configuración actual de un dispositivo de comunicaciones.                                                                |
| [**GetCommMask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask)                         | Recupera el valor de la máscara de eventos para un dispositivo de comunicaciones especificado.                                                   |
| [**GetCommModemStatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus)           | Recupera los valores de registro de control de módem.                                                                                       |
| [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties)             | Recupera información sobre las propiedades de comunicaciones de un dispositivo de comunicaciones especificado.                               |
| [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate)                       | Recupera la configuración de control actual para un dispositivo de comunicaciones especificado.                                                  |
| [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts)                 | Recupera los parámetros de tiempo de espera para todas las operaciones de lectura y escritura en un dispositivo de comunicaciones especificado.                      |
| [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga)       | Recupera la configuración predeterminada para el dispositivo de comunicaciones especificado.                                                   |
| [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm)                             | Descarta todos los caracteres del búfer de salida o entrada de un recurso de comunicaciones especificado.                                |
| [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak)                       | Suspende la transmisión de caracteres para un dispositivo de comunicaciones especificado y coloca la línea de transmisión en un estado de interrupción.       |
| [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig)                     | Establece la configuración actual de un dispositivo de comunicaciones.                                                                     |
| [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask)                         | Especifica un conjunto de eventos que se supervisarán para un dispositivo de comunicaciones.                                                         |
| [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate)                       | Configura un dispositivo de comunicaciones según las especificaciones de un bloque de control de dispositivo.                                  |
| [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts)                 | Establece los parámetros de tiempo de espera para todas las operaciones de lectura y escritura en un dispositivo de comunicaciones especificado.                           |
| [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga)       | Establece la configuración predeterminada para un dispositivo de comunicaciones.                                                                    |
| [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm)                             | Inicializa los parámetros de comunicaciones para un dispositivo de comunicaciones especificado.                                               |
| [**TransmitCommChar**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar)               | Transmite un carácter especificado delante de los datos pendientes en el búfer de salida del dispositivo de comunicaciones especificado.         |
| [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent)                     | Espera a que se produzca un evento para un dispositivo de comunicaciones especificado.                                                             |



 

 

 



