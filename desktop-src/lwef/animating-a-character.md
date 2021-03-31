---
title: Animar un carácter
description: Animar un carácter
ms.assetid: ed42de30-acac-41e8-bacb-4caaff254724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed47b30a9bcfcdb5e305b87ced5f02526ae0056
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077629"
---
# <a name="animating-a-character"></a>Animar un carácter

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Una vez cargado un carácter, puede usar varios métodos de Microsoft Agent para animar el carácter. El primero que se usa es normalmente el método [**Show**](show-method.md) . **Mostrar** hace que el marco del carácter sea visible y reproduce la animación asignada al estado en el **que se muestra** el carácter.

Una vez que el marco del carácter esté visible, puede usar el método [**Play**](play-method.md) , especificando el nombre de una animación, para reproducir esa animación. Los nombres de animación son específicos de una definición de caracteres. A medida que se reproduce una animación, la forma de la ventana cambia para coincidir con la imagen del marco. Esto da como resultado una imagen gráfica móvil, o *Sprite*, que se muestra en la parte superior del escritorio y en todas las ventanas, o en el *orden z*.

Si el archivo del carácter está almacenado localmente, simplemente puede llamar al método [**Play**](play-method.md) . En otros casos, como cuando se ha cargado un. Carácter ACF de un servidor HTTP, debe usar el método [**Get**](get-method.md) (o [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare)) para recuperar primero los datos de la animación. Esto hará que el agente solicite el archivo de animación del servidor y lo almacene en el búfer del explorador en el equipo local.

El método [**Speak**](speak-method.md) permite programar el carácter que se va a hablar, sincronizando automáticamente la salida de Lip. En la sección salida de este documento se explican más detalles.

Puede usar el método [**moveTo**](moveto-method.md) para colocar el carácter en una nueva ubicación. Cuando se llama al método **moveTo** , el agente de Microsoft reproduce automáticamente la animación adecuada en función de la ubicación actual del carácter y, a continuación, mueve el fotograma del carácter. Del mismo modo, cuando se llama a [**GestureAt**](gestureat-method.md), el agente de Microsoft reproduce la animación gesturing adecuada en función de la ubicación del carácter y la ubicación especificada en la llamada.

Para ocultar el carácter, llame al método [Hide](hide-method.md) . Esto reproduce automáticamente el carácter asociado al estado de **ocultación** del carácter y, a continuación, oculta el fotograma del carácter. Sin embargo, también puede ocultar o mostrar un carácter estableciendo la propiedad [**visible**](visible-property.md) del carácter.

El agente de Microsoft procesa todas las llamadas de animación, o *solicitudes*, de forma asincrónica. Esto permite al código de la aplicación seguir controlando otros eventos mientras se procesa la solicitud. Por ejemplo, las llamadas al método [**Play**](play-method.md) colocan la animación en una cola para el carácter de modo que las animaciones se puedan reproducir secuencialmente. Sin embargo, esto significa que no se puede suponer que una llamada a otras funciones se ejecutará necesariamente después de la animación que sigue en el código. Por ejemplo, normalmente, una instrucción que sigue a una llamada a **Play** o [**moveTo**](moveto-method.md) se ejecutará antes de que finalice la animación.

Puede sincronizar el código con animaciones en la cola de un carácter creando una referencia de objeto a la solicitud de animación y, cuando la animación se inicia o se completa, supervisando los eventos de [solicitud](the-request-object.md) que el servidor utiliza para notificar a los clientes el carácter. Por ejemplo, si desea que aparezca un cuadro de mensaje cuando el carácter finaliza una animación, puede colocar la llamada del cuadro de mensaje en la subrutina de control de eventos de [**RequestComplete**](requestcomplete-event.md) , comprobando el identificador de solicitud determinado.

Cuando se oculta un carácter, el servidor no reproduce animaciones; sin embargo, todavía pone en cola y procesa la solicitud de animación (reproduce la animación) y pasa de nuevo el estado de la solicitud al cliente. En el estado oculto, el carácter no puede ser de entrada-activo. Sin embargo, si el usuario habla el nombre del carácter (cuando está habilitada la entrada de voz), el servidor muestra automáticamente el carácter.

Cuando la aplicación cliente carga varios caracteres al mismo tiempo, los servicios de animación de Microsoft Agent permiten animar los caracteres de forma independiente o usar los métodos [**Wait**](wait-method.md), [**Interrupt**](interrupt-method.md)o [**Stop**](stop-method.md) para sincronizar la animación entre sí.

El agente de Microsoft también reproduce otras animaciones automáticamente. Por ejemplo, si el estado del carácter no ha cambiado durante varios segundos, el agente comienza a reproducir animaciones asignadas a las animaciones de **ralentí** del carácter. Del mismo modo, cuando la entrada de voz está habilitada, el agente desempeña las animaciones de **escucha** del carácter y, a continuación, **escucha** animaciones cuando se detecta un utterance. Estas animaciones administradas por el servidor se denominan *Estados* y se definen cuando se crea un carácter. Para obtener más información, vea [diseñar caracteres para el agente de Microsoft](agent-states.md).

 

 