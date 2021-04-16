---
description: Cuando una aplicación tiene privilegios de propietario para una sesión de comunicaciones, la aplicación puede optar por entregar la propiedad a otra aplicación.
ms.assetid: d6d188c9-9cbd-45af-93f0-b78850374919
title: Entregas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343815e35f1fc331c57c4aa2d9d311697cab7022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677512"
---
# <a name="handoffs"></a>Entregas

Cuando una aplicación tiene [privilegios](privilege-ovr.md) de propietario para una sesión de comunicaciones, la aplicación puede optar por entregar la propiedad a otra aplicación. La operación de entrega se usa normalmente para permitir que se cambie el tipo de medio de la llamada. La aplicación de prioridad más alta para el nuevo tipo de medio debe tomar y controlar la llamada. El cambio de tipo de medio normalmente se produce por uno de los siguientes motivos.

**Comando de usuario:** A través de una interfaz de usuario o a través de mensajes de ventana, la aplicación aprende que el usuario local desea cambiar el tipo de medio. Por ejemplo, el usuario ha indicado la nueva aplicación de destino (que todavía no es un propietario) para obtener una llamada de voz existente para la transmisión de datos. La aplicación de destino debe tomar el control de la llamada. En este caso, el propietario actual observa el aumento del número de propietarios y, a continuación, renuncia a su control de la llamada. Como alternativa, el usuario podría indicar al propietario actual de la llamada que lo entregue a una aplicación que pueda controlar el nuevo tipo de medio.

**Cambio de tipo de medio:** El proveedor de servicios puede detectar un cambio de tipo de medio. Por ejemplo, la aplicación local está reproduciendo un mensaje de voz grabado para el autor de la llamada. Durante este mensaje, el autor de la llamada decide de forma espontánea de transmitir un tono de llamada de fax, y la aplicación local puede responder en consecuencia cambiando el tipo de medio a fax y, si es necesario, entregando la llamada a una aplicación de fax. Otra forma de hacerlo es que una aplicación de supervisión habilite la supervisión de tipos de medios y, cuando se detecte el tipo de medio en el que está interesado en una llamada, puede solicitar la propiedad de la llamada. Este mecanismo hace que sea innecesario que cada aplicación supervise cada llamada para cada tipo de medio.

**Comando de entidad remota:** La parte remota puede indicar interactivamente un cambio en los tipos de medios durante una llamada existente, por ejemplo, si la aplicación local supervisa la entrada de DTMF por parte del llamador remoto. A través de esta supervisión, el autor de la llamada indica, por ejemplo, que se va a enviar un fax. Otras formas en las que el autor de la llamada puede controlar las aplicaciones locales con comandos recibidos en otras conexiones de datos y a través de mensajes de información de usuario de usuario ISDN.

Una entrega de llamada tendrá uno de estos resultados:

-   La llamada se proporciona a otra aplicación (SUCCEss).
-   La aplicación de entrega es el destino (TARGETSELF).
-   Se produce un error en la entrega (TARGETNOTFOUND).

Si la aplicación que recibe la llamada entregada ya tiene un identificador de llamada a la llamada, se utiliza este identificador de llamada anterior. De lo contrario, se crea un nuevo identificador de llamada. En cualquier caso, la aplicación finaliza con privilegios de propietario en la llamada. Siempre que la aplicación de entrega no sea la misma que la aplicación de destino, se informa al destino sobre la entrega en un mensaje de estado de sesión como si estuviera recibiendo una nueva llamada.

Si se indica a la aplicación propietaria actual que cambie los tipos de medios, lo hace mediante la entrega de la llamada a una aplicación que se usa para el tipo de medio de destino. Los dos tipos de llamadas entregas se describen en [entregas dirigido](#directed-handoffs) y el [tipo de medio entregas](#media-type-handoffs).

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2. x:** Vea [**lineHandoff**](/windows/win32/api/tapi/nf-tapi-linehandoff), con *lpszFileName* establecido en el nombre de aplicación para una entrega directa o *dwMediaMode* establecido en un tipo de medio para una entrega indirecta.

**TAPI 3. x:** Vea [**ITBasicCallControl:: HandoffDirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffdirect), [**ITBasicCallControl:: HandoffIndirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffindirect).

## <a name="directed-handoffs"></a>Entregas dirigido

Una *entrega dirigida* tiene lugar cuando la aplicación de destino se conoce por nombre en la aplicación original. Esta situación se produciría, por ejemplo, entre un conjunto de aplicaciones escritas por el mismo proveedor. Normalmente, el usuario puede configurar el control de entregas dirigidos. Con este tipo de entrega, se proporciona la llamada a la aplicación especificada si ha abierto la línea en la que existe la llamada. Se omite el tipo de medio especificado en el momento en que se ha abierto la línea de la aplicación. Un ejemplo común es una llamada de voz seguida de una transmisión de fax en la misma llamada. La entrega dirigida normalmente la usan las aplicaciones del mismo desarrollador que están vinculadas de otras maneras.

La entrega dirigida también puede usarse en versiones futuras como parte del proceso de arbitración de varias aplicaciones que esperan llamadas entrantes del mismo tipo de medio, con la selección de la aplicación para controlar la llamada basada en el vínculo de datos o en la detección de protocolo de nivel superior en lugar de un tipo de medio. Un ejemplo de su uso sería una línea de módem de datos de entrada con aplicaciones como la adquisición remota, el tablón de anuncios, el acceso remoto a la red y el acceso a correo electrónico remoto todo en espera de llamadas simultáneamente.

## <a name="media-type-handoffs"></a>Tipo de medio entregas

La *entrega* de un tipo de medio tiene lugar cuando hay un nuevo tipo de medio de destino, normalmente cuando la aplicación propietaria determina que el tipo de medio necesario para la llamada no está presente o está a punto de cambiar.

El proceso para una entrega dependiente del medio puede ser un proceso de sondeo si el tipo de medio bit desconocido es on. Es responsabilidad de la aplicación propietaria recorrer los tipos de medios para encontrar la aplicación de prioridad más alta. TAPI realiza este ciclo solo en la llamada de entrada inicial para buscar el primer propietario. No realiza esto para una operación de entrega. De lo contrario, una entrega es prácticamente la misma que para la asignación inicial de una llamada a una aplicación. La diferencia es el hecho de que solo se puede establecer un tipo de medio para una entrega indirecta (tipo de medio).

Dado que solo se puede especificar un bit de tipo de medio, se proporciona la llamada a la aplicación de prioridad más alta para ese tipo de medio. Sin embargo, es posible que se tenga en cuenta más de un tipo de medio para la entrega. En este caso, la aplicación de entrega debe especificar la prioridad más alta de los posibles tipos de medios como parámetro.

Si una aplicación especifica el bit desconocido al realizar una entrega de tipo multimedia y se produce un error en la entrega, significa que una aplicación desconocida capaz de realizar la determinación del tipo de medio no se está ejecutando actualmente. A continuación, la aplicación que se entrega se intenta entregar la llamada a la aplicación de prioridad más alta registrada para el siguiente tipo de medio.

La aplicación receptora ahora es responsable de la llamada. Ahora sondea el tipo de medio real de la llamada. Si la aplicación puede controlar el tipo de medio de la llamada, debe asegurarse de que es la aplicación de prioridad más alta registrada para ese tipo de medio. Si es así, mantiene la llamada y la procesa normalmente. Si no es así, entrega la llamada a otra aplicación registrada para ese tipo de medio.

Sin embargo, si se produce un error en el sondeo de ese tipo de archivo multimedia, la aplicación sondea de nuevo, intentando las posibilidades de modo multimedia restantes. Primero debe desactivar el bit actual del tipo de medio y, a continuación, intentar otra entrega con un tipo diferente.

Este proceso de sondeo y entrega continuará, y los demás tipos de medios se eliminarán uno por uno. A lo largo del proceso, una de las aplicaciones puede ver que el tipo de medio que controla está en la llamada y la entrega se realiza correctamente.

A continuación, la aplicación debe establecer el tipo de medio correcto y borrar todos los demás bits de tipo de medio. Esto informa a otras aplicaciones interesadas del tipo de medio correcto. Estas otras aplicaciones reciben un mensaje de notificación de eventos que indica que el tipo de medio de la llamada ha cambiado.

 

 
