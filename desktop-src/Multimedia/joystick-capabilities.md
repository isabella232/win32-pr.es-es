---
title: Funcionalidades de Capacidades de Capacidades
description: Funcionalidades de Capacidades de Capacidades
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- entrada multimedia, entradas
- desplazamiento de dos ejes
- desplazamiento de tres ejes
- controles, botones
- y, por último, intervalos de movimiento
- y frecuencias de sondeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161400"
---
# <a name="joystick-capabilities"></a>Funcionalidades de Capacidades de Capacidades

Los ejes pueden admitir el movimiento de dos o tres ejes y hasta cuatro botones. Los radios también admiten *diferentes intervalos de frecuencias de movimiento* y *sondeo.* El intervalo de movimiento es la distancia a la que un asa de manija puede moverse desde su posición de reposo a la posición más alejada de su posición de reposo. La frecuencia de sondeo es el intervalo de tiempo entre consultas de intervalo.

Los controladores de controladores de controladores pueden admitir uno o dos velocidades. Puede determinar el número de velocidades admitidas por un controlador de driver mediante la [**funcióngetGetNumDevs.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) Esta función devuelve un entero sin signo que contiene el número de velocidades admitidas o cero si no hay compatibilidad con los bytes. El valor devuelto no indica el número de vehículos conectados al sistema.

Puede determinar si se adjunta un vuelo al sistema mediante la [**funcióngetPos.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) Esta función devuelve EL NOERROR DE \_ SELEERR si el dispositivo especificado está conectado. De lo contrario, devuelve \_ UNPLUGGED de DRAGERR.

Cada uno de ellos tiene varias funcionalidades que están disponibles para la aplicación. Puede recuperar las funcionalidades de un objeto mediante la [**funcióngetDevCaps.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) Esta función rellena una estructura [**DECAPS CON**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) funcionalidades como los valores mínimos y máximos de su sistema de coordenadas, el número de botones en el radio y las frecuencias de sondeo mínimas y máximas.

 

 