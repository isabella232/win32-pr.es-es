---
description: A los remitentes de PGM se les proporciona cierta configuración predeterminada que afecta al rendimiento de la transmisión de datos y cuánto tiempo se almacena en búfer los datos para tener en cuenta la pérdida de paquetes y las solicitudes de retransmisión de cliente PGM asociadas.
ms.assetid: 56b15eac-ea0d-4d18-b5f6-2f1a7b1bb25f
title: Opciones del remitente de PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04bce19e096f269207a22f8e3078643fefd9a7ced31482305c2caeb0ae8b7749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857915"
---
# <a name="pgm-sender-options"></a>Opciones del remitente de PGM

A los remitentes de PGM se les proporciona cierta configuración predeterminada que afecta al rendimiento de la transmisión de datos y cuánto tiempo se almacena en búfer los datos para tener en cuenta la pérdida de paquetes y las solicitudes de retransmisión de cliente PGM asociadas. En los párrafos siguientes se describe esta configuración predeterminada.

## <a name="window-size-and-transmission-rate"></a>Tamaño de ventana y velocidad de transmisión

La capacidad de establecer el tamaño de la ventana y la velocidad de transmisión permite a las aplicaciones controlar la cantidad de datos que los búferes de transporte van a transmitir y la velocidad a la que se transmite la secuencia de bytes.

Los datos de retransmisión se almacenan en un archivo, por lo que el tamaño máximo de la ventana está limitado por el espacio en disco que puede ser usado por el transporte. El tamaño predeterminado de la ventana es de 10 MB. Aunque es posible que un tamaño de envío o mensaje supere el tamaño de la ventana o búfer, el flujo de datos permanece ininterrumpido. el envío se envía hasta que se han enviado todos los datos.

> [!Note]  
> El espacio de búfer máximo está limitado por el número máximo de paquetes que se pueden almacenar en la ventana en un momento dado, que es igual a 2^31 – 1.

 

La velocidad de transmisión es el flujo de salida combinado de paquetes de datos originales (ODATA), paquetes de datos retransmitido (RDATA) y paquetes de contabilidad específicos del transporte (SPM), expresados por segundo. Si el límite de velocidad se establece en 56 kilobits por segundo de forma predeterminada. El tamaño predeterminado de la ventana es de 10 megabytes, con una velocidad predeterminada de 56 kilobits por segundo. Debido a la relación entre los tres miembros de la estructura [**RM \_ SEND \_ WINDOW,**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window) el tamaño predeterminado de la ventana es de 1428 segundos. Consulte **RM SEND WINDOW \_ \_ para** obtener más información.

## <a name="window-advance-rate"></a>Tasa de avance de ventana

La velocidad de avance de la ventana se establece mediante la opción de socket [RM \_ SENDER WINDOW \_ \_ ADV \_ RATE.](socket-options.md) Esta opción permite a las aplicaciones especificar el incremento en el que la ventana del remitente del PGM está avanzada, expresada como un valor de porcentaje distinto de cero del tamaño de la ventana. El valor predeterminado es 15 % y la tasa máxima es del 50 %. Si el remitente de PGM tiene pendientes los datos de reparación que se encuentra en el espacio de la ventana de incremento, la ventana se avanza parcialmente a medida que se envía cada paquete de reparación de la ventana.

## <a name="forward-error-correction-fec"></a>Corrección de errores de reenvío (FEC)

La corrección de errores hacia delante se establece mediante el uso de la \_ opción de socket RM USE \_ FEC. Esta opción de socket permite al remitente de PGM enviar paquetes de reparación como paquetes de paridad en lugar de paquetes de datos normales. Al hacerlo, se minimiza el número de paquetes de reparación enviados para reparar distintas secuencias perdidas por varios receptores del mismo grupo de datos. La habilitación de FEC solo se establece en el remitente de PGM. Los receptores PGM siguen automáticamente la directiva establecida por el remitente. Para obtener una explicación detallada sobre FEC, consulte la RFC de PGM que se encuentra en el [sitio web de IETF.](https://www.ietf.org/)

 

 



