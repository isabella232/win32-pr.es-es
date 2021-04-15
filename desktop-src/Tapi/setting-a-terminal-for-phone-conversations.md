---
description: Es posible que el equipo de los usuarios tenga acceso a varios dispositivos que puede seleccionar el usuario y que se usan para realizar conversaciones de voz interactivas.
ms.assetid: cc7ad70a-157e-4db4-b5e4-00d25686a9dd
title: Configuración de un terminal para conversaciones telefónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b12e772d8f941cb7c68e25136a843ec5f9a1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688622"
---
# <a name="setting-a-terminal-for-phone-conversations"></a>Configuración de un terminal para conversaciones telefónicas

El equipo del usuario puede tener acceso a varios dispositivos que son seleccionables por el usuario y que se usan para realizar conversaciones de voz interactivas. En primer lugar, hay un dispositivo telefónico en sí, con luces, botones, pantalla, timbre y dispositivo de e/s de voz (auricular, altavoz, auriculares). El equipo del usuario también puede tener un dispositivo de e/s de voz independiente (por ejemplo, un auricular o una combinación de micrófono/altavoz conectado a una tarjeta de sonido) para su uso con conversaciones telefónicas.

TSPI permite al usuario seleccionar dónde enrutar la información que el modificador envía a través de la línea, la dirección o la llamada. Normalmente, el conmutador espera que sea uno de sus conjuntos de teléfonos y envía solicitudes de timbre, eventos de lámpara (para teléfonos de estímulo), datos de presentación y datos de voz según corresponda. El teléfono, a su vez, envía eventos conmutador, eventos de pulsación de botones (para teléfonos de estímulo) y datos de voz de vuelta al conmutador.

La parte de la *línea* de TSPI hace que los eventos de lámpara, los eventos de visualización y los eventos de anillo estén disponibles, ya sea como códigos de retorno funcionales para las distintas operaciones de línea de TSPI, o como mensajes de estado de llamada funcional no solicitados que se envían a la devolución de llamada de la aplicación. La implementación del proveedor de servicios es responsable de la asignación entre el nivel funcional de TSPI y el estímulo subyacente o los mensajes funcionales que usa la red de telefonía. En entornos de telefonía funcional, las funciones de TSPI se asignan al protocolo funcional.

Con la función [**TSPI \_ LINESETTERMINAL**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) , TAPI puede controlar el enrutamiento de distintos eventos de bajo nivel intercambiados entre el conmutador y la estación; también puede decidir no enrutar algunos de estos eventos de bajo nivel a un dispositivo. El enrutamiento de las distintas clases de eventos se puede controlar de forma individual. Por ejemplo, el flujo de medios de una llamada (por ejemplo, voz) se puede enviar a cualquier dispositivo de transductor si el proveedor de servicios y el hardware son capaces de hacerlo. Los eventos de anillo del conmutador al teléfono se pueden asignar a una alerta visual en la pantalla del equipo o se pueden enrutar a un dispositivo telefónico. Los eventos de lámpara y los eventos de visualización se pueden omitir o enrutar a un dispositivo telefónico (que parece que se comporta como un conjunto de teléfonos normal). Por último, las pulsaciones de botón en un dispositivo telefónico pueden pasarse o no a la línea. En cualquier caso, este enrutamiento de señales de bajo nivel de la línea no afecta al funcionamiento de la parte de la línea de TSPI, que siempre asigna los eventos de bajo nivel a su equivalente funcional. Las aplicaciones pueden consultar las capacidades de los dispositivos de una línea para determinar los terminales que tiene disponibles.

En otras palabras, la función [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) especifica el dispositivo de terminal al que se enrutan los eventos de línea, eventos de dirección o secuencia de medios de llamada especificados. Se pueden especificar terminales independientes para cada clase de eventos. Entre las clases de eventos se incluyen las luces, los botones, la pantalla, el timbre, el conmutador y el flujo multimedia.

 

 
