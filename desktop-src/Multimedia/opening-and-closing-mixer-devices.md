---
title: Abrir y cerrar dispositivos de mezclador
description: Abrir y cerrar dispositivos de mezclador
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- audio multimedia, dispositivos de mezclador de apertura
- audio, abrir dispositivos de mezclador
- Mezcladores de audio, abrir
- mezcladores, abrir
- audio multimedia, dispositivos de mezclador de cierre
- audio, cerrar dispositivos de mezclador
- Mezcladores de audio, cerrar
- mezcladores, cerrar
- abrir dispositivos de mezclador
- cerrar dispositivos de mezclador
- identificadores de dispositivo frente a identificadores de dispositivo
- Mezcladores de audio, identificadores de dispositivo y controladores de dispositivo
- mezcladores, identificadores de dispositivo frente a manipuladores de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2be7fcc0563508aabfd957109d62c7dbfe1c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077600"
---
# <a name="opening-and-closing-mixer-devices"></a>Abrir y cerrar dispositivos de mezclador

Si desea usar un dispositivo de mezclador, puede empezar a usarlo o bien puede abrirlo explícitamente antes de usarlo. Abrir explícitamente un dispositivo de mezclador ofrece dos ventajas principales:

-   Garantiza la existencia continua de ese dispositivo de mezclador.
-   Le permite recibir una notificación de los cambios de línea y control de audio.

Puede usar la función [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) para abrir explícitamente un dispositivo de mezclador. Esta función toma como parámetros un identificador de dispositivo, un puntero a una ubicación de memoria y otros valores exclusivos de cada tipo de dispositivo. La ubicación de memoria se rellena con un identificador de dispositivo. Use este identificador de dispositivo para identificar el dispositivo de mezclador abierto al llamar a otras funciones del mezclador de audio. Siempre que exista un identificador de dispositivo de mezclador, el dispositivo seguirá existiendo en el sistema. Si se produce un cambio de configuración en el dispositivo de mezclador y no se ha abierto explícitamente, es posible que la aplicación no pueda acceder a él de repente.

> [!Note]  
> La diferencia entre los identificadores de dispositivo y los controladores de dispositivo es importante. Los identificadores de dispositivo se devuelven cuando se abre un controlador de dispositivo mediante **mixerOpen**. Los identificadores de dispositivo se determinan implícitamente a partir del número de dispositivos presentes en un sistema; Este número se obtiene mediante la función [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) .

 

Puede usar la función [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) para cerrar un dispositivo de mezclador. Debe cerrar el dispositivo cuando termine de usarlo.

 

 