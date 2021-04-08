---
description: La compatibilidad con dispositivos telefónicos es complementaria en lugar de básica, por lo que no es necesario que los proveedores de servicios admitan dispositivos telefónicos.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Dispositivos telefónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f406442e43d8d4f31a89bfc0ccb1e59916d33e0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001316"
---
# <a name="phone-devices"></a>Dispositivos telefónicos

La compatibilidad con dispositivos telefónicos es complementaria en lugar de básica, por lo que no es necesario que los proveedores de servicios admitan dispositivos telefónicos.

Del mismo modo que una clase de dispositivo de línea es una abstracción de un dispositivo de línea física, la clase de dispositivo telefónico representa una abstracción independiente del dispositivo de un juego de teléfono. TAPI trata los dispositivos de línea y teléfono como dispositivos que son independientes entre sí. En otras palabras, puede usar un teléfono (dispositivo) sin usar una línea asociada, y puede usar una línea (dispositivo) sin usar un teléfono.

Los proveedores de servicios que implementan totalmente esta independencia pueden ofrecer usos para estos dispositivos no definidos por los protocolos de telefonía tradicionales. Por ejemplo, una persona puede usar el auricular del teléfono del escritorio como dispositivo de audio de forma de onda para grabar o reproducir voz, quizás sin la información del conmutador de que el teléfono está en uso. En este tipo de implementación, levantar el auricular del teléfono local no debe enviar automáticamente una señal OffHook al conmutador.

Esta independencia también permite que una aplicación suene el teléfono local de forma independiente de las llamadas entrantes. Las capacidades de los proveedores de servicios están limitadas por las capacidades del hardware y el software que se usan para interconectar el conmutador, el teléfono y el equipo.

TAPI incluye funciones para recuperar funciones del dispositivo que permiten a los clientes determinar si se admite dicho modelo de uso.

En esta sección se describen los dispositivos telefónicos y se explica cómo usar las funciones de teléfono TAPI para tener acceso a estos dispositivos.

-   [Dispositivo telefónico](phone-device-elements.md)
-   [Inicialización y apagado](initialization-and-shutdown.md)

 

 



