---
title: Notificaciones informativas
description: Para los Estados de conexión conocidos como Estados en ejecución, no se requiere ninguna acción del controlador de notificación a menos que se produzca un error.
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6223c808309fcac3afc563f02c160412c80c88
ms.sourcegitcommit: dc13cc13522097188392392d85f99de48a213984
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2020
ms.locfileid: "104487362"
---
# <a name="informational-notifications"></a>Notificaciones informativas

Para los [Estados de conexión](connection-states.md) conocidos como Estados en ejecución, no se requiere ninguna acción del controlador de notificación a menos que se produzca un error. Los Estados de ejecución se producen durante las partes de la operación de conexión que RAS administra automáticamente, como la conexión a los dispositivos necesarios, la autenticación del usuario y la espera de una devolución de llamada desde el servidor remoto. La notificación es simplemente un informe de progreso para el cliente.

El cliente puede optar por pasar estas notificaciones informativas al usuario. En algunos Estados en ejecución, es posible que el cliente desee mostrar información adicional. Por ejemplo, un controlador de notificación que recibe una \_ notificación ConnectDevice de RASCS puede llamar a la función [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obtener el nombre y el tipo del dispositivo al que se está conectando. Otro ejemplo es cuando el cliente recibe una notificación de RASCS \_ proyectada. Esto sucede cuando se ha completado la fase de proyección de RAS de la operación de conexión. El cliente puede llamar a la función [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) para obtener información adicional sobre la proyección. El cliente puede usar esta información para notificar al usuario en qué protocolos de red puede usar esta conexión.

Debe evitar escribir código que dependa del orden o la aparición de Estados informativos determinados, ya que puede variar entre las distintas plataformas.

 

 




