---
description: Compatibilidad con extensiones MTP
ms.assetid: 9e5f3da6-346a-4eca-bc85-2755c569986d
title: Compatibilidad con extensiones MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16a80b640b50346f1724aec771d8ffd82de565f078e5b3e1d562c346e34973a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193576"
---
# <a name="supporting-mtp-extensions"></a>Compatibilidad con extensiones MTP

## <a name="media-transfer-protocol"></a>Protocolo de transferencia de medios

El Protocolo de transferencia de medios (MTP) es una extensión del Protocolo de transferencia de imágenes (PTP). Como resultado, toda la semántica del protocolo PTP es válida en MTP.

MTP se comunica mediante comandos y respuestas entre dos partes, el iniciador y el respondedor. Los roles de los dispositivos implicados están muy claramente definidos. El equipo suele ser el iniciador y el dispositivo siempre es el respondedor. Un dispositivo que no es de PC también podría ser un iniciador (por ejemplo, una baraja de automóviles o una caja X de Microsoft). Un dispositivo nunca puede asumir ambos roles al mismo tiempo.

El iniciador inicia la comunicación mediante el envío de un comando al respondedor. El respondedor procesa el comando y devuelve una respuesta adecuada. Puede haber una fase de datos asociada al comando . Si este es el caso, la dirección del flujo de datos debe conocerse de antemano y ser aceptada tanto por el iniciador como por el respondedor. Tenga en cuenta que no hay un encabezado descriptivo que indique los flujos de datos para los nuevos comandos.

El respondedor puede iniciar la comunicación independientemente del iniciador. Por ejemplo, el respondedor puede enviar eventos al iniciador. Sin embargo, no se puede enviar ningún dato junto con el evento . Si hay algún dato que deba leerse como parte del evento, el iniciador debe enviar un comando MTP y, a continuación, el dispositivo puede enviar datos en respuesta al comando.

Para obtener una descripción completa de MTP, consulte la [especificación de MTP](https://www.usb.org/sites/default/files/MTPv1_1.zip).

## <a name="sending-mtp-commands"></a>Envío de comandos MTP

Las aplicaciones pueden enviar comandos MTP a un dispositivo invocando el [**método IPortableDevice::SendCommand.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) El comando que se envía depende de si hay una fase de datos y de si los datos adjuntos se leen o escriben en el dispositivo. En la tabla siguiente se describen los tres posibles comandos de extensión MTP.

Tenga en cuenta que estos comandos son específicos de MTP; y, por lo tanto, solo se implementan mediante el controlador de clase MTP de WPD.



| Get-Help  | Descripción  |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**TRANSFERENCIA DE DATOS \_ FINALES \_ EXT DEL COMANDO WPD MTP \_ \_ \_ \_**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-end-data-transfer)                                      | Emite un comando MTP que indica la conclusión de una operación de lectura o escritura de datos.              |
| [**COMANDO WPD \_ \_ MTP \_ EXT EXECUTE COMMAND WITHOUT DATA \_ \_ \_ \_ \_ PHASE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-without-data-phase)  | Emite un comando MTP sin una fase de datos correspondiente.                                         |
| [**COMANDO WPD \_ \_ MTP EXT EXECUTE COMMAND WITH DATA TO WRITE (COMANDO MTP EXT EXECUTE DE WPD \_ \_ CON DATOS PARA \_ \_ \_ \_ \_ ESCRIBIR)**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) | Emite un comando MTP que va seguido de los datos adjuntos, que se escribirán en el dispositivo. |
| [**COMANDO WPD \_ \_ MTP EXT EXECUTE COMMAND WITH DATA TO READ (COMANDO MTP EXT EXECUTE DE WPD \_ \_ CON DATOS PARA \_ \_ \_ \_ \_ LEER)**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read)   | Emite un comando MTP que va seguido de los datos adjuntos, que se leen desde el dispositivo.       |
| [**COMANDO WPD \_ \_ MTP \_ EXT READ \_ \_ DATA**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-read-data)                                                       | Emite un comando MTP que envía datos desde el dispositivo al equipo.                                  |
| [**COMANDO WPD \_ \_ MTP \_ EXT WRITE \_ \_ DATA**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-write-data)                                                     | Emite un comando MTP que envía datos al dispositivo desde el equipo.                                  |



 

Independientemente de la fase, se deben especificar **WPD \_ PROPERTY \_ MTP \_ EXT OPERATION \_ \_ CODE** y **WPD PROPERTY \_ \_ MTP EXT OPERATION \_ \_ \_ PARAMS.**

Si el controlador MTP pudo enviar el comando al dispositivo, los valores devueltos siempre contendrán **WPD \_ PROPERTY \_ MTP \_ EXT RESPONSE \_ \_ CODE**. Si el código de respuesta indica correcto y la semántica del comando permite parámetros de respuesta, **WPD \_ PROPERTY \_ MTP \_ EXT RESPONSE \_ \_ PARAMS** también estará disponible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 
