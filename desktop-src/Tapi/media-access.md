---
description: Las características multimedia son diferentes con TAPI 2.2 (TAPI/C) en lugar de TAPI 3 (COM), en gran medida porque la API COM tiene acceso a proveedores de servicios multimedia (MSP).
ms.assetid: 73042eb1-b2d6-4dcb-b40e-f8f3933dcdb0
title: Acceso a medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f2fc67e18a85718a10a0489656d4b423dd2f9f849a876ea5eec0543017611f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575615"
---
# <a name="media-access"></a>Acceso a medios

Las características multimedia son diferentes con TAPI 2.2 (TAPI/C) en lugar de TAPI 3 (COM), en gran medida porque la API COM tiene acceso a proveedores de servicios multimedia (MSP). Para obtener más información sobre los MSP, vea [Acerca del proveedor de Media Service (MSP).](./about-the-media-service-provider-msp-.md) Para obtener más información sobre las operaciones de flujo multimedia, vea [Control multimedia](./device-control.md).

Los dos conceptos más importantes de una aplicación son el tipo de medio (o modo) y la secuencia. El tipo es el formulario en el que se transmiten los datos. Para obtener más información y una lista de tipos definidos por TAPI, vea [LINEMEDIAMODE \_ Constants](linemediamode--constants.md). El flujo multimedia es el flujo de datos real. Un MSP puede proporcionar acceso directo a la secuencia. Las aplicaciones TAPI 2.2 tienen cierto acceso, pero hacen referencia principalmente a otras API para implementar estos controles.

Estas API incluyen la API de forma de onda, la API comm y la interfaz de control multimedia (MCI). La API de forma de onda se usa para la programación multimedia, la API de Comm es el conjunto de funciones de comunicaciones proporcionadas por el Kit de desarrollo de software de plataforma (SDK) y MCI proporciona una interfaz generalizada de alto nivel para controlar los dispositivos multimedia.

Por ejemplo, para los dispositivos de línea, una aplicación puede usar TAPI 2.2 para establecer una conexión a otra estación. Una vez establecida la conexión, la aplicación puede usar la API de forma de onda (o MCI Waveaudio API) en el dispositivo asociado para reproducir (enviar) y grabar (recibir) datos de audio a través de la conexión. De forma similar, si el flujo multimedia de conexión es de un módem, una aplicación usaría las extensiones de configuración de módem de Communications API para controlar el flujo multimedia.

Para proporcionar a TAPI 2.2 acceso de secuencia multimedia a un teléfono o a una llamada en un dispositivo de línea, el proveedor de servicios debe implementar tanto el SPI de telefonía como el SPI de flujo multimedia adecuado o la interfaz de controlador de dispositivo (DDI). El proveedor de servicios puede admitir líneas y teléfonos simultáneamente.

Dado que estas clases de dispositivo y las operaciones de flujo multimedia funcionan de forma independiente entre sí, la coordinación de su uso debe producirse en el nivel de aplicación. Es probable que varias aplicaciones que comparten llamadas y secuencias multimedia requieran la coordinación de sus actividades en el nivel de aplicación para evitar el uso en conflicto de TAPI y la API de flujo multimedia.

TAPI notifica los cambios en el tipo de flujo multimedia (voz, fax, módem de datos, entre otros) a las aplicaciones participantes. Este proceso se conoce a veces como clasificación [*de llamadas*](c-tapgloss.md). El mecanismo utilizado para determinar el tipo de flujo multimedia es específico del proveedor de servicios. Por ejemplo, un proveedor de servicios puede filtrar el flujo multimedia para la energía o los tonos que caracterizan el tipo de medio, o puede usar un anillo distintivo, datos intercambiados en mensajes a través de la red o conocimientos sobre el autor de la llamada o el identificador llamado para realizar esta determinación.

-   [Supervisión de llamadas](call-monitoring.md)
-   [Control multimedia](/previous-versions/windows/desktop/legacy/ms736578(v=vs.85))
-   [Recopilación de dígitos](digit-gathering.md)
-   [Generación de dígitos y tonos de banda](generating-inband-digits-and-tones.md)

 

 
