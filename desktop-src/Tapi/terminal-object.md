---
description: En TAPI versión 3.0 y posteriores, el modelo de objetos TAPI usa objetos de terminal para representar el origen o receptor de una secuencia multimedia asociada a una llamada o una sesión de comunicaciones.
ms.assetid: 0d96f229-76c0-46a3-bc4b-6f558b9956c6
title: Objeto terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe85dcf2643cbf60835a7df9e8b20de8287da2c752ed6555f480609d9b79873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476265"
---
# <a name="terminal-object"></a>Objeto terminal

En TAPI versión 3.0 y posteriores, el modelo de objetos TAPI usa objetos de terminal para representar el origen o receptor de una secuencia multimedia asociada a una llamada o una sesión de comunicaciones. Este modelo de objetos permite a una aplicación especificar, en un nivel detallado, cómo se procesan los medios en una llamada. Este modelo también permite seleccionar varios terminales simultáneamente, por lo que, por ejemplo, se puede generar una llamada a un altavoz de audio y grabarse simultáneamente.

El objeto Terminal representa un origen o representador, como un micrófono o un altavoz. Una aplicación elige entre los terminales disponibles en función de la dirección del medio y el tipo o los tipos implicados en una sesión de comunicaciones. A continuación, cada secuencia multimedia asociada se selecciona en el terminal adecuado para iniciar el streaming.

Los terminales normalmente los implementa un proveedor de servicios multimedia (MSP) y los objetos de terminal no estarán disponibles si no hay ningún MSP asociado a una sesión de comunicaciones. Una excepción es que con Windows 2000 SP1 y versiones posteriores, una aplicación puede implementar una forma de [terminal conectable](pluggable-terminals.md). Esto permite que un servidor de conferencias cree terminales de puente para que se puedan agregar clientes que no sean de Windows 2000 SP1 o H323 sin multidifusión a las conferencias de multidifusión SDP/IP de TAPI 3.

Cada terminal pertenece a una [clase de terminal](terminal-class.md). Una clase de terminal representa un conjunto de características de origen o representación. Por ejemplo, un terminal que se asigna a un conjunto de altavoces de audio se identificaría como CLSID SpeakersTerminal y se esperaría que el proveedor de servicios implementara el \_ control de volumen. TAPI 3 define un conjunto de clases de terminal, un MSP puede definir clases adicionales y una aplicación puede registrar nuevas clases de terminal. A cada clase de terminal se le asigna un identificador único global (GUID).

Desde el punto de vista de una aplicación, un terminal se describe por su [tipo de terminal y](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_type) [dirección.](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) El tipo puede ser estático o dinámico. Un terminal estático se asigna al hardware, como un teléfono o un micrófono. Un terminal dinámico se asigna a un objeto transitorio, como un archivo o una ventana de vídeo. Direction describe si un terminal determinado es un origen o un representador.

Las funcionalidades de un objeto terminal determinado pueden variar considerablemente en función del par de proveedores de servicios actual en uso. El MSP de un dispositivo especializado podría implementar una interfaz con métodos adecuados para ese dispositivo. Esa interfaz se podría agregar al objeto terminal y los métodos disponibles para una aplicación. Para obtener más información y material de referencia, consulte la documentación del proveedor de servicios multimedia.

Para obtener más información sobre las interfaces de terminal y los métodos implementados por TAPI 3, vea [Terminal Object Interfaces](terminal-object-interfaces.md).

Si los autores de un proveedor de servicios multimedia usan las clases base msp, pueden implementar algunas de las características de Terminal de streaming multimedia.

Para obtener más información y ejemplos de código que muestran ilustraciones del uso de un objeto Terminal, vea [Realizar](make-a-call.md) una llamada y [recibir una llamada .](receive-a-call.md)

**Windows XP:** Para obtener más información sobre cómo se ha expandido el objeto terminal en Windows XP, vea [Terminales](file-terminals.md)de archivo, [Terminales](multitrack-terminals.md)multipista y [Terminales conectables.](pluggable-terminals.md)

Para obtener más información y ejemplos de código, vea Using [File Terminals](using-file-terminals.md), [Using Multitrack Terminals and the Default Selection Mechanism](using-multitrack-terminals-and-the-default-selection-mechanism.md)y [Pluggable Terminal Registration](pluggable-terminal-registration.md).

 

 



