---
title: Mezcladores de audio en Windows Vista
description: Mezcladores de audio en Windows Vista
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- audio multimedia, Windows mezcladores de audio de Vista
- audio,Windows mezcladores de audio de Vista
- mezcladores de audio, Windows Vista
- mixers,Windows Vista
- Windows Mezcladores de audio de Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4299a7c4d1dcbc3fa5d92e4bb18042793976dafac4e836f80ac5c70ac53f09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989605"
---
# <a name="audio-mixers-in-windows-vista"></a>Mezcladores de audio en Windows Vista

A partir Windows Vista, algunos controles mezcladores se implementan en software en lugar de hardware. Por ejemplo, los controles de volumen se implementan mediante la API Windows sesión de audio (WASAPI). Estos controles no afectan directamente a la configuración de hardware. Además, están asociados a una sesión de audio específica del proceso, por lo que los cambios afectan a la aplicación que realiza la llamada, pero no afectan a otras aplicaciones.

Cada dispositivo de punto de conexión de audio tiene un diseño mezclador estándar, implementado en software.

-   Cada punto de conexión de representación de audio contiene una línea de destino que contiene lo siguiente:
    -   Control de volumen
    -   Control de exclusión mutua
    -   Línea de origen: salida de audio de forma de onda.
    -   Línea de origen: CD de audio.
-   Cada punto de conexión de captura de audio contiene una línea de destino que contiene lo siguiente:
    -   Control de volumen
    -   Control de exclusión mutua
    -   Línea de origen: entrada de audio de forma de onda. El tipo de componente depende del dispositivo de entrada, por ejemplo, un micrófono.

Cada línea de código fuente contiene un control de volumen y un control de exclusión mutua. En el diagrama siguiente se muestran los componentes de los puntos de conexión de representación y de captura.

![diseños de mezclador predeterminados](images/mixer1.gif)

Todos los controles de un punto de conexión manipulan el mismo control de software subyacente. Por lo tanto, si cambia la configuración de un control, recibirá una notificación de cambio de control en los demás controles. (Vea [**MM \_ MIXM CONTROL \_ \_ CHANGE**](mm-mixm-control-change.md)).

Este diseño estándar se proporciona por compatibilidad con las aplicaciones existentes que usan las funciones mezcladoras de audio. Las nuevas aplicaciones deben evitar el uso de estas funciones.

 

 




