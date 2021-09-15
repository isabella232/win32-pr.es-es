---
title: Apertura y cierre de Mixer dispositivos
description: Apertura y cierre de Mixer dispositivos
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- audio multimedia, abrir dispositivos mezcladores
- audio, abrir dispositivos mezcladores
- mezcladores de audio, apertura
- mezcladores, abrir
- audio multimedia, cerrar dispositivos mezcladores
- audio, cerrar dispositivos mezcladores
- mezcladores de audio, cerrar
- mixers,closing
- abrir dispositivos mezcladores
- cerrar dispositivos mezcladores
- identificadores de dispositivo frente a identificadores de dispositivo
- mezcladores de audio, identificadores de dispositivo frente a identificadores de dispositivo
- mezcladores, identificadores de dispositivo frente a identificadores de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2be7fcc0563508aabfd957109d62c7dbfe1c1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476782"
---
# <a name="opening-and-closing-mixer-devices"></a>Apertura y cierre de Mixer dispositivos

Si desea usar un dispositivo mezclador, puede empezar a usarlo simplemente o puede abrirlo explícitamente antes de usarlo. La apertura explícita de un dispositivo mezclador ofrece dos ventajas principales:

-   Garantiza la existencia continua de ese dispositivo mezclador.
-   Le permite recibir notificaciones de la línea de audio y controlar los cambios.

Puede usar la función [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) para abrir explícitamente un dispositivo mezclador. Esta función toma como parámetros un identificador de dispositivo, un puntero a una ubicación de memoria y otros valores únicos para cada tipo de dispositivo. La ubicación de memoria se rellena con un identificador de dispositivo. Use este identificador de dispositivo para identificar el dispositivo mezclador abierto al llamar a otras funciones de mezclador de audio. Mientras exista un identificador de un dispositivo mezclador, el dispositivo seguirá existiendo en el sistema. Si se produce un cambio de configuración en el dispositivo mezclador y no se ha abierto explícitamente, es posible que la aplicación no pueda acceder a él de repente.

> [!Note]  
> La diferencia entre los identificadores de dispositivo y los identificadores de dispositivo es importante. Los identificadores de dispositivo se devuelven cuando se abre un controlador de dispositivo mediante **mezcladorAbrir**. Los identificadores de dispositivo se determinan implícitamente a partir del número de dispositivos presentes en un sistema; Este número se obtiene mediante la [**función mixerGetNumDevs.**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

 

Puede usar la función [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) para cerrar un dispositivo mezclador. Debe cerrar el dispositivo una vez que termine de usarlo.

 

 