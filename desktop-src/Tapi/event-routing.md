---
description: Con la función lineSetTerminal, la aplicación puede controlar o suprimir el enrutamiento de eventos de bajo nivel especificados (intercambiados entre el conmutador y la estación) a un dispositivo.
ms.assetid: 36658d83-0ea4-4f62-b2e5-c0f6d6569d0d
title: Enrutamiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6749969faf89ac0212c19049fe02c9dad57a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686785"
---
# <a name="event-routing"></a>Enrutamiento de eventos

Con la función [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) , la aplicación puede controlar o suprimir el enrutamiento de eventos de bajo nivel especificados (intercambiados entre el conmutador y la estación) a un dispositivo. Con **lineSetTerminal**, la aplicación especifica el dispositivo de terminal al que se enrutan estos eventos (como la línea, la dirección o los eventos de secuencia de medios de llamada).

El enrutamiento de las distintas clases de eventos se puede controlar individualmente, lo que permite especificar terminales independientes para cada clase de eventos. Entre las clases de eventos se incluyen las luces, los botones, la pantalla, el timbre, el conmutador y el flujo multimedia.

Por ejemplo, el flujo de medios de una llamada (por ejemplo, voz) se puede enviar a cualquier dispositivo de transductor si el proveedor de servicios y el hardware son capaces de hacerlo. En general, un *transductor* significa lo mismo que lo que se conoce como dispositivo *conmutador* en TAPI, algo que tiene un micrófono y un altavoz. Los eventos de anillo del conmutador al teléfono se pueden asignar a una alerta visual en la pantalla del equipo o se pueden enrutar a un dispositivo telefónico. Los eventos de lámpara y los eventos de visualización se pueden omitir o enrutar a un dispositivo telefónico (que parece que se comporta como un conjunto de teléfonos normal). Por último, las pulsaciones de botón en un dispositivo telefónico pueden o no pasarse a la línea. En cualquier caso, este enrutamiento de señales de bajo nivel de la línea no afecta al funcionamiento de la parte de la línea de TAPI, que siempre asigna eventos de bajo nivel a su equivalente funcional. Para determinar los terminales que tiene un dispositivo de línea disponible (y sus funcionalidades), consulte las funcionalidades del dispositivo de línea con [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps).

Suponga inicialmente que la aplicación ha suprimido el enrutamiento de todos los eventos (con [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal)) y el usuario selecciona un casco como dispositivo de e/s actual. Una llamada entrante envía un mensaje de [**línea \_ CALLSTATE**](line-callstate.md) y un mensaje de [**línea \_ LINEDEVSTATE**](line-linedevstate.md) con la indicación de *timbre* . Dado que se suprime el enrutamiento de todos los eventos, los eventos de anillo no se enrutan al teléfono, por lo que se suprime el anillo. En su lugar, la aplicación notifica al usuario con un cuadro de diálogo emergente y un pitido del sistema en el casco.

El usuario decide responder a la llamada. Dado que el dispositivo de e/s actual del usuario es el casco, la aplicación de telefonía invoca [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) en la llamada entrante para enrutar los medios de la llamada al casco y responder a la llamada. La aplicación también puede invocar **lineSetTerminal** para enrutar los eventos de información LAMP y de presentación al conjunto de teléfonos para que se comporte de la forma habitual.

Como segundo ejemplo, supongamos que una llamada entrante se alerta en el equipo del usuario. En lugar de seleccionar la opción de respuesta con el mouse, el usuario decide simplemente seleccionar el auricular del teléfono para responder a la llamada. El estado OffHook en el teléfono envía un mensaje a la aplicación. La aplicación puede interpretar este estado como una solicitud del usuario para seleccionar el auricular del teléfono para realizar la conversación. A continuación, la aplicación invoca [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) para enrutar los datos de voz en la llamada al conjunto de teléfonos.

 

 



