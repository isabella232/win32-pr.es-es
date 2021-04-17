---
description: En la versión 3,0 de TAPI y versiones posteriores, el modelo de objetos de TAPI utiliza objetos de terminal para representar el origen o el receptor de un flujo multimedia asociado a una sesión de llamada o de comunicaciones.
ms.assetid: 0d96f229-76c0-46a3-bc4b-6f558b9956c6
title: Objeto terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2568d3c6f047fec8ca46b3b7d56e5026b61a1113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678556"
---
# <a name="terminal-object"></a>Objeto terminal

En la versión 3,0 de TAPI y versiones posteriores, el modelo de objetos de TAPI utiliza objetos de terminal para representar el origen o el receptor de un flujo multimedia asociado a una sesión de llamada o de comunicaciones. Este modelo de objetos permite a una aplicación especificar, en un nivel detallado, cómo se procesan los elementos multimedia en una llamada. Este modelo también permite seleccionar varios terminales simultáneamente, por lo que, por ejemplo, se puede enviar una llamada a un altavoz de audio y grabarse simultáneamente.

El objeto terminal representa un origen o un representador, como un micrófono o un altavoz. Una aplicación elige entre los terminales disponibles en función de la dirección del medio y tipo o tipos implicados en una sesión de comunicaciones. Cada flujo de medios asociado se selecciona en el terminal adecuado para iniciar el streaming.

Los terminales se implementan normalmente mediante un proveedor de servicios multimedia (MSP) y los objetos de terminal no estarán disponibles si no hay ningún MSP asociado a una sesión de comunicaciones. Una excepción es que con Windows 2000 SP1 y versiones posteriores, una aplicación puede implementar una forma de [terminal conectable](pluggable-terminals.md). Esto permite que un servidor de conferencia cree terminales de puente de modo que se puedan agregar a los clientes de la multidifusión de los servidores SDP/IP de Windows 2000 SP1 o de multidifusión.

Cada terminal pertenece a una [clase de terminal](terminal-class.md). Una clase de terminal representa un conjunto de características de origen o representación. Por ejemplo, un terminal que se asigna a un conjunto de altavoces de audio se identificaría como CLSID \_ SpeakersTerminal y se espera que el proveedor de servicios implemente el control de volumen. TAPI 3 define un conjunto de clases de terminal, un MSP puede definir clases adicionales y una aplicación puede registrar nuevas clases de terminal. A cada clase de terminal se le asigna un identificador único global (GUID).

Desde el punto de vista de una aplicación, un terminal se describe mediante su [tipo de terminal](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_type) y [Dirección](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction). El tipo puede ser estático o dinámico. Un terminal estático se asigna a hardware, como un teléfono o micrófono. Un terminal dinámico se asigna a un objeto transitorio, como un archivo o una ventana de vídeo. Direction describe si un terminal determinado es un origen o un representador.

Las capacidades de un objeto de terminal determinado pueden variar considerablemente dependiendo del par de proveedores de servicios actual en uso. El MSP de un dispositivo especializado podría implementar una interfaz con los métodos adecuados para ese dispositivo. Esa interfaz se podría agregar en el objeto terminal y los métodos están disponibles para una aplicación. Para obtener más información y material de referencia, consulte la documentación del proveedor de servicios multimedia.

Para obtener más información acerca de las interfaces de terminal y métodos implementados por TAPI 3, consulte [interfaces de objetos de terminal](terminal-object-interfaces.md).

Si los autores de un proveedor de servicios multimedia usan las clases base MSP, pueden implementar algunas de las características del terminal de streaming multimedia.

Para obtener más información y ejemplos de código que muestren ilustraciones sobre el uso de un objeto terminal, consulte [hacer una llamada](make-a-call.md) y [recibir una llamada](receive-a-call.md).

**Windows XP:** Para obtener más información acerca de cómo se ha expandido el objeto terminal en Windows XP, consulte [terminales de archivos](file-terminals.md), [terminales multipista](multitrack-terminals.md)y [terminales conectables](pluggable-terminals.md).

Para obtener más información y ejemplos de código, vea [usar terminales de archivos](using-file-terminals.md), [usar terminales multipista y el mecanismo de selección predeterminado y el](using-multitrack-terminals-and-the-default-selection-mechanism.md) [registro de terminales conectables](pluggable-terminal-registration.md).

 

 



