---
description: Compatibilidad con extensiones MTP
ms.assetid: 9e5f3da6-346a-4eca-bc85-2755c569986d
title: Compatibilidad con extensiones MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6a5a585167984ec944528bb74a6746e42ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912142"
---
# <a name="supporting-mtp-extensions"></a>Compatibilidad con extensiones MTP

## <a name="media-transfer-protocol"></a>Protocolo de transferencia de medios

El protocolo de transferencia multimedia (MTP) es una extensión del Protocolo de transferencia de imágenes (PTP). Como resultado, todas las semánticas del protocolo PTP son válidas en MTP.

MTP se comunica mediante el uso de comandos y respuestas entre dos partes, el iniciador y el respondedor. Los roles de los dispositivos implicados están claramente definidos. El equipo es normalmente el iniciador y el dispositivo siempre es el respondedor. Un dispositivo que no es PC también podría ser un iniciador (por ejemplo, una baraja de coches o un cuadro X de Microsoft). Un dispositivo nunca puede asumir ambos roles al mismo tiempo.

El iniciador inicia la comunicación enviando un comando al respondedor. El respondedor procesa el comando y devuelve una respuesta adecuada. Puede haber una fase de datos asociada con el comando. En este caso, la dirección del flujo de datos se debe conocer de antemano y el iniciador y el contestador lo aceptan. Tenga en cuenta que no hay un encabezado descriptivo que indique los flujos de datos para los nuevos comandos.

El respondedor puede iniciar la comunicación independientemente del iniciador. Por ejemplo, el respondedor puede enviar eventos al iniciador. Sin embargo, no se pueden enviar datos junto con el evento. Si hay datos que deben leerse como parte del evento, el iniciador debe enviar un comando MTP y el dispositivo puede enviar datos como respuesta al comando.

Para obtener una descripción completa de MTP, consulte la [especificación de MTP](https://www.usb.org/sites/default/files/MTPv1_1.zip).

## <a name="sending-mtp-commands"></a>Envío de comandos MTP

Las aplicaciones pueden enviar comandos MTP a un dispositivo mediante la invocación del método [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) . El comando que se envía depende de si hay una fase de datos y de si los datos adjuntos se leen o se escriben en el dispositivo. En la tabla siguiente se describen los tres comandos de extensión MTP posibles.

Tenga en cuenta que estos comandos son específicos de MTP; y, por tanto, solo se implementan mediante el controlador de clase MTP de WPD.



|                                                                                                                                      |                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Get-Help                                                                                                                              | Descripción                                                                                       |
| [**comando de WPD \_ \_ transferencia de \_ \_ datos de finalización ext \_ \_**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-end-data-transfer)                                      | Emite un comando MTP que indica la finalización de una operación de lectura o escritura de datos.              |
| [**comando de WPD ext comando de ejecución de comandos de WPD \_ \_ \_ \_ \_ \_ sin \_ fase de datos \_**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-without-data-phase)  | Emite un comando MTP sin una fase de datos correspondiente.                                         |
| [**comando de WPD \_ \_ \_ ext \_ comando de ejecución MTP \_ \_ con \_ datos \_ para \_ escribir**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) | Emite un comando MTP seguido de los datos que lo acompañan, que se escribirán en el dispositivo. |
| [**comando de WPD \_ comando \_ \_ ext \_ Execute \_ \_ con \_ datos \_ para \_ leer**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read)   | Emite un comando MTP seguido de los datos que lo acompañan, que se lee desde el dispositivo.       |
| [**comando de WPD \_ \_ \_ datos de \_ lectura ext \_**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-read-data)                                                       | Emite un comando MTP que envía datos del dispositivo al equipo.                                  |
| [**comando de WPD \_ \_ \_ datos de escritura ext MTP \_ \_**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-write-data)                                                     | Emite un comando MTP que envía datos al dispositivo desde el equipo.                                  |



 

Independientemente de la fase, se deben especificar los **\_ \_ \_ \_ \_ parámetros** de operación **ext ext de la propiedad WPD y el \_ \_ \_ \_ \_ código de operación ext** de la propiedad WPD.

Si el controlador MTP pudo enviar el comando al dispositivo, los valores devueltos contendrán siempre **el \_ \_ código de \_ \_ respuesta ext \_ MTP de la propiedad WPD**. Si el código de respuesta indica que se ha realizado correctamente y la semántica del comando permite parámetros de respuesta, también estarán disponibles los parámetros de **\_ \_ \_ \_ \_ respuesta ext ext de la propiedad WPD** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 
