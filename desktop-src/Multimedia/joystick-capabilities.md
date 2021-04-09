---
title: Funcionalidades del joystick
description: Funcionalidades del joystick
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- entrada multimedia, joysticks
- joysticks, movimiento de dos ejes
- joysticks, movimiento de tres ejes
- joysticks, botones
- joysticks, intervalos de movimiento
- joysticks, frecuencias de sondeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791188"
---
# <a name="joystick-capabilities"></a>Funcionalidades del joystick

Los joysticks pueden admitir el movimiento de dos o tres ejes y hasta cuatro botones. Los joysticks también admiten diferentes *intervalos de frecuencias de movimiento* y *sondeo*. El intervalo de movimiento es la distancia que un controlador de joystick puede pasar de su posición de colocación a la posición más alejada de su posición de descanso. La frecuencia de sondeo es el intervalo de tiempo entre las consultas de joystick.

Los controladores de joystick pueden admitir uno o dos joysticks. Puede determinar el número de joysticks admitidos por un controlador de joystick mediante la función [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) . Esta función devuelve un entero sin signo que contiene el número de joysticks admitidos o cero si no hay compatibilidad con el joystick. El valor devuelto no indica el número de joysticks conectados al sistema.

Puede determinar si un joystick está conectado al sistema mediante la función [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) . Esta función devuelve JOYERR \_ NoError si se adjunta el dispositivo especificado. De lo contrario, devuelve JOYERR \_ UNenchufado.

Cada joystick tiene varias funciones que están disponibles para la aplicación. Puede recuperar las capacidades de un joystick mediante la función [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) . Esta función rellena una estructura [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) con funciones de joystick como los valores mínimo y máximo de su sistema de coordenadas, el número de botones del joystick y las frecuencias de sondeo mínima y máxima.

 

 