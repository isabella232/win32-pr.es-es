---
description: Los remitentes de PGM se proporcionan con ciertas configuraciones predeterminadas que afectan al rendimiento de la transmisión de datos y a cuánto tiempo se almacenan en búfer los datos para tener en cuenta la pérdida de paquetes y las solicitudes de retransmisión de cliente PGM asociadas.
ms.assetid: 56b15eac-ea0d-4d18-b5f6-2f1a7b1bb25f
title: Opciones del remitente de PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c2e83ec7b098b9a82f74d4a3e0b6aa3ab03b63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705598"
---
# <a name="pgm-sender-options"></a>Opciones del remitente de PGM

Los remitentes de PGM se proporcionan con ciertas configuraciones predeterminadas que afectan al rendimiento de la transmisión de datos y a cuánto tiempo se almacenan en búfer los datos para tener en cuenta la pérdida de paquetes y las solicitudes de retransmisión de cliente PGM asociadas. En los párrafos siguientes se describen estos valores predeterminados.

## <a name="window-size-and-transmission-rate"></a>Velocidad de transmisión y tamaño de la ventana

La capacidad de establecer el tamaño de la ventana y la velocidad de transmisión permite a las aplicaciones controlar la cantidad de datos que los búferes de transporte para la retransmisión y la velocidad a la que se transmite la secuencia de bytes.

Los datos de retransmisión se almacenan en un archivo, por lo que el tamaño máximo de la ventana está limitado por el espacio en disco que puede usar el transporte. El tamaño de ventana predeterminado es 10 MB. Aunque es posible que el tamaño de un mensaje o envío supere el tamaño de la ventana o del búfer, el flujo de datos permanece ininterrumpido. el envío queda pendiente hasta que se envíen todos los datos.

> [!Note]  
> El espacio de búfer máximo está limitado por el número máximo de paquetes que se pueden mantener en la ventana en un momento dado, que es igual a 2 ^ 31 – 1.

 

La velocidad de transmisión es el flujo de salida combinado de paquetes de datos originales (ODATA), paquetes de datos retransmitidos (RDATA) y paquetes de contabilidad específicos de transporte (SPMs), expresados por segundo. De forma predeterminada, si el límite de velocidad se establece en 56 kilobits por segundo. El tamaño predeterminado de la ventana es de 10 megabytes, con una velocidad predeterminada de 56 kilobits por segundo. Debido a la relación entre los tres miembros de la estructura de la [**\_ \_ ventana de envío de RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window) , el tamaño predeterminado de la ventana es, por lo tanto, de 1428 segundos. Para obtener más información, vea **\_ \_ ventana de envío de RM** .

## <a name="window-advance-rate"></a>Tasa de avance de ventana

La tasa de avance de la ventana se establece mediante la opción de socket de [ \_ \_ \_ \_ velocidad avanzada](socket-options.md) de la ventana del remitente de RM. Esta opción permite a las aplicaciones especificar el incremento en el que la ventana del remitente PGM está avanzada, expresada como un valor porcentual distinto de cero del tamaño de la ventana. El valor predeterminado es 15% y la velocidad máxima es 50%. Si el remitente PGM tiene datos de reparación pendientes que se encuentran en el espacio de la ventana de incremento, la ventana se adelantará parcialmente, ya que cada paquete de reparación de la ventana se envía.

## <a name="forward-error-correction-fec"></a>Corrección de errores de reenvío (FEC)

La corrección de errores de reenvío se establece mediante el uso de la opción de socket de FEC de uso de RM \_ \_ . Esta opción de socket permite al remitente de PGM enviar paquetes de reparación como paquetes de paridad en lugar de paquetes de datos normales. Al hacerlo, se minimiza el número de paquetes de reparación enviados para reparar diferentes secuencias perdidas por varios receptores desde dentro del mismo grupo de datos. La habilitación de FEC solo se establece en el remitente PGM. Los receptores de PGM siguen automáticamente la directiva establecida por el remitente. Para obtener información detallada sobre FEC, consulte la RFC de PGM que se encuentra en el sitio web de [IETF](https://www.ietf.org/) .

 

 



