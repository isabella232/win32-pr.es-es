---
title: Funcionalidades de los juegos
description: Funcionalidades de los juegos
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- entrada multimedia, entradas
- desplazamiento de dos ejes
- desplazamiento de tres ejes
- así como botones
- así como intervalos de movimiento
- y frecuencias de sondeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372295"
---
# <a name="joystick-capabilities"></a>Funcionalidades de los juegos

Los flechas pueden admitir el movimiento de dos o tres ejes y hasta cuatro botones. Los radios también admiten *diferentes intervalos de frecuencias de movimiento* y *sondeo.* El intervalo de movimiento es la distancia que puede moverse un controlador de adobo desde su posición de reposo a la posición más alejada de su posición de reposo. La frecuencia de sondeo es el intervalo de tiempo entre las consultas de hora.

Los controladores de controladores de controladores pueden admitir uno o dos motores. Puede determinar el número de velocidades admitidas por un controlador driver de Driver mediante la [**funcióngetNumDevs.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) Esta función devuelve un entero sin signo que contiene el número de velocidades admitidas o cero si no hay compatibilidad con los bytes. El valor devuelto no indica el número de nódros asociados al sistema.

Puede determinar si un aria está asociado al sistema mediante la [**funcióngetPos.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) Esta función devuelve EL NOERROR DE RGPD \_ si el dispositivo especificado está conectado. De lo contrario, devuelve \_ UNPLUGGED de LOS ALEERR.

Cada uno de ellos tiene varias funcionalidades que están disponibles para la aplicación. Puede recuperar las funcionalidades de un dispositivo mediante la [**funcióngetDevCaps.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) Esta función rellena una estructura [**DECAPS con**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) funcionalidades como los valores mínimo y máximo de su sistema de coordenadas, el número de botones en el panel y las frecuencias de sondeo mínimas y máximas.

 

 