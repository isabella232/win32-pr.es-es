---
title: Mezcladores de audio en Windows Vista
description: Mezcladores de audio en Windows Vista
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- audio multimedia, mezcladores de audio de Windows Vista
- audio, mezcladores de audio de Windows Vista
- Mezcladores de audio, Windows Vista
- mezcladores, Windows Vista
- Mezcladores de audio de Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0610e9f16e13c19a253fbd9f6fac5ef452fa68ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104555495"
---
# <a name="audio-mixers-in-windows-vista"></a>Mezcladores de audio en Windows Vista

A partir de Windows Vista, algunos controles de mezclador se implementan en software en lugar de hardware. Por ejemplo, los controles de volumen se implementan mediante la API de sesión de audio de Windows (WASAPI). Estos controles no afectan directamente a la configuración de hardware. Además, están asociados a una sesión de audio específica del proceso, por lo que los cambios afectan a la aplicación que realiza la llamada, pero no afectan a otras aplicaciones.

Cada dispositivo de punto de conexión de audio tiene un diseño de mezclador estándar, que se implementa en software.

-   Cada extremo de representación de audio contiene una línea de destino que contiene lo siguiente:
    -   Control de volumen
    -   Silenciar control
    -   Línea de código fuente: de onda-salida de audio.
    -   Línea de código fuente: CD de audio.
-   Cada extremo de captura de audio contiene una línea de destino que contiene lo siguiente:
    -   Control de volumen
    -   Silenciar control
    -   Línea de código fuente: onda de entrada de audio. El tipo de componente depende del dispositivo de entrada, por ejemplo, un micrófono.

Cada línea de código fuente contiene un control de volumen y un control de silencio. En el diagrama siguiente se muestran los componentes de los extremos de representación y de captura.

![diseños de mezclador predeterminados](images/mixer1.gif)

Todos los controles de un extremo manipulan el mismo control de software subyacente. Por lo tanto, si cambia la configuración de un control, recibirá una notificación de cambio de control en los otros controles. (Vea [**el \_ \_ \_ cambio de control mm MIXM**](mm-mixm-control-change.md)).

Este diseño estándar se proporciona por compatibilidad con las aplicaciones existentes que utilizan las funciones del mezclador de audio. Las nuevas aplicaciones deben evitar el uso de estas funciones.

 

 




