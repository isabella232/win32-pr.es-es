---
description: Las características multimedia son diferentes con TAPI 2,2 (TAPI/C) en lugar de TAPI 3 (COM), en gran medida porque la API COM tiene acceso a los proveedores de servicios multimedia (MSP).
ms.assetid: 73042eb1-b2d6-4dcb-b40e-f8f3933dcdb0
title: Acceso a medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb3fe361aab9d5b5c9897deb5ea36d6e85adcfd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279814"
---
# <a name="media-access"></a>Acceso a medios

Las características multimedia son diferentes con TAPI 2,2 (TAPI/C) en lugar de TAPI 3 (COM), en gran medida porque la API COM tiene acceso a los proveedores de servicios multimedia (MSP). Para obtener más información acerca de los MSP, consulte [acerca del proveedor de servicios multimedia (MSP)](./about-the-media-service-provider-msp-.md). Para obtener más información sobre las operaciones de streaming multimedia, vea [control multimedia](./device-control.md).

Los dos conceptos más importantes para una aplicación son el tipo de medio (o el modo) y el flujo. El tipo es el formulario en el que se transmiten los datos. Para obtener más información y una lista de tipos definidos por TAPI, [vea \_ constantes LINEMEDIAMODE](linemediamode--constants.md). El flujo multimedia es la secuencia de datos real. Un MSP puede proporcionar acceso directo a la secuencia. Las aplicaciones TAPI 2,2 tienen algún acceso, pero principalmente hacen referencia a otras API para implementar tales controles.

Estas API incluyen la API de la interonda, la API de comunicaciones y la interfaz de control de medios (MCI). La API de forma de onda se usa para la programación multimedia, la API de COMM es el conjunto de funciones de comunicaciones proporcionadas por el kit de desarrollo de software (SDK) de la plataforma, y el MCI proporciona una interfaz generalizada de alto nivel para controlar los dispositivos multimedia.

Por ejemplo, en el caso de los dispositivos de línea, una aplicación puede usar TAPI 2,2 para establecer una conexión a otra estación. Una vez establecida la conexión, la aplicación puede usar la API de forma de onda (o la API WaveAudio de MCI) en el dispositivo asociado para reproducir (enviar) y grabar (recibir) datos de audio a través de la conexión. Del mismo modo, si la secuencia de medios de conexión procede de un módem, una aplicación usaría las extensiones de configuración del módem de la API de comunicaciones para controlar el flujo multimedia.

Para proporcionar TAPI 2,2 con acceso de flujo de medios a un teléfono o una llamada en un dispositivo de línea, el proveedor de servicios debe implementar tanto el SPI de telefonía como el SPI de flujo de medios adecuado o la interfaz de controlador de dispositivo (DDI). El proveedor de servicios puede admitir líneas y teléfonos simultáneamente.

Dado que estas clases de dispositivos y operaciones de flujo multimedia funcionan de forma independiente entre sí, la coordinación de su uso debe realizarse en el nivel de la aplicación. Es probable que varias aplicaciones que compartan llamadas y flujos multimedia requieran la coordinación de sus actividades en el nivel de aplicación para evitar el uso en conflicto de TAPI y la API de streaming multimedia.

TAPI informa de los cambios en el tipo de flujo multimedia (voz, fax, módem de datos, etc.) a las aplicaciones participantes. Este proceso se conoce a veces como [*clasificación de llamadas*](c-tapgloss.md). El mecanismo que se usa para determinar el tipo de flujo multimedia es específico del proveedor de servicios. Por ejemplo, un proveedor de servicios puede filtrar el flujo multimedia para la energía o los tonos que caracterizan el tipo de medio, o puede usar timbres distintivos, datos intercambiados en mensajes a través de la red o conocimiento sobre el llamador o identificador para tomar esta determinación.

-   [Supervisión de llamadas](call-monitoring.md)
-   [Control multimedia](/previous-versions/windows/desktop/legacy/ms736578(v=vs.85))
-   [Recopilación de dígitos](digit-gathering.md)
-   [Generar dígitos y tonos en banda](generating-inband-digits-and-tones.md)

 

 
