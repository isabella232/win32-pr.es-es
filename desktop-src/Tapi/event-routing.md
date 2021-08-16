---
description: Con la función lineSetTerminal, la aplicación puede controlar o suprimir el enrutamiento de eventos de bajo nivel especificados (intercambiados entre el conmutador y la estación) a un dispositivo.
ms.assetid: 36658d83-0ea4-4f62-b2e5-c0f6d6569d0d
title: Enrutamiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13c71d07994090a1e68fcbadd1cd3b686a3de316e4a6fd01cca506fcdbcdbd00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763106"
---
# <a name="event-routing"></a>Enrutamiento de eventos

Con la [**función lineSetTerminal,**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) la aplicación puede controlar o suprimir el enrutamiento de eventos de bajo nivel especificados (intercambiados entre el conmutador y la estación) a un dispositivo. Con **lineSetTerminal**, la aplicación especifica el dispositivo terminal al que se enruta estos eventos (por ejemplo, línea, dirección o llamada a eventos de flujo multimedia).

El enrutamiento de las diferentes clases de eventos se puede controlar individualmente, lo que permite especificar terminales independientes para cada clase de evento. Las clases de eventos incluyen bombillas, botones, pantalla, timbre, conmutador de enlace y secuencia multimedia.

Por ejemplo, el flujo multimedia de una llamada (voz, por ejemplo) se puede enviar a cualquier dispositivo de la zona si el proveedor de servicios y el hardware son capaces de hacerlo. En general, un *artefacto* significa lo mismo que lo que se conoce como un dispositivo *de* interruptor de enlace en TAPI, algo que tiene un micrófono y un altavoz. Los eventos de anillo del conmutador al teléfono se pueden asignar a una alerta visual en la pantalla del equipo o se pueden enrutar a un dispositivo de teléfono. Los eventos lamp y display se pueden omitir o enrutar a un dispositivo de teléfono (que parece comportarse como un conjunto de teléfonos normal). Por último, las pulsaciones de botón en un dispositivo de teléfono pueden o no pasarse a la línea. En cualquier caso, este enrutamiento de señales de bajo nivel desde la línea no afecta al funcionamiento de la parte de línea de TAPI, que siempre asigna eventos de bajo nivel a su equivalente funcional. Para determinar los terminales que un dispositivo de línea tiene disponible (y sus funcionalidades), consulte las funcionalidades del dispositivo de línea [**con lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps).

Supongamos inicialmente que la aplicación ha suprimido el enrutamiento de todos los eventos (con [**lineSetTerminal)**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal)y el usuario selecciona un casco como el dispositivo de E/S actual. Una llamada entrante envía un [**mensaje LINE \_ CALLSTATE**](line-callstate.md) y un [**mensaje LINE \_ LINEDEVSTATE**](line-linedevstate.md) con la *indicación de timbre.* Dado que se suprime el enrutamiento de todos los eventos, los eventos de anillo no se enruta al teléfono, por lo que se suprime el timbre. En su lugar, la aplicación notifica al usuario con un cuadro de diálogo emergente y un pitido del sistema en el casco.

El usuario decide responder a la llamada. Dado que el dispositivo de E/S actual del usuario es el casco, la aplicación de telefonía invoca [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) en la llamada entrante para enrutar los medios de la llamada al casco y responder a la llamada. La aplicación también puede invocar **lineSetTerminal** para enrutar la bombilla y mostrar eventos de información al conjunto de teléfonos para que se comporte como de costumbre.

Como segundo ejemplo, suponga que una llamada entrante está generando alertas en el equipo del usuario. En lugar de seleccionar la opción de respuesta con el mouse, el usuario decide simplemente recoger el terminal del teléfono para responder a la llamada. El estado del offhook en el teléfono envía un mensaje a la aplicación. La aplicación puede interpretar este estado como una solicitud del usuario para seleccionar el teléfono para llevar a cabo la conversación. A continuación, la aplicación invoca [**lineSetTerminal para**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) enrutar los datos de voz de la llamada al conjunto de teléfonos.

 

 



